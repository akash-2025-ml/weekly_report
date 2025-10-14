# Data Extraction Guide for IMMEDIATE ACTIONS

## Your Current Data Structure
- 68 signals for each email
- Email text and subject
- Email sender and receiver
- Email classification (Safe/Warning/Spam/Malicious)
- Action status (Done/Pending)

## Data Extraction Process for IMMEDIATE ACTIONS

### Step 1: Calculate Base Metrics

```python
# Example extraction logic
total_emails = count(all_emails)
malicious_emails = count(emails WHERE class = 'Malicious')
malicious_percentage = (malicious_emails / total_emails) * 100

# Week comparison (requires historical data)
malicious_this_week = count(malicious WHERE date >= week_start)
malicious_last_week = count(malicious WHERE date >= last_week_start AND date < week_start)
```

### Step 2: Extract Required Data Points

#### 1. VENDOR COMPROMISES
**What to look for:**
- Group malicious emails by sender domain
- Compare this week vs last week counts
- Identify known vendor domains

**SQL-like query:**
```sql
SELECT 
    sender_domain,
    COUNT(*) as threats_this_week,
    LAG(COUNT(*), 1, 0) as threats_last_week
FROM emails
WHERE class = 'Malicious'
GROUP BY sender_domain, week
HAVING threats_this_week > threats_last_week * 3
```

**Manual extraction:**
1. List all sender domains from malicious emails
2. Count emails per domain this week
3. Count emails per domain last week
4. Calculate percentage increase
5. Flag if domain is a known vendor/partner

#### 2. DEPARTMENT TARGETING
**What to look for:**
- Group malicious emails by receiver department
- Identify threat types from signals/subject analysis
- Calculate percentage of total threats

**Extraction process:**
```python
# Group by receiver email domain/department
finance_threats = count(malicious WHERE receiver LIKE '%finance%' OR receiver LIKE '%accounts%')
hr_threats = count(malicious WHERE receiver LIKE '%hr%' OR receiver LIKE '%human%')
it_threats = count(malicious WHERE receiver LIKE '%it%' OR receiver LIKE '%tech%')

# Calculate percentages
finance_percentage = (finance_threats / total_malicious) * 100
```

**Threat type identification from signals:**
- BEC/CEO Fraud: Signals indicating urgency + financial requests
- Phishing: Credential harvesting signals
- Malware: Attachment-based signals

#### 3. NEW MALWARE VECTORS
**What to look for:**
- Extract file extensions from email attachments
- Count detections per file type
- Check against your blocked list

**From 68 signals, focus on:**
- Attachment-related signals
- File type detection signals
- Malware classification signals

**Extraction process:**
```python
# Identify file types from signals or email content
file_extensions = extract_extensions_from_signals()
malware_by_type = group_by_extension(malware_emails)

# Compare with blocked list
new_threats = []
for ext, count in malware_by_type:
    if ext not in blocked_extensions and count > 10:
        new_threats.append({
            "file_type": ext,
            "detections": count,
            "currently_blocked": False
        })
```

### Step 3: Transform to Required Format

```json
{
  "organization_name": "Your Company Name",
  "reporting_week": "Current Week Dates",
  
  "vendor_compromises": [
    {
      "domain": "sender-domain.com",
      "threats_this_week": 45,
      "threats_last_week": 3,
      "is_known_vendor": true
    }
  ],
  
  "department_targeting": [
    {
      "department": "Finance",
      "threat_type": "BEC/Impersonation",
      "count": 28,
      "percentage_of_total": 35,
      "financial_risk": "Calculate from email content"
    }
  ],
  
  "new_malware_vectors": [
    {
      "file_type": ".zip",
      "detections": 22,
      "currently_blocked": false
    }
  ]
}
```

## Signal Mapping Guide

### Signals that indicate VENDOR COMPROMISE:
- Sender reputation signals
- Domain age signals
- Authentication failure signals (SPF/DKIM/DMARC)
- Known vendor domain in threat list

### Signals that indicate DEPARTMENT TARGETING:
- Recipient analysis signals
- Social engineering signals
- Urgency/financial request signals
- VIP impersonation signals

### Signals that indicate NEW MALWARE:
- Attachment type signals
- Sandbox detection signals
- File hash/signature signals
- Zero-day detection signals

## Quick Extraction Checklist

**For each malicious email, extract:**
- [ ] Sender domain
- [ ] Receiver email/department
- [ ] Week sent (for comparison)
- [ ] Threat type (from signals)
- [ ] Attachment types (if any)
- [ ] Financial impact (from content)

**Aggregate data to find:**
- [ ] Domains with >300% increase
- [ ] Departments with >30% targeting
- [ ] File types with >10 detections

## Python Example for Data Extraction

```python
import pandas as pd
from datetime import datetime, timedelta

def extract_immediate_action_data(emails_df):
    # Filter malicious emails
    malicious = emails_df[emails_df['class'] == 'Malicious']
    
    # Define current and last week
    today = datetime.now()
    week_start = today - timedelta(days=7)
    last_week_start = week_start - timedelta(days=7)
    
    # Vendor compromises
    vendor_data = []
    domains = malicious.groupby(['sender_domain', 'week']).size()
    for domain in domains.index.get_level_values(0).unique():
        this_week = domains.get((domain, 'current'), 0)
        last_week = domains.get((domain, 'previous'), 0)
        if last_week > 0 and (this_week / last_week) > 3:
            vendor_data.append({
                "domain": domain,
                "threats_this_week": this_week,
                "threats_last_week": last_week,
                "is_known_vendor": check_vendor_list(domain)
            })
    
    # Department targeting
    dept_data = []
    total_malicious = len(malicious)
    for dept in ['Finance', 'HR', 'IT']:
        dept_emails = malicious[malicious['receiver'].str.contains(dept, case=False)]
        count = len(dept_emails)
        percentage = (count / total_malicious) * 100
        if percentage > 30:
            dept_data.append({
                "department": dept,
                "threat_type": identify_threat_type(dept_emails),
                "count": count,
                "percentage_of_total": percentage
            })
    
    # New malware vectors
    malware_data = []
    # Extract from attachment signals
    file_types = extract_file_types_from_signals(malicious)
    for file_type, count in file_types.items():
        if count > 10 and file_type not in blocked_extensions:
            malware_data.append({
                "file_type": file_type,
                "detections": count,
                "currently_blocked": False
            })
    
    return {
        "vendor_compromises": vendor_data,
        "department_targeting": dept_data,
        "new_malware_vectors": malware_data
    }
```

## Key Points for Your Data

1. **You have the raw data** - 68 signals contain all needed information
2. **Extract patterns** - Look for sender domains, receiver patterns, file types
3. **Calculate changes** - Compare this week vs last week
4. **Apply thresholds** - >300% for vendors, >30% for departments, >10 for files
5. **Generate JSON** - Format extracted data as shown in the guide

Once you extract this data, the prompt will generate professional IMMEDIATE ACTIONS recommendations automatically.