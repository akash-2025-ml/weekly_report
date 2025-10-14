# IMMEDIATE ACTIONS Generation Guide

## Overview
This document provides a simple, professional framework for generating IMMEDIATE ACTION recommendations from weekly email security reports. Focus is on critical threats requiring response within 24-48 hours.

---

## 🔴 IMMEDIATE ACTIONS REQUIRED - Framework

Immediate Actions are critical security responses needed within 24-48 hours to prevent ongoing threats. They focus on three key areas:

1. **Compromised Vendor Accounts** - Known partners sending malicious emails
2. **Targeted Department Attacks** - Specific teams under concentrated assault
3. **New Malware Vectors** - Unblocked file types actively delivering malware

---

## 🎯 IMMEDIATE ACTIONS PROMPT

### Simple Professional Prompt Template

```
Based on the weekly email security data, generate IMMEDIATE ACTION recommendations for critical threats that require response within 24-48 hours.

Focus on these three threat categories:
1. Vendor/Partner Account Compromises (domain threat spikes >300%)
2. Targeted Department Attacks (departments receiving >30% of specific threat types)
3. New Malware Vectors (unblocked file types with >10 detections)

Format each action item as follows:

### [Number]. [Clear Action Title]
**Priority:** Critical | **Owner:** [Role] | **Deadline:** Within [X] hours

**Issue:** [One sentence with specific numbers and percentage change]

**Recommended Actions:**
- [Action 1: Immediate containment step]
- [Action 2: Communication/verification step]
- [Action 3: Follow-up monitoring step]

**Impact if Ignored:** [One sentence describing consequence]

Provide 2-3 immediate actions based on the data provided.
```

---

## 📊 MINIMUM REQUIRED DATA FOR IMMEDIATE ACTIONS

### Essential Data Structure (Simplified)

```json
{
  "organization_name": "TechVision Solutions Pvt Ltd",
  "reporting_week": "March 10-16, 2025",
  
  "vendor_compromises": [
    {
      "domain": "globaltech-suppliers.com",
      "threats_this_week": 89,
      "threats_last_week": 2,
      "is_known_vendor": true
    }
  ],
  
  "department_targeting": [
    {
      "department": "Finance",
      "threat_type": "BEC/Impersonation",
      "count": 58,
      "percentage_of_total": 42,
      "financial_risk": "₹18.5 Lakhs"
    }
  ],
  
  "new_malware_vectors": [
    {
      "file_type": ".iso",
      "detections": 15,
      "currently_blocked": false
    },
    {
      "file_type": ".img",
      "detections": 10,
      "currently_blocked": false
    },
    {
      "file_type": ".vhd",
      "detections": 6,
      "currently_blocked": false
    }
  ],
  
  "blocked_file_types": ["exe", "scr", "bat"]
}
```

### Data Collection Checklist

✅ **For Vendor Compromises:**
- Domain name
- Email count this week vs last week
- Is it a known vendor/partner?

✅ **For Department Targeting:**
- Department name
- Type of attack (BEC, Phishing, etc.)
- Number of attacks
- Percentage of total attacks
- Financial impact (if applicable)

✅ **For New Malware Vectors:**
- File extension
- Number of detections
- Currently blocked or not?

---

## 🎯 IMMEDIATE ACTIONS FORMATTING

### Priority Classification for Immediate Actions

| Trigger Condition | Priority | Deadline | Owner |
|-------------------|----------|----------|--------|
| Vendor domain spike >300% | Critical | 24 hours | IT Manager |
| Department targeted >40% | High | 7 days | HR + IT Manager |
| New malware vector >20 detections | Medium | 14 days | IT Manager |

### Standard Action Format

```
### [Number]. [Verb + Specific Threat]
**Priority:** [Critical/High/Medium] | **Owner:** [Role] | **Deadline:** Within [X] hours/days

**Issue:** [Domain/Department] [showed/received] [number] [threats], up [X%] from [previous number].

**Recommended Actions:**
- [Immediate containment action]
- [Investigation/communication action]
- [Long-term prevention action]

**Impact if Ignored:** [Consequence in one sentence].
```

---

## 📋 Step-by-Step Process

### Step 1: Collect Data
Gather these three data points from weekly report:
- Vendor domains with unusual activity
- Departments with high threat concentration
- File types detected but not blocked

### Step 2: Apply Triggers
Check if data meets these thresholds:
- Vendor spike >300%? → Critical (24 hrs)
- Department >40% targeted? → High (7 days)
- New file type >20 detections? → Medium (14 days)

