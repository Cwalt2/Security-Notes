# Chapter 13

## Introduction to Business Security

### Business Security Key Terms

- Vendor/suppliers
  - Provide key materials or services
- Partners
  - Organzations with mutual business objectives or collaboration
- Consultants
  - External experts guiding business strategy or processes
- Cloud Service Providers (CSPs)
  - Companies offering cloud-based platforms, infrastructure, software
- Subcontractors
  - Entities hired to fulfill a specific portion of a project or service

### Due Diligence

- Rigorous research and analysis of a third-party
- Ensures they uphold security standards

### Conflict of Interest

- When personal interests compromise business decisions

### Questionnaires

- Provide systematic way to gather analyze, and validate a third-party
- Standardized Information Gathering (SIG) Questionnaire
  - [sharedassessments.org/about-sig/](sharedassessments.org/about-sig/)

## Business Impact Analysis

- (BIA)
- Prioritize mission-critical processes
  - Payment processing systems
  - Custome/patient records
- Assess risk
  - Identify sensitive data
  - Identify single points of failure
  - Identify security controls and compliance
- Financial
  - Fines
  - Loss of contracts
- Reputation
- Data Loss
  - Breach notification
  - Escalation requirements
  - Exfiltration

### Failed Component Impact

- Mean time between failures (MTBF)
  - Average time between repairable component failures
  - Software patching
- Mean time to failure (MTTF)
  - Average time between NON-repairable component failures
  - Hard disks, switches, routers
- Mean time to repair (MTTR)
  - Time required to repair a failed component

### Locating Critical Resources

- Data discovery and classification
  - Where is our sensitive data?
  - Privacy threshold assessment (PTA)
    - First step before implementing solutions related to sensitive data
- Impact on sensitive data
  - Privacy impact assessment (PIA)
  - Regulatory compliance
- Recovery point objective (RPO)
  - Maximmum tolerable amount of data loss
  - Directly related to backup frequency
- Recovery time objective (RTO)
  - Maximum tolerable amount of downtime
  - Return system and data to usable state

## Data Types and Roles

### Data Classification

- Government/military classification
  - Top secret
  - Secret
  - Confidential
  - Restricted

### Standard Classifications

- Sensitive information
  - Personally identifiable information (PII)
  - Protected health information (PHI)
- Other classifications
  - Proprietary
  - Public/private
  - Critical
  - Financial

### Data Privacy Standards

- Ensure data privacy and breach notification
- Levy fines
- Protect intellectual property (IP)
- Example
  - Health Insurance Portability and Accountability Act (HIPAA)
- Payment Card Industry Data Security Standard (PCI DSS)
  - Cardholder information
- General Data Protection Regulation (GDPR)
  - Protects EU citizens' data regardless of location

### Data Classification Tools

- Any method applying metadata
- Example:
  - Cloud resource tagging

### Data Roles and Responsibilities

- Owner
  - Legal data owner
  - Set policies on how data will be managed
- Controller
  - Ensure data complies with applicable regulations
- Processor
  - Handles data in accordance with privacy guidelines
- Custodian/steward
  - Responsible for managing data (permissions, backup) in alignment with data owner policies
- Data Privacy Officer (DPO)
  - Ensures data privacy regulation compliance such as with GDPR

## Personnel Risk and Policies

### Personnel Management Policies

- Standard operating procedure (SOP)
  - Example: proper steps for sending sensitive data via email
- Mandatory vacation, job rotation
  - Detection of irregularities
- Separation of duties (multi-person control)
  - Reduce likelihood of internal fraud
  - Does not prevent collusion
- Social Media analysis
- Web search
- Background check
  - Criminal record
  - Unpaid fines
  - Credit check
  - Interviews with friends, family, colleagues

### User Onboarding

- Non-disclosure agreement (NDA)
  - Proprietary secrets, PII/PHI
- Security policy awareness
  - User sign-off
- User account and resource access
- Issue security badge, smart card

### User Habits

- Clean desk policies
- Physical and digital document shredding
  - Mitigates dumpster diving, data recovery
- Personally-owned devices
  - Mobile device management (MDM)
  - Bring your own device (BYOD)

### User Training

- Ongoing, role-based
- Computer-based training (CBT)
- Gamification
  - Capture the flag contests
- Phishing campaigns/simulations
  - Lunch and learn
  - Can be part of a penetration test

### User Offboarding

- Termination letter
- Exit interview
- Return of equipment
- Knowledge transfer
- Account disablement vs. deletion

## Attestation

### System-Based Attestation

- Validates a system or component to ensure its authenticity and integrity against a security standard
- Example: TPM chip

### Identity-Based Attestation

- Validation based on a set of identity attributes
- Example: validating credentials using MFA

### Legal-Based Attestation

- Formal agreement under the law to confirm accuracy of facts, events, etc.
- Example: Employee signs an acceptable use policy and promises to use the IT resources appropriately

## Internal Audits and Assessments

### Internal Compliance

