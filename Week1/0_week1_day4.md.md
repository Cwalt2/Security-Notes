
# Week 1 -- Day 4

## Threat Intelligence Sources

- Facilitate risk management
- Hardening can reduce incident response time
- Provide cybersecurity insight
  - Adversary tactics, techniques, and procedures
  - Threat maps (ex. geographical representations of malware outbreaks)
  - [threatmap.checkpoint.com](https://threatmap.checkpoint.com/) check malware attacks happening currently
    - Current attacks
    - malware used
    - infrastructure constantly targeted
- closed/proprietary

### **OSINT** (Open Source Intelligence)

#### Government reports, Media, Academic Papers

- [exploit-db.com](https://www.exploit-db.com/)
  - google hacking exploit
  - Can actually exploit live web servers
- Vulnerability Databases
  - Common vulnerabilities and exposures **(CVEs)**
    - Uniquely numbered threat
    - **OSINT** tactic
    - [cve.org](https://www.cve.org/)
      - database of common vulnerabilities

### Dark Web/Dark Net

#### Tor Network, Tor Web browser

- Encrypted anonymous connections
- Not indexed by search engines
- Tor encryption and anonymity
  - Journalists
  - Law Enforcement
  - Government Informants
- Tor
  - Tor browser -> Tor network entry point -> Tor relay servers -> Tor network exit point -> Origin Tor browser IP
  - Automated Indicator Sharing **(AIS)**
    - Exchange of Cybersecurity Intelligence **(CI)** between entities
  - Structured Threat Information eXpression **(STIX)**
    - A form of **AIS**
    - Data Exchange format for cybersecurity intelligence
  - Trusted Automated eXchange of Intelligence Information **(TAXII)**
    - Like RSS feed for threats
    - Consists of **TAXII** servers and clients
    - Real-time cyber intelligence feeds

## Risk Management

- Risk Vector
  - Mission-critical IT systems
    - Payment Processing
    - Human resources
    - emergency
  - Sensitive Data
    - Do we know what we have and where it is?
  - Third Party Access
- Physical Risk Vectors
  - Access Control vestibules (mantraps)
  - Server Room Access
  - Limit USB bootable devices
- Risk Management Frameworks **(RMFs)**
  - Center for internet security **(CIS)**
    - Cybersecurity best practices
  - NIST Risk Management Framework **(RMF)**/Cybersecurity Framework **(CSF)**
    - Cybersecurity Risk Management
  - International Organization for Standardization/International Electrotechnical Commission **(ISO/IEC)**
    - 27001/27002/27701/31000
      - IT system and Information Security
  - Financial **RMFs**
    - Statement on Standards for Attestation Engagements System and Organization Controls **(SSAE SOC 2)**
      - Financial Statement Integrity
      - Internal Controls
      - Type I and Type II
    - NIST Special Publication **(SP)** 800-30, Rev. 1
    - Data Privacy Regulations and Standards
      - General Data Protection **(GDPR)**
        - Protects EU citizens' private data
      - Health Insurance Portability and Accountability Act **(HIPAA)**
        - Protect American patient medical information
      - Payment Card Industry Data Security Standard **(PCI DSS)**
        - Protect cardholder information
    - Types of Security Policies
      - Acceptable Use Policy **(AUP)**
        - Email, Social Media, Web Browsing
      - Resource access policies
        - App or file access
      - Account policies
        - Account hardening
    - Data Retention policies
      - Often dictated by regulations
      - Change control policies
      - Asset Management policies

## Malware

### Software that is detrimental to the operation of a host

#### Ransomware

- Once infected, encrypts all files with a ransom to unlock
- bulk file renames, fast encryption of files, and unorthodox file extensions added to files
- other names include, cryptomalware/crypto-ransomware
- uses encryption to lock a user out of a system
- attacker hides your data until you pay a ransom

#### Trojan

- self contained programs made to look like a trusted program
- command prompt window that quickly disappears
- Applications becoming suddenly unresponsive to usual commands
- Remote Access Trojan **(RAT)**
- Maliciously takes control of a system remotely

#### Worms

- malware capable of rapidly infecting many systems on an enterprise network by transmitting copies of itself from one system to another via network connections.
- disrupt network bandwidth
- evolved payloads range from recording keystrokes to deleting files
- Indicators of compromise includes a series of computers infected with the same virus

#### Keylogger

- A type of surveillance technology used to monitor and record keystrokes
- stealing login information, critical enterprise data and personally identifiable information
- Can track sites visited and only log keystrokes entered on domains of interest
- common indicators include accounts being compromised with no clear reason
- Many have WAPs built in for remote access

#### Adware

- a form of malware that generates money
- forcefully shows ads from perpetrator to generate ad revenue
- adware is not a severe concern but can be a gateway for more serious malware
- indicators include ads where not usually found ex. search engine start up page

#### Virus

- malicious program that infects and damages a system
- tablet, smartphone, or computer
- Can destroy data on the device, prevent from booting, or using resources that results in shutdown or malfunction
- common indicators are programs that don't respond to commands to shut down, quit, or exit
- Program that can replicate only through definite user interaction
- activates once a user clicks or downloads
- fileless malware/virus
  - no file, only lives in memory
  - difficult for anti-malware to detect

#### Spyware

- a malicious program that collects information regarding a user's habits/activities on a system
- indicators include other program completing searches, removing a program and it redownloads itself, reduction in systems' connection speed, takes up disk space and cause severe performance issues

#### Rootkit

- software commonly used to obtain root-level access and hide specific things from the OS
- indicators include antivirus program shutting itself off for no apparent reason, constant blue screening, constant rebooting, and incorrect system clock and date
- Often invisible

#### Bot

- an automated malicious program that gathers information on the internet
- usually executed from compromised systems remotely controlled by adversaries
- indicators include issues downloading antimalware software updates or being installed, issues downloading OS updates
- hosts are called bots or zombies
- cause botnet attacks such as DDoS attack
- Usually consists of more than 7 individual unsuspecting computers
- Command and Control **(C2/C&C)**
- protocols that automate the control, not requiring human interaction after the initial programming

#### Backdoor

- malicious program that creates a converted channel for aiding adversaries
- can access and control compromised system through phones and other mobile gadgets
- indicators include locked out of PC under normal use, unrecognized messages sent from accounts, pop-up ads
- can be added by developers as maintenance but abused by attackers

#### Logic Bomb

- slag-code
- designed to explode under certain conditions to erase critical files or other serious damage
- indicators include custom programs with full access, recently developed programs that act strange after being used
- Often a script set to execute
- Created with a timer or specific event to set off the "bomb"

#### Potentially Unwanted Programs **(PUPs)**

- Software that may have negative or undesirable effects
- other names are crapware, adware, spyware, bloatware