### Step 3: Generate Actions
Use the prompt template with your data to create recommendations

---

## 💡 REAL-WORLD EXAMPLES

### Example 1: Using the Prompt with Data

**Input Data:**
```json
{
  "organization_name": "ABC Corp Ltd",
  "vendor_compromises": [
    {
      "domain": "trusted-supplier.com",
      "threats_this_week": 156,
      "threats_last_week": 3,
      "is_known_vendor": true
    }
  ],
  "department_targeting": [
    {
      "department": "Accounts",
      "threat_type": "Invoice Fraud",
      "count": 89,
      "percentage_of_total": 67,
      "financial_risk": "₹45 Lakhs"
    }
  ],
  "new_malware_vectors": [
    {
      "file_type": ".rar",
      "detections": 34,
      "currently_blocked": false
    }
  ]
}
```

**Generated Output:**

### 1. Investigate Compromised Vendor Account
**Priority:** Critical | **Owner:** IT Manager | **Deadline:** Within 24 hours

**Issue:** Domain `trusted-supplier.com` sent 156 malicious emails this week (up from 3 last week).

**Recommended Actions:**
- Contact vendor IT team to verify account security status
- Temporarily block domain until confirmation of remediation  
- Review past 30 days of emails from this sender for missed threats

**Impact if Ignored:** Continued credential phishing exposure for entire organization.

---

### 2. Deploy Targeted Invoice Fraud Training for Accounts Team
**Priority:** High | **Owner:** HR + IT Manager | **Deadline:** Within 7 days

**Issue:** Accounts team received 67% of all invoice fraud attempts (89 total emails).

**Recommended Actions:**
- Schedule 30-minute invoice fraud awareness session for accounts department
- Share real examples from recent attacks
- Implement dual verification for invoice changes >₹10 Lakhs

**Expected Outcome:** 40% reduction in user susceptibility based on industry training data.

---

### 3. Block High-Risk Archive Files
**Priority:** Medium | **Owner:** IT Manager | **Deadline:** Within 14 days

**Issue:** 34 malware samples detected via .rar archive files.

**Recommended Actions:**
- Update email filtering policy to block .rar attachments
- Communicate policy change to users with legitimate use cases
- Monitor for business process disruption and adjust whitelist if needed

**Expected Outcome:** Eliminate 85% of archive-based malware (based on detection data).

---

## 🚀 Implementation Tips

1. **Data-Driven Recommendations:** Always base recommendations on specific metrics from the weekly data
   - Bad: "Improve email security training"
   - Good: "Deploy BEC training for Finance team - received 42% of impersonation attempts"

2. **Actionability:** Make steps so specific that someone can execute them immediately
   - Bad: "Review vendor security"
   - Good: "Contact globaltech-suppliers.com IT team via phone +91-XXX to verify account status"

3. **Impact Quantification:** Always include measurable expected outcomes
   - Bad: "This will improve security"
   - Good: "Expected to reduce attachment-based malware by 82% based on threat analysis"

4. **Urgency Indicators:** Use specific threat growth rates to justify priority
   - Include percentage increases (e.g., "340% spike in URL redirects")
   - Reference financial impact ("₹18.5 Lakhs in prevented wire fraud")

5. **Progressive Actions:** Structure recommendations to build on each other
   - Immediate: Block the threat
   - Strategic: Fix the vulnerability
   - Long-term: Prevent recurrence

6. **Incident References:** Link recommendations to specific incidents in the report
   - "As seen in Incident #1 (CEO impersonation targeting Suresh Patel)..."

7. **Cost-Benefit Analysis:** Include ROI or cost avoidance figures
   - "₹8.5 Lakhs average ransomware incident cost" 
   - "36.2 IT hours saved through automation"

---

## 🔍 IDENTIFYING IMMEDIATE ACTION TRIGGERS

### Quick Scanning Guide

When reviewing weekly reports, look for these red flags:

**🚨 Critical (24-hour response):**
- Any domain with >300% increase in threats
- Known vendor/partner domains in threat list
- Financial impact >₹10 Lakhs prevented

**⚠️ High Priority (7-day response):**
- Department receiving >30% of specific attack type
- Repeated targeting of same department
- User-reported successful phishing

**📢 Medium Priority (14-day response):**
- New file types with >10 malware detections
- Emerging attack patterns
- Policy gaps identified

### Data Extraction Template

```
Vendor Compromises:
☐ Domain: _________ This Week: ___ Last Week: ___ Increase: ___%

Department Targeting:
☐ Department: _________ Attack Type: _________ Count: ___ Percentage: ___%

New Malware Vectors:
☐ File Type: _________ Detections: ___ Currently Blocked: Yes/No
```