- Ensuring the organization's practices align with internal policies and procedures, and external laws and regulations
- Compliance Department
  - Policy Adherence
  - Legal Compliance
  - Risk Mitigation
- Audit Committee
  - Oversee cybersecurity strategy
  - Review risk management processes, compliance, standards, regulations, and findings from audits
- Self-assessments
  - Individual or team evaluations to assess compliance
  - Identify areas of improvement
  - Foster a culture of growth
  - More efficient

## External Audits and Assessments

### Regulatory Audit

- Performed by an external entity
- Ensures compliance with cybersecurity laws and regulations within a specific industry
- Can be used for:
  - Legal compliance
  - Risk mitigation
  - Stakeholder assurance

### Examination

- Detailed review of a company's compliance in specific processes, systems, or controls
- Example:
  - Review of the company's incident response process
  - Tailored recommendations enable targeted improvements

### Assessments

- Identify weaknesses and give solutions against potential threats
- Offer a comprehensive view of the organization's cybersecurity status
- Identify gaps between current practices and desired standards

### Penetration Test

- Simulated cyber-attack on an IT infrastructure to identify vulnerabilities
- Conducted by ethical hackers
- Pen testing focuses on specific cybersecurity weaknesses, while audits provide a comprehensive assessment of the security posture

## Third-Party Risk Management

- Measurement systems analysis (MSA)
  - Quality Assurance

### Supply Chain Security Risks

- Hardware and software vendors
  - End-of-service life (EOL, EOSL) means no more patches or support
- Cloud service providers security compliance
- Contractos
  - Data privacy notices
- Company mergers and system linking
- Software developers using third-party components

### Third-Party Risk Management

- Data Loss Prevention (DLP) systems
  - Reduce intentional/unintentional sensitive data exfiltration

## Agreement Types

- Interconnection security agreement (ISA)
  - Legal review, regulatory compliance
  - Linking companies, partners, agencies
  - Vulnerability scan results
  - Mandatory training/certification
  - Input from IT security professionals
- Service Level Agreement (SLA)
  - Contractual document stating level of service
  - Guarantee service uptime
  - Consequences for not meeting requirements
- Memorandum of understanding (MOU)
  - Broad terms of agreement between parties
- Memorandum of agreement (MOA)
  - Detailed terms between parties
- Business partnership agreement (BPA)
  - Legal document
  - Responsibilities, investment, decision-making
- Non-disclosure agreement (NDA)
  - Prevent sensitive data disclosure to third parties

## Change Management

### Change Management Considerations

- Approval of ownership
- Stakeholders
- Impact analysis
- Test results
- Backout plans
- Maintenance windows
- Standard operating procedures

### Approval of Ownership

- Formal authorization confirming a proposed change aligns with security needs
- Identifies who is responsible for the change

### Stakeholders

- Have an invested interest in the change
- Ensures different perspectives are considered, especially for overall organizational goals

### Impact Analysis

- Assess how the change will affect various parts of the organization
- Evaluate risks and benefits

### Test Results

- Information gathered from testing change in a controlled environment
- Reveals how the change behaves and the impact on security

### Backout plans

- Strategies for reversing a change if something goes wrong

### Maintenance Windows

- Scheduled time frames for when changes are implemented
- Usually during off-peak hours to minimize disruptions

### Standard Operating Procedures (SOPs)

- Detailed, step-by-step instructions on how to carry out the change
- Ensure everyone understands their responsibilities, timelines, and execution to minimize mistakes

## Cybersecurity awareness and reporting

### Security Awareness, Monitoring, and Reporting

1. Initial reporting and monitoring
2. Development of security awareness practices
3. Execution of security awareness practices
4. Recurring monitoring and reporting

### Initial Reporting and Monitoring

- Regularly monitor your system with:
  - Security incident and Event Management (SIEM) systems
  - Intrusion Detection System (IDS)
  - Intrusion Prevention System (IPS)

### Develop Security Awareness Practices

- Starts with risk assessment
- Proper employee training
  - Tailored training programs
  - Simulated attacks
  - Target social engineering campaigns

### Execute Security Awareness Practices

- In-person, virtual, eLearning
- Make it engaging
- Regularly update training materials
- Gather feedback

### Recurring Monitoring and Reporting

- Set a schedule for reporting on security awareness
- Monthly or quarterly reports

# Chapter 14

- Incident Response
- Digital Forensics
- Continuity of operations
- Disaster Recovery

## Incident Response Plans (IRPs)

### Indicators of Compromise (IoC)

- Suspicious occurence that raises a red flag
- Examples:
  - Excessive outbound traffic to a single unknown host
  - Newly detected linux device on a windows network
  - Log/IDS/IPS alerts

### Incident Response Plan (IRP)

- Proactive preparation for reacting to an attack
  - Step-by-step procedures
  - Document(s)
- Response to threats
  - Detection
  - Containment
  - Eradication
