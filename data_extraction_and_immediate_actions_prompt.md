# Data Extraction & IMMEDIATE ACTIONS Generation Prompt

## Complete Prompt for Your Email Security System

```
You have access to email security data with the following structure:
- Total emails analyzed
- Email classifications (Safe/Warning/Spam/Malicious)
- 68 signals per email indicating various threat indicators
- Email metadata (sender, receiver, subject, text)
- Action status (done/pending)

Please perform the following analysis and generate IMMEDIATE ACTION recommendations:

STEP 1: DATA EXTRACTION
From the email data, extract:

1. VENDOR COMPROMISE ANALYSIS
- List all sender domains from malicious emails
- Count malicious emails per domain for current week
- Count malicious emails per domain for previous week
- Calculate percentage increase
- Identify if sender is a known vendor/partner (based on domain reputation or previous legitimate communications)
- Flag any domain with >300% increase in malicious emails

2. DEPARTMENT TARGETING ANALYSIS
- Group malicious emails by receiver email patterns:
  * Finance/Accounts: emails containing finance@, accounts@, ap@, ar@, cfo@
  * HR: emails containing hr@, human.resources@, recruitment@
  * IT: emails containing it@, tech@, support@, helpdesk@
  * Management: emails containing ceo@, coo@, director@, manager@
- Count malicious emails per department
- Calculate percentage of total malicious emails per department
- Identify primary threat type per department based on signals:
  * BEC/CEO Fraud: urgency signals + financial request signals
  * Phishing: credential harvesting signals + fake login pages
  * Malware: attachment signals + executable files
- Extract financial risk if mentioned in email content

3. NEW MALWARE VECTOR ANALYSIS
From the 68 signals, identify:
- File attachment types detected in malicious emails
- Count of each file type
- Check against current blocked extensions list
- Flag any unblocked file type with >10 detections

STEP 2: GENERATE IMMEDIATE ACTIONS
Based on the extracted data, generate 2-3 IMMEDIATE ACTION recommendations following this format:

## 🔴 IMMEDIATE ACTIONS REQUIRED

### [Number]. [Action Title]
**Priority:** [Critical/High/Medium] | **Owner:** [Role] | **Deadline:** Within [X] hours/days

**Issue:** [Specific statement with numbers and percentages]

**Recommended Actions:**
- [Immediate containment action]
- [Investigation/communication action]  
- [Preventive measure]

**Impact if Ignored:** [One sentence describing consequence]

---

Priority Guidelines:
- Critical (24 hours): Vendor domain with >300% malicious email increase
- High (7 days): Department receiving >40% of specific attack type
- Medium (14 days): New file type with >20 malware detections

Focus on actionable, specific recommendations that can be immediately implemented.
```

## Simplified Version for Direct Use

```
Analyze the email security data and create IMMEDIATE ACTION recommendations.

From the malicious emails, identify:
1. Sender domains with dramatic increases (>300%) week-over-week
2. Departments receiving concentrated attacks (>40% of a threat type)
3. New malware file types not currently blocked (>10 detections)

For each finding, generate an action item with:
- Clear title describing the threat
- Priority level and deadline
- Specific issue with numbers
- Three concrete action steps
- Impact if not addressed

Format as professional security recommendations for IT management.
```

## Example Input Structure for the Prompt

```
Email Security Summary:
- Total emails: 15,234
- Malicious emails: 247
- Top malicious sender: globaltech-suppliers.com (89 emails this week, 2 last week)
- Finance department: Received 58 BEC attempts (42% of all BEC)
- New threat: 31 malware samples via .iso files (not blocked)
- Currently blocked: .exe, .scr, .bat files
```

## Expected Output Format

The prompt will generate output exactly like:

```
## 🔴 IMMEDIATE ACTIONS REQUIRED

### 1. Investigate Compromised Vendor Account
**Priority:** Critical | **Owner:** IT Manager | **Deadline:** Within 24 hours

**Issue:** Domain `globaltech-suppliers.com` sent 89 malicious emails this week (up from 2 last week).

**Recommended Actions:**
- Contact vendor IT team to verify account security status
- Temporarily block domain until confirmation of remediation
- Review past 30 days of emails from this sender for missed threats

**Impact if Ignored:** Continued credential phishing exposure for entire organization.
```

## Usage Instructions

1. **Prepare your data**: Run analysis on your email data to get counts and classifications
2. **Apply the prompt**: Use either the detailed or simplified version
3. **Provide the data**: Include actual numbers from your analysis
4. **Review output**: Ensure recommendations are specific to your organization
5. **Implement actions**: Follow the prioritized recommendations

This prompt will work with your current data structure and generate professional, actionable IMMEDIATE ACTIONS for your weekly security reports.