---

## ✅ Quality Checklist for Immediate Actions

### Each recommendation must have:
- [ ] Specific threat numbers (not vague descriptions)
- [ ] Clear ownership (IT Manager, HR, etc.)
- [ ] Exact deadline (Within 24 hours, not "ASAP")
- [ ] Three concrete action steps
- [ ] One-sentence impact statement

### Common Mistakes to Avoid:
- ❌ "Review security" → ✅ "Block domain xyz.com"
- ❌ "Improve training" → ✅ "Deploy BEC training for Finance by March 20"
- ❌ "Monitor threats" → ✅ "Audit past 30 days of vendor emails"

### Expected Outcomes:
- **Vendor Investigation:** Stop ongoing attack within 24 hours
- **Department Training:** 40% reduction in clicks within 30 days  
- **File Blocking:** 80%+ reduction in malware delivery immediately

---

## 📨 Complete Working Example

### Weekly Report Extract:
```
Vendor Alert: partner-tech.in sent 234 malicious emails (up from 4 last week)
Department Risk: HR received 76 phishing emails (55% of all phishing)
New Threat: 28 malware samples via .7z files (not currently blocked)
```

### Applied Data:
```json
{
  "organization_name": "Example Corp",
  "vendor_compromises": [{
    "domain": "partner-tech.in",
    "threats_this_week": 234,
    "threats_last_week": 4
  }],
  "department_targeting": [{
    "department": "HR",
    "threat_type": "Phishing",
    "count": 76,
    "percentage_of_total": 55
  }],
  "new_malware_vectors": [{
    "file_type": ".7z",
    "detections": 28,
    "currently_blocked": false
  }]
}
```

### Generated Output:

## 🔴 IMMEDIATE ACTIONS REQUIRED

### 1. Investigate Compromised Vendor Account
**Priority:** Critical | **Owner:** IT Manager | **Deadline:** Within 24 hours

**Issue:** Domain `partner-tech.in` sent 234 malicious emails this week (up from 4 last week).

**Recommended Actions:**
- Contact vendor IT team to verify account security status
- Temporarily block domain until confirmation of remediation
- Review past 30 days of emails from this sender for missed threats

**Impact if Ignored:** Continued credential phishing exposure for entire organization.

---

### 2. Deploy Targeted Phishing Training for HR Team  
**Priority:** High | **Owner:** HR + IT Manager | **Deadline:** Within 7 days

**Issue:** HR team received 55% of all phishing attempts (76 total emails).

**Recommended Actions:**
- Schedule 30-minute phishing awareness session for HR department
- Share real examples from this week's attacks
- Implement email verification process for sensitive HR data requests

**Expected Outcome:** 40% reduction in user susceptibility based on industry training data.

---

### 3. Block High-Risk Compression Files
**Priority:** Medium | **Owner:** IT Manager | **Deadline:** Within 14 days

**Issue:** 28 malware samples detected via .7z compressed files.

**Recommended Actions:**
- Update email filtering policy to block .7z attachments
- Communicate policy change to users with legitimate use cases
- Monitor for business process disruption and adjust whitelist if needed

**Expected Outcome:** Eliminate 75% of compression-based malware (based on file type analysis).

---

## 📌 Quick Reference Checklist

### Before Generating Recommendations
- [ ] Review threat volume trends and week-over-week changes
- [ ] Identify domains with suspicious activity spikes (>300% increase)
- [ ] Check department-specific targeting patterns
- [ ] Analyze new attack vectors and file types
- [ ] Review current security configurations and gaps
- [ ] Note available but unused security tools

### When Writing Each Recommendation
- [ ] Use specific numbers from the weekly data
- [ ] Assign clear ownership to a specific role
- [ ] Set concrete deadlines (hours for critical, days for strategic)
- [ ] Include 3 actionable steps that can be executed immediately
- [ ] Quantify the expected outcome or impact
- [ ] Reference specific incidents or examples from the report

### Quality Checks
- [ ] Is the recommendation based on actual data, not assumptions?
- [ ] Can someone execute this without asking clarifying questions?
- [ ] Is the priority justified by the threat severity or growth rate?
- [ ] Does the expected outcome include measurable benefits?
- [ ] Are the steps specific enough to be auditable?

---

## 📧 Support

For questions about generating recommendations:
- Review the weekly report sample for context
- Use the complete data input template for testing
- Ensure all critical data points are extracted
- Follow the priority matrix for proper categorization