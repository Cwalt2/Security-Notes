# Chapter 8 Securing Wireless LAN

## Wi-Fi Encryption Standards

### Wireless Equivalent Privacy (WEP)

- Part of original 802.11 standard
- RC4 streaming
- Began with initialization vector (IV)
- Problem was with IVs

### IEEE 802.11i

- AES instead of RC4
- Pre-shared key (PSK) instead of IV
  - Or WPA-enterprise
    - Authenicate with RADIUS server
- The Problem:
  - Most WAPs and network cards couldn't handle AES
- The solution:
  - Wi-Fi Protected Access (WPA)
  - RC4 with PSK or RADIUS server
- WPA2
  - AES
  - Can do RADIUS or PSK
  - Counter-mode/CBC-MAC Protocol
    - CCMP
  - The Problem
    - Can be cracked through the handshake
- WPA3
  - Disallows outdated protocols
  - Protected Management Frames (PMF)
  - Simultaneous authentication of equals (SAE)
- Wi-Fi Protected Setup (WPS)
  - Must have WPS-capable wireless access points (WAPs) and devices
  - Press button on both WAP and device
  - Creates a WPA2-encrypted connection
  - The problem:
    - Easy to crack
  - The solution:
    - Devices no longer include it

## RFID, NFC, and Bluetooth

### Radio Frequency Identifier (RFID)

- Uses RF communication to track objects with RFID tags
- Range is ~5 meters (16.5 feet)
- Commonly used for inventory control, locating pets, and in some passports
- RFID tags are normally powered by the reading/scanning device

### Near Field Communication (NFC)

- Type of RFID
- Close-range wireless communications
  - Approximately 5 cm (1.5 inches)
- Common uses
  - Payment cards
  - Smartphone (data sharing, payments)
  - Read/write NFC tags

### Bluetooth

- 802.15.1 Standard
  - 2.4 or 5 GHz frequency range
- Wireless networking with shorted range than Wi-Fi
  - Class 1
    - Up to 100 meters (328 feet)
    - Example: USB Wi-Fi dongles
  - Class 2
    - 10 meters (33 feet)
    - Example: Bluetooth headset
- Devices must be paired together to communicate
  - Car stereo
  - headset
  - keyboards
- Bluetooth Attacks
  - Bluejacking
    - Unauthorized sending of anonymous messages to a bluetooth device
    - Example: sharing fake contact information with a message as the contact name
  - Bluesnarfing
    - Data theft from remote devices using Bluetooth
  - Mitigation
    - Disable bluetooth when not needed

## Wi-Fi Coverage and Performance

- Signal strength weakens over distance
  - Transmission power measured in decibel
  - milliwatts (dBm)
- Atmospheric conditions affect wireless conditions affect wireless connectivity

## Wi-Fi Site Survey

- Conduct during Wi-Fi deployment and troubleshooting
- Collect wireless stats
  - Signal strength
  - Noise
  - Channel overlapping
  - Transmission speeds

> possible question about connectivity issues

## Wi-Fi Discovery and Attack

- War-chalking
  - Sidewalk marking
- War-driving 
  - Scan from within vehicle
- War-flying
  - Scan using a drone

### Malicious WAP Targeting

- Rogue Access Point
  - Unauthorized wireless AP
- Evil Twin
  - Unauthorized wireless AP mimicking valid AP name

### Wi-Fi AP Beacon Frames

- Sent every ~100ms
- Clients cannot verify beacons
  - Key not established yet
  - Beacon frames are easily forged
- Contains
  - SSID (WLAN name)
  - Maximum transmit power (dBm)

### Wi-Fi attacks

- Connects to open WLANs
- Cracking WEP passphrase
- RF signal jamming
  - Interference
  - Wi-Fi channel overlap
  - Flood AP with deauthentication (disassociation) packets
  - Denial of Service (DoS) Attack

## Cracking WPA2

### Disassociation/Deauthentication Attacks

- Discover APs
- Discover connected clients
- Disconnect active client from AP
  - sudo aireplay-ng -0 1 -a \<AP MAC> -c \<Client MAC>
- Monitor client-AP handshake
- Perform online or offline dictionary or brute-force to determine PSK

## Wi-Fi Hardening

- Change default AP credentials
- Hide the SSID
- WLAN name is removed from AP beacon frames
- Clients must know the SSID to connect
- Clients must know PSK or credentials
- Enable MAC filtering
- Use WPA3 Enterprise
  - RADIUS server authentication
- Limit signal emanation
  - Transmit power levels
- Captive portal
  - Landing page (web site)
  - May require user authentication
    - Until authenticated, all HTTP requests show the landing page
  - User may only need to agree to terms of use

### Extensible Authentication Protocol (EAP)

- IEEE 802.1x RADIUS authentication
  - Supports identity federation
- EAP-FAST (Flexible Authentication via Secure Tunneling)
  - No certificates
  - Shared secret must be configured on both devices
- EAP-TLS
  - Server- and client-side certificates
- EAP-TTLS
  - Requires a server certificate
  - Encapsulates RADIUS messages
- Protected EAP
  - Requires a server certificate
  - Encapsulates EAP messages

## Securing Virtual and Cloud Environments

### Defending a Public Server

#### Distributed Denial of Service (DDoS)

- Botnets
- Network/App flooding
- Low and slow attacks
- Mitigation
  - Throttling
  - Blackhole routing

