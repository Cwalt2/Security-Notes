
# Week 1 Day 5

## Social Engineering

- Social Engineering Tactics
  - Impersonation
  - Urgency
  - Misinformation/disinformation

### Phishing

#### Social Engineering with a touch of spoofing

- Often delivered by email, text, etc
- Very remarkable when well done
- Indicators
  - Odd URL not matching original site
- can be very convincing using spoofing (emails or phone numbers) or copying a website style/theme
- Typosquatting
  - URL hijacking
  - Misdirection
  - Looks like the same website but spelled wrong
- Pretexting
  - Lying to get information
  - Attacker is a character in a situation they create
  - Calling Visa, Bill Collector, etc. to extract information
- Vishing
  - Voice Phishing
  - Caller ID spoofing is common
  - Fake security checks or bank updates
- Smishing
  - SMS Phishing
  - Text Message Phishing
  - Spoofing numbers also occurs here
  - Forward links or asks for person information
- Variation
  - Variations of these attacks are common
  - Fake check scam, phone verification code scam, Boss/CEO scam, Advance-fee scam
  - examples and summaries at [r/Scams]([reddit.com](https://www.reddit.com/r/Scams/wiki/index/)) on Reddit
- Business Email Compromise
  - Vector
    - Business Email
  - Attack surface
    - Partners and clients of the employee who gets targeted
- Watering Hole
  - Well-known website that has been compromised
- Brand Impersonation
  - Using Email or social media creates a fake brand with reviews
  - fake trust in order to get information out of victims
  - fake sponsors

## Security Controls

### Solution that mitigates threats

- ex. Malware scanner mitigates malware infections
- implemented differently based on platform/vendor/user
  - Network infrastructure devices (switches, routers, firewall)

- Security Control Categories
- Managerial/administrative
  - What should be done?
  - Employee background checks
- Operations
  - How often must we do it?
  - Periodic review of security policies
- Technical
  - How exactly will we do it?
  - Firewall rule Configuration
- Physical
  - Access control vestibule (mantrap)
  - Detective
    - Log analysis
  - Corrective
    - Patching known vulnerabilities
  - Deterrent
    - Device logon warning banners
  - Compensating
    - Network isolation for Internet of Things (IoT) devices
- Security Control Documents
  - Cloud Security Control Documents
    - Cloud Security Alliance (CSA)
      - Cloud Controls Matrix (CCM)
  - Payment Card Industry Data Security Standard (PCI DSS)
    - Security controls must be in place to be compliant
- Risk Example
  - Risk
    - Theft of online banking credentials
  - Attack Vector
    - Spoofed email message with a link to spoofed website tricking an end user
  - Mitigation through security controls
    - User security awareness
    - antivirus software
    - spam filters

## Risk

### Risk Assessment

> "Prioritization of threats against assets and determining what to do about it."

- Applicable to:
  - Entire organization
  - A single project or department
- Targets:
  - Servers
  - Legacy Systems
  - Intellectual Property (IP)
  - Software licensing
- Risk Assessment Process
  - Risk Awareness
    - Cybersecurity intelligence sources
  - Evaluate Security Controls
    - Inherent (current) residual risk
  - Implement Security Controls
  - Periodic Review
    - present tools can become obsolete fast
- Risk Types
  - Environmental
    - Flood, hurricane
  - Person-made
    - Riots, terrorism, sabotage
  - Internal
    - Malicious insider, malware infections
  - External
    - Distributed Denial of Service (DDoS)
- Risk Treatments
  - Mitigation/Reduction
    - Security controls are proactively put in place before understanding the risk
  - Transference/Sharing
    - Some risk is transferred to a third party in exchange for payment
    - example: cybersecurity insurance
  - Avoidance
    - Avoid an activity because the risk outweighs potential gains
  - Acceptance
    - The current level of risk is acceptable
    - The risk falls within the organizations risk appetite

### Quantitative Risk Assessment

#### Based on numeric values

- Asset value (AV)
- Exposure Factor (EF)
  - Percentage of asset value loss when negative incident occurs
- Single Loss Expectancy (SLE)
  - How much loss is experienced during one negative incident?
  - Multiply asset value (AV) by the exposure factor (EF)
  - **For exam need to calculate and determine numbers of this**
    - Asset Value (AV) = $24,000
    - Exposure Factor (EF) = 12.5%
    - $24,000 (AV) X 0.125 (EF) = $3,000 (SLE)
- Full example
  - Calculate Single Loss Expectancy
    - SLE = Asset Value (AV) x Exposure Factor (EF)
    - Risk of Downtime = 3 hours / 24 hours in a day = 12.5% exposure factor (EF)
    - SLE = Asset Value (AV) x Exposure Factor (EF)
- Annualized Rate of Occurrence (ARO)
  - Expected number of yearly occurrences
  - Example: 2-3 times per year
- Annualized Loss Expectancy (ALE)
  - Total yearly cost of bad things happening
  - ALE = SLE X ARO

> **Need to know how to calculate SLE and ALE**

- ALE = Single Loss Expectancy (SLE) x Annualized Rate of Occurrence (ARO)
  - $6,000 = SLE $3,000 x ARO 2 = ALE
  - Conclusion: spending less than $6,000 annually to protect our e-commerce site is worthwhile

### Qualitative Risk Assessment

- Based on subjective opinions regarding:
  - Threat likelihood
  - Impact of realized threat
- Threats are given a severity rating

#### Risk Register

- Organization should have one or more
- Centralized list of risks, severities, responsibilities, and mitigations
- Generally considered qualitative
  - Example: severity or impact ratings
  - Occasionally includes hard numbers (%,$)
- Risk Heat Map
  - Take risk severity levels and map visually by color
- Risk Matrix
  - Table of risk details
  - Similar to heat map but without colors

## Vulnerabilities

### Vulnerability Scans

- compare to baseline scans
- Passive/non-invasive compared to penetration tests
- Should be run periodically
  - Manual
  - Automatic (scheduled)
- Scan Targets
  - Network
  - Host
  - Application
- Scans
  - Credentialed scan
    - Tester provides host/device credentials
    - testing is more thorough
  - Non-credentialed
    - Mimic someone who doesn't have access
  - Keep vulnerabilities database up-to-date
    - Reduces false negatives/positives

> **Scenario based questions on exam**

## Penetration Testing

- AKA "pen testing"
- Attempt to exploit vulnerabilities
- Invasive/active compared to vulnerability assessments
- Pen tester must sign non-disclosure agreement (NDA)
- Normally triggers IDS/IPS alerts

### Types

- Known (white box)
- Unknown (black box)
- Partially-known (gray box)
- Bug bounty
  - Offered by vendors for discovery of zero-day attacks

### Pen Testing Exercises

- Red Team
  - Attackers
- Blue Team
  - Defenders
- White Team
  - Manages red and blue team engagements
- Purple Team
  - Red and blue team feedback and knowledge transfer
- The penetration testing process
  1. Rules of engagement
  2. Discovery/enumeration
  3. Vulnerability identification and exploitation
  4. Privilege escalation, backdoor pivoting, lateral movement
  5. Cleanup
  6. Report findings
