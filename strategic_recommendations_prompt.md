# STRATEGIC RECOMMENDATIONS - Complete Prompt Guide

## Final Comprehensive Prompt

```
Generate STRATEGIC RECOMMENDATIONS for medium-term security improvements (7-90 days) based on the organization's weekly (7-day) email security data analysis.

Analyze the provided 7-day period data for patterns, trends, and gaps, then create 2-3 strategic recommendations from these categories:

## RECOMMENDATION CATEGORIES:

### 1. AUTHENTICATION & TRUST
- Email authentication (DMARC, SPF, DKIM, BIMI)
- Certificate management
- Domain reputation monitoring
- Sender verification systems

### 2. INTEGRATION & ORCHESTRATION
- Security tool integration (SIEM, SOAR, XDR)
- API connections
- Workflow automation
- Incident response orchestration

### 3. DATA PROTECTION & PRIVACY
- Email encryption implementation
- Data Loss Prevention (DLP) for emails
- Sensitive data discovery
- Privacy compliance automation

### 4. THREAT INTELLIGENCE & ANALYTICS
- Industry-specific threat feeds
- Predictive analytics
- Behavioral analysis
- Dark web monitoring

### 5. SUPPLY CHAIN & VENDOR SECURITY
- Vendor risk assessment automation
- Partner domain monitoring
- Third-party email security
- Supply chain communication protocols

### 6. ADVANCED DETECTION CAPABILITIES
- AI/ML threat detection
- Natural Language Processing for BEC
- Image-based threat analysis
- Zero-day detection systems

### 7. BUSINESS CONTINUITY & RESILIENCE
- Email backup strategies
- Disaster recovery planning
- Redundancy systems
- Business email compromise insurance

### 8. REGULATORY & COMPLIANCE
- Industry-specific compliance (HIPAA, PCI, GDPR, CERT-In, DPDP Act)
- Audit trail enhancement
- Automated compliance reporting
- Legal hold capabilities

### 9. TRAINING & SECURITY CULTURE
- Role-based security training (Finance, HR, IT, Executives)
- Phishing simulation programs
- Security champions program
- Gamified awareness initiatives
- Micro-learning modules
- Culture transformation programs

### 10. EMERGING TECHNOLOGY PROTECTION
- Cloud email security
- Mobile device email protection
- IoT communication security
- Quantum-safe cryptography preparation

### 11. PROCESS OPTIMIZATION
- Incident response automation
- Security metrics dashboards
- ROI measurement frameworks
- Continuous improvement programs

### 12. SPECIALIZED PROTECTIONS
- Executive communication security
- Board-level reporting systems
- M&A due diligence protocols
- Crisis communication channels

## FORMAT FOR EACH RECOMMENDATION:

## 🟡 STRATEGIC RECOMMENDATIONS

### [Number]. [Strategic Initiative Title]
**Priority:** [Medium/Low] | **Timeline:** [X days]

**Current Status:** [Specific gap or opportunity identified from the weekly (7-day) data analysis]

**Recommendation:** [What to implement and business value]

**Steps:**
1. [Planning/Assessment phase with specific actions]
2. [Implementation/Configuration phase]
3. [Testing/Validation phase]
4. [Rollout/Optimization phase]

**Training Component:**
- [Role-specific training for affected teams]
- [Awareness sessions for general staff if needed]
- [Technical training for administrators/operators]
- [Ongoing reinforcement schedule (monthly/quarterly)]

**Impact:** [Measurable benefit - percentage improvement, cost savings, efficiency gain, or compliance achievement]

---

## SELECTION CRITERIA:
Choose recommendations based on:
- Biggest security gaps identified in the data
- Industry-specific threats and requirements
- Compliance/regulatory needs
- Available budget and resources
- Organization size and maturity
- Recent incidents or near-misses
- Upcoming business initiatives

## DATA FLEXIBILITY:
Work with whatever data is provided from the 7-day analysis period. If data is limited, focus recommendations on the gaps that ARE visible.
Common data points from weekly (7-day) analysis include:
- Current authentication status and failure rates over the week
- Existing security tools and their effectiveness metrics
- Threats/incidents detected in the past 7 days
- Compliance gaps identified during the week
- Department vulnerabilities based on weekly targeting patterns
- Training completion rates and engagement metrics
- Vendor/supply chain risks observed in 7-day period

Generate recommendations that are:
- Specific to the organization's context
- Achievable within the timeline
- Measurable in impact
- Complementary to any immediate actions
- Progressive (building security maturity)
```

## Priority Guidelines