#### URL Hijacking/Redirecting

- Stems from
  - User typos that result in redirection to similar URL
  - Tainted search results redirect to a malicious site
- Also called "typosquatting"

#### Session Replay Attacks

- Attacker takes over user session
  - Cookie
  - URL
  - HTML form field
- Cookie Mitigation
  - Set HTTPOnly flag
    - Disallows JavaScript cookie access

#### Pass-the-Hash Attacks

- Takes advantage of password hashes
- Attacker compromises system with user login session
- Attacker uses the hash to gain access to other network resources

#### Managed Security Service Provider (MSSP)

- Security as a Service (SECaaS)
- Cybersecurity Outsourcing
  - 24/7 remote security monitoring
  - Vulnerability assessments
  - Pen tests
  - Report generation

## DDoS Attacks in the Real World

### Reflected DDoS attack

### Amplified DDoS Attack

### Network Time Protocol (NTP) Amplification Attack

## Containers and Software-Defined Networking

### Application Containers

- App components are managed as a single unit
- Microservices/API
  - App component decoupling
- Can be accessible over the network
  - Example: TCP port 80 for a web site

### Software-Defined Network (SDN)

- Facilitates network management
  - Command line
  - GUI
- Hide underlying network configuration complexities
  - Vnets
  - Subnets
  - VPNs

## Hypervisors and Virtual Machines

### Hypervisors

- OS that manages virtual machine guests
- On-premises hypervisor
  - Full configuration control
- Cloud hypervisors
  - Limited control
- Type 1
  - Bare metal OS
  - It is the OS
- Type 2
  - Runs as an app within an OS

### Virtual Machines Vulnerabilities

- Same as host hardening
  - Still have to install patches
  - Disable unused accounts/services
- VM sprawl
  - Unused, forgotten VMs
- VM escape
  - Attacker breaks out of VM to hypervisor
- CVE-2008-0923

### VM Hardening

- Disable unnecessary components
- Use complex passwords and MFA
- Limit public internet visibility
- Encrypt the VM

## Cloud Deployment Models

### Cloud Computing

- Running IT servicess on somebody else's equipment over a network
- Thin vs. thick client
- Fog/edge computing
  - Storage/compute at network perimeter
  - Reduces network latency
- Cloud Computing Characteristics
  - Pooled Resources
  - Broad Access
  - Self-service provisioning
  - Rapid Elasticity
  - Metered usage

### Public Cloud

- Anybody can sign up for an account
- Cloud tenant isolation
- Ongoing monthly expenses (OPEX)
- Shared IT responsibility depending on service

### Private Cloud

- Cloud is owned and used by a single organization
- Requires an up-front capital investment (CAPEX)
- Organization assumes full hardware/software responsibility

### Hybrid Cloud

- Combines public and private clouds
- Public clouds can be used as an alternate disaster recovery site

### Community Cloud

- Cloud computing for organizations/agencies with similar cloud computing needs
- Example:
  - Microsoft Azure Government Cloud

## Cloud Service Models

- Categories of Cloud Services Offerings
- Shared responsibility
  - Cloud service provider (CSP) is responsible for hardware
  - CSP may be responsible for software configurations
  - Cloud tenant may be responsible for software configurations

### Anything as a Service (XaaS)

- As an IT service that is accessible remotely over a network
- IT services run on provider infrastructure
- Adheres to cloud computing characteristics

### Common Cloud Service Models

- Infrastructure as a Service (IaaS)
- Platform as a Service (PaaS)
- Software as a Service (SaaS)

### Infrastructure as a Service (IaaS)

- Storage
- Networking
- Manually deployed and managed virtual machines
- Do not expose directly to the internet where possible
- CSP responsibility
  - Hardware
- Cloud tenant responsibility
  - VM and storage account deployment, hardening

### Platform as a Service (PaaS)

- Databases
- Software developer tools
- Underlying virtual machines are managed by the provider
  - Managed service
  - Serverless

### Software as a Service (SaaS)

- End-user productivity software
- CSP responsibility
  - Hardware
  - Virtual machines
  - Software installation and patching
- Cloud tenant responsibility
  - Software configuration
  - User provisioning

## Securing the Cloud

### CSP Cloud Security Responsibility

- Hardware
  - Power
  - HVAC
  - Hardware Configuration
  - Firmware Updates
- Software
  - PaaS and SaaS

### Cloud Tenant Security Responsibility

- Internet connection to the public cloud
  - Redundant network links to CSP
- Cross-region replication
  - Increases high availability
    - Virtual machines
    - Storage Accounts

### Cloud Security Controls

- Cloud Access Security Broker (CASB)
  - Enforces security policies when accessing cloud resources
  - Normally done via proxying
- Next-generation secure web gateway (SWG)
  - CASB functionality
  - Web content filtering
  - Data loss prevention (DLP)
- CSP firewall solutions
  - Example: Azure Network Security Group (NSG)
- Policies
  - Example: Azure Policy
  - Control cloud resource deployment
  - Assess cloud resource compliance
- Data Loss Prevention (DLP)
  - Prevent data exfiltration
  - Example: Azure Information Protection (AIP)

### Cloud Monitoring

- Detect abnormalities or suspicious activity (auditing)
- Who is deploying VMs?
- What apps are running?
- Log reviews are a type of "detective" security control
- Centralized log repository
  - Log forwarding