- Contact list
- What to escalate
- IRP Life Cycle
  - Periodic review -> Assign roles -> Regular training -> Update the IRP
  - Prepare -> Identify and contain -> Eradicate -> Recover -> Lessons learned

### IRP Testing

- Designed to detect, contain, and eradicate threats
- Walkthroughs
- Simulations
- Tabletop exercises

> Incident response lifecycle and process on exam

## IRP Testing

### IRP Resilience Testing

- Table-top exercises
- Fail-over testing
- Simulations
- Parallel Processing
- Alert tuning

### Table-Top Exercises

- Company's key players mentally walk through potential disaster scenarios
- Discuss actions, decisions, and communication pathways

### Fail-Over Tests

- Systems are switched from primary to backup or standby modes
- Helps measure how smooth the transition happens
- Validates backup mechanisms

### Simulations

- Mimics potential cyber attacks or failures
- Helps teams practice their response strategies and skills and evaluate their tools and procedures

### Parallel Processing

- Running systems concurrently to ensure uninterrupted service
- If components fail, there's a backup already running
- Mitigates risk of single-point-of-failure

### Alert Tuning

- Validates expectations in monitoring solutions
- Helps identify false outcomes and distinguish between:
  - False-positive
    - System falsely indicates that there is a problem
  - False-negative
    - System reports everything is fine when there actually is a problem
  - True-positive
    - The event being alerted on is actually happening
  - True-negative
    - No event is being reported and there is no issue

## Threat Analysis and Mitigating Actions

### Cyber Kill Chain Analysis

- Trace steps taken for a successful compromise/data exfiltration event
- Security compromise knowledge can help prevent future breaches
- Recon -> Intrusion -> Exploitation -> Privilege escalation -> Lateral Movement -> Obfuscation/anti-forensics -> Denial of Service (DoS) -> Exfiltration

### MITRE ATT&CK Framework

- Used for post-compromise identification and analysis
  - Threat detection
  - What was done and how was it done?
- Identify attacker techniques
- Mitigation
  - Modify existing firewall, IDS/IPS alert rules
  - Deploy honeypot traps

### The Diamond Model of Intrusion Analysis

- Shows how malicious actors (adversaries) use exploit capabilities over an infrastructure against victims
- Data can stem from the use of honeypots

### Security Orchestration, Automation, and Response (SOAR)

- Automate Incident response using playbooks
  - Firewall rules, content filters
  - Application allow/deny lists
  - Revoke certificates
- Reduce incident response time

## Digital Forensics

- Legal hold
  - Ensures no data or digital evidence is deleted or altered
- Digital Chain of Custody
  - Documented timeline record of who handled the digital evidence
  - Ensures integrity and authenticity of the evidence
- Acquisition
  - Collecting digital data without altering it
- Reporting
  - Analyzing the digital data and creating a report containing:
    - Findings
    - Actions taken
    - Any other relevant information
- E-discovery
  - Finding, collecting, and delivering electronic information relevant for use in legal cases
- Preservation
  - Ensuring the evidence remains safe, intact, and unchanged
  - Make backups and store them safely

### Steganography

- Concealing information within seemingly unsuspicious data
- Criminals can try and hide data in other messages, videos, or images

## Business Continuity and Alternate Sites

### Planning for Disasters

- Business continuity plan (BCP)
  - Continuity of operations (COOP)
  - Broad scope
- Disaster Recovery Plan (DRP)
  - Narrow scope such as specific server
- Organizational policies
  - Change Management
  - Asset management
  - Security
- Disaster Types
  - Natural Disasters
  - Man-made disasters
  - Utility failures
  - Intentional Sabotage
  - Cybersecurity attacks

### Disaster Recovery Sites

- Site risk assessment
  - Geographical location
- Site components
  - Hardware
  - Software
  - Data
  - Personnel
- The public cloud is often used as an alternate site

### Hot Site

- Hardware
- Software
- Networking in place
- Up-to-date data
  - Continuous replication with primary site
- Personnel
- Quicket switchover time, most expensive

### Warm Site

- Hardware
- Software
- Networking in place
- No up-to-date data
- Longer switchover time than hot, less expensive than hot
- Personnel may be present

### Cold Site

- Basic IT infrastructure in place
  - Networking
- No hardware
- No software
- No data
- No personnel
- Longest switchover time, cheapest type of recovery site

## Data Backup

### Data Backup Considerations

- On-premises
  - Tape
  - Network attached storage (NAS)
  - Storage area network (SAN)
- Offsite
  - Cloud
- Compression
- Encryption
- Type of backup
- Virtual Machine
  - snapshots
  - custom images
- Full/Copy Backup
  - All data is backed up
    - Longest time for backup
    - Shortest time for restore
  - Example
    - Weekly full backup
- Incremental Backup
  - New/modified data since the last incremental backup
    - Shortest time to backup
    - Longest time to restore
  - Example:
    - Full backup weekly, incremental nightly
- Differential Backup
  - New/modified data since last fill backup
    - Longer to backup than incremental, shorten than full
    - Quicker to restore than incremental, slower than full