### Medium Priority (7-30 days)
- Critical compliance gaps
- High-impact integrations
- Department-specific training for targeted teams
- Authentication improvements
- Quick-win automations

### Low Priority (30-90 days)
- Advanced capabilities (AI/ML)
- Culture transformation programs
- Long-term infrastructure changes
- Strategic initiatives
- Future-proofing measures

## Comprehensive Examples

### Example 1: Data Protection (DLP)
```
### 4. Implement Email Data Loss Prevention (DLP)
**Priority:** Medium | **Timeline:** 45 days

**Current Status:** No automated detection for sensitive data in emails (PAN, Aadhaar, financial data).

**Recommendation:** Deploy email DLP to prevent accidental data exposure and ensure DPDP Act compliance.

**Steps:**
1. Define sensitive data patterns (PAN, Aadhaar, bank accounts, API keys)
2. Configure DLP policies with warning/blocking rules
3. Test with security team, refine false positive rates
4. Roll out department by department with training

**Training Component:**
- Conduct workshops on handling sensitive data for all departments
- Train administrators on DLP policy management and incident response
- Create quick reference cards for identifying sensitive data types
- Monthly refresher emails with examples of what triggers DLP alerts

**Impact:** 90% reduction in accidental sensitive data exposure, full DPDP Act compliance for email communications.
```

### Example 2: Supply Chain Security
```
### 5. Establish Vendor Email Risk Monitoring
**Priority:** Medium | **Timeline:** 30 days

**Current Status:** No systematic monitoring of 47 critical vendor domains for compromise indicators.

**Recommendation:** Implement automated vendor domain monitoring with risk scoring and alerts.

**Steps:**
1. Create inventory of all vendor/partner email domains
2. Deploy continuous monitoring for authentication changes, threat patterns
3. Establish risk scoring system (authentication, volume anomalies, reputation)
4. Create automated alerts and vendor notification workflows

**Training Component:**
- Train procurement team on vendor domain verification procedures
- SOC team workshop on vendor risk indicators and response protocols
- All-staff awareness on recognizing fake vendor communications
- Quarterly tabletop exercises on vendor compromise scenarios

**Impact:** 75% faster detection of vendor account compromises, preventing supply chain attacks.
```

### Example 3: Advanced Analytics
```
### 6. Deploy Behavioral Analytics for BEC Detection
**Priority:** Low | **Timeline:** 60-90 days

**Current Status:** Rule-based detection missing 23% of sophisticated BEC attempts.

**Recommendation:** Implement ML-based behavioral analysis to detect anomalous communication patterns.

**Steps:**
1. Baseline normal communication patterns for executives and finance team
2. Deploy machine learning models for anomaly detection
3. Integrate with existing email security for enhanced scoring
4. Create feedback loop for continuous model improvement

**Training Component:**
- Executive team training on BEC tactics and behavioral changes to watch for
- IT/Security team technical training on ML model tuning and interpretation
- Finance team awareness on communication verification protocols
- Monthly updates on new BEC patterns detected by the system

**Impact:** 45% improvement in BEC detection rates, ₹2.4 Cr annual fraud prevention.
```

### Example 4: Business Continuity
```
### 7. Implement Email Disaster Recovery System
**Priority:** Medium | **Timeline:** 45 days

**Current Status:** No email backup system; potential 72-hour downtime in disaster scenario.

**Recommendation:** Deploy cloud-based email continuity solution for zero-downtime operations.

**Steps:**
1. Evaluate email continuity solutions compatible with current infrastructure
2. Configure automatic email journaling and backup
3. Test failover procedures with IT and key departments
4. Document and train on emergency access procedures

**Training Component:**
- IT team hands-on training on failover procedures and recovery processes
- Department heads training on emergency email access protocols
- All-staff awareness on disaster recovery expectations and alternate communication
- Quarterly disaster recovery drills with lessons learned sessions

**Impact:** Reduce email downtime from 72 hours to <5 minutes, ensure business continuity.
```

### Example 5: Role-Based Security Training
```
### 8. Deploy Targeted Finance Team Email Security Training
**Priority:** Medium | **Timeline:** 30 days

**Current Status:** Finance department targeted in 42% of BEC attacks; generic annual training only.

**Recommendation:** Implement role-specific, scenario-based training with monthly phishing simulations.

**Steps:**
1. Analyze actual BEC attempts targeting finance from past 90 days
2. Develop finance-specific training modules (invoice fraud, wire transfers, vendor changes)
3. Launch bi-weekly phishing simulations mimicking real attacks
4. Create "Finance Security Champion" role with monthly best practices sharing

**Training Component:**
- Finance-specific workshops on BEC tactics, invoice fraud, payment verification
- One-on-one coaching for high-risk roles (AP, Treasury, Controllers)
- Bi-weekly phishing simulations with immediate feedback and learning
- Monthly "Security Champion" meetings to share real incidents and best practices

**Impact:** 45% reduction in successful BEC attempts, ₹18.5L fraud prevention, 90% engagement rate.
```

### Example 6: Security Culture Transformation
```
### 9. Establish Organization-Wide Security Culture Program
**Priority:** Low | **Timeline:** 60-90 days

**Current Status:** Traditional compliance training with 65% completion; low security awareness engagement.

**Recommendation:** Transform security training into continuous culture program with gamification and rewards.

**Steps:**
1. Launch "Security Hero" recognition program with monthly departmental awards
2. Deploy 3-minute weekly micro-learning modules via Teams/Slack
3. Create real-time security scorecard dashboard visible to all employees
4. Implement "Catch of the Month" showcase for reported sophisticated attacks

**Training Component:**
- Leadership workshop on championing security culture from the top
- Department-specific micro-learning paths based on risk profiles
- Gamified security challenges with team competitions and rewards
- Continuous reinforcement through storytelling and real incident sharing

**Impact:** 90%+ voluntary engagement, 60% increase in threat reporting, security becomes competitive advantage.
```

### Example 7: Compliance Automation
```
### 10. Automate CERT-In Compliance Reporting
**Priority:** Medium | **Timeline:** 30 days

**Current Status:** Manual incident reporting taking 4-6 hours; risk of missing 6-hour deadline.

**Recommendation:** Implement automated incident detection and reporting workflow for CERT-In compliance.

**Steps:**
1. Map email security incidents to CERT-In reporting categories
2. Configure automated incident classification and severity scoring
3. Build reporting templates with auto-population from security tools
4. Test with tabletop exercises and refine workflows

**Training Component:**
- SOC team training on CERT-In requirements and automated workflow operation
- Incident response team workshop on severity classification and escalation
- Management briefing on compliance obligations and reporting timelines
- Monthly compliance drills to maintain readiness and identify gaps

**Impact:** Reduce reporting time to <30 minutes, ensure 100% compliance with 6-hour mandate.
```

### Example 8: SIEM Integration
```
### 11. Integrate Email Security with Splunk SIEM
**Priority:** Low | **Timeline:** 60 days

**Current Status:** Splunk SIEM available but not connected; missing email threat correlation.

**Recommendation:** Integrate email security platform with Splunk for unified threat detection and response.

**Steps:**
1. Configure API connections between email security and Splunk
2. Create correlation rules linking email threats to endpoint/network events
3. Build unified dashboards showing full attack chain visibility
4. Develop automated playbooks for common email-initiated attacks

**Training Component:**
- SOC analysts advanced training on email-to-endpoint attack correlation
- Security engineers workshop on Splunk query optimization for email threats
- Incident response team training on using unified dashboards for investigations
- Quarterly threat hunting exercises focusing on email-initiated attack chains

**Impact:** 50% faster incident response, complete attack visibility, enhanced threat hunting capabilities.
```

## Quality Checklist

- [ ] Recommendation addresses specific gap identified in data
- [ ] Timeline is realistic (7-90 days) and achievable
- [ ] Steps are detailed, actionable, and sequenced properly
- [ ] Impact is measurable with specific metrics or percentages
- [ ] Aligns with organization's industry, size, and context
- [ ] Considers available resources, budget, and constraints
- [ ] Complements immediate actions without overlap
- [ ] Provides long-term security value and maturity growth
- [ ] Includes relevant tools, vendors, or platforms where applicable

## Using This Prompt

1. **Provide any available data** about the organization's security posture
2. **The prompt adapts** to whatever data you provide
3. **Recommendations generated** will focus on the biggest gaps found
4. **No need for complete data** - work with what you have

Example minimal input:
```json
{
  "organization_name": "ABC Corp",
  "current_issues": {
    "no_dmarc": true,
    "finance_targeted": "45% of attacks",
    "no_vendor_monitoring": true
  }
}
```

This will generate recommendations for DMARC setup, finance training, and vendor monitoring.

## Supported Industries

The prompt automatically adapts recommendations for:
- Financial Services (fraud prevention, regulatory compliance)
- Healthcare (PHI protection, HIPAA compliance)
- Manufacturing (supply chain security, IP protection)
- Retail (seasonal threats, PCI compliance)
- Technology (code security, competitive threats)
- Government (citizen data, classified handling)
- Education (research protection, diverse systems)
- Any other industry based on context provided