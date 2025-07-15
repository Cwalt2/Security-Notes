# Chapter 10

## Securing Dedicated and Mobile Systems

### Programmable Logic Controller (PLC)

- Industrial control system (ICS) device
  - Sensors
  - Valves
  - Robots,actuators
- Has an IP address
- Vendors
  - Siemens, Allen-Bradley
- Security Implications
  - Firmware updates

### Real-Time Operating System (RTOS)

- Used with PLCs
  - RTLinux
  - VxWorks
- Security Implications
  - Firmware updates
  - Network isolation

### Supervisory Control and Data Acquisition (SCADA)

- Collection of ICS devices
  - Focused on specific tasks
  - Manufacturing, water, oil pipelines, power grid
  - Can be dispersed over a wide area network
- SCADA over WAN
  - SCADA master station -> WAN link -> Remote Terminal Unit (RTU) -> PLCs

> Indirectly tested on roles PLCs play

## Internet of Things (IoT) devices

- Computing device connected to the internet
  - May have an embedded web server
- Security implications
  - Update firmware
  - Change default credentials
  - Network isolation
- IoT Devices
  - Smart light bulbs
  - Medical devices
  - Video surveillance systems

### Modern Vehicle Security

- Connectivity
  - Bluetooth
  - Cellular
  - WiFi hotspot
- Security implications
  - Systems can be hacked
- Vehicle key fobs
  - Firmware can be vulnerable
  - Might have to replace or update compromised key fob

### Zigbee Network Protocol

- Smart home wireless networking
- Uses 128-bit AES encryption
- Does not use TCP/IP
- Interconnects smart home IoT devices
  - Smart locks, HVAC, Smart lights
- Security implications
  - Update firmware
  - Change default settings
  - Harden connected devices
  - Network isolation

## Connecting to Dedicated and Mobile Systems

### Mobile Device Wireless Communication

- Global Positioning System (GPS)
  - Uses satellites
- Infrared
  - Legacy
  - Line-of-sight
- Cellular
  - Phone calls
  - SMS text/multimedia
- Wi-Fi
- Bluetooth
- Near-field communication (NFC)

### Global Positioning System (GPS)

- Satellite navigation system for objects on Earth
- Point-to-multipoint
- GPS receivers use triangulation to determine exact longitude and latitude position
- Security implications
  - Disable when not needed

### 4th Generation (4G) Cellular

- Use radio frequencies
  - Narrow-band (small range)
  - Broadband (wide range)
    - Multiple transmissions at the same time (baseband sends one signal)
- Cell coverage is ~10km (6.2 miles)
- Security implications
  - firmware over-the-air (OTA) updates

### 5th Generation (5G) Cellular

- High data speeds
  - Up to 10 Gbps
- Cells are smaller than with 4G
  - Up to 2km (1.2 miles)
- Base stations use fibers connections
- Requires 5G-capable devices

### WiFi Direct

- Peer-to-peer WiFi
  - Not apple devices
- Does not use a wireless router
- No internet connectivity

### Mobile Device Tethering

- Share Internet connection
- Wireless
  - WiFi hotspot
- Wired
  - USB tethering
  - USB on-the-go (attachment with USB ports)

## Security Constraints for Dedicated Systems

### Mobile Device Constraints

- CPU
  - Limited Power
  - lightweight cryptography
  - Elliptic Curve Cryptography (ECC) uses a small crypto key size
- Battery
  - Limited power duration
- Limited transmission range
- Limited device access
  - Rooting (Android)
  - Jailbreaking (Apple)
- Unable to patch firmware
  - Embedded devices
  - IoT devices
- Unable to change defaults or authentication settings
- Mitigation
  - Replace device
  - VLAN device isolation

## Mobile Device Deployment and Hardening

### Mobile Device Provisioning

- Bring Your Own Device (BYOD)
  - Usually IT department applies centralized policy
- Choose Your Own Device (CYOD)
  - Company offers a range of devices to choose from
- Coporate-Owned Personally Enabled (COPE)
  - Personal and Business use
  - Corporate and personal device partitions (containers) for remote wipe

## SIM Card

### Subscriber Identity Module (SIM) Cards

- Authenticates device to carrier network
- Contains carrier subscription data, SIM card serial number, and phone contacts (if not in the cloud)
- Carrier unlock
  - Reuse device on a different carrier network
  - Check carrier unlock requirements

### Mobile Device Hardening

- reduce the attack surface
- Management at scale
  - Mobile Device Management (MDM)
  - Mobile Application Management (MAM)
    - Sideloading
    - Geofencing
    - SE Android
  - Unified Endpoint Management (UEM)
- Authentication
  - Password
  - PIN
  - Facial Recognition
  - Screen lock
- Full Device Encryption
- Micro SD Hardware Security Module (HSM)
  - Cryptographic operations
    - Encryption
    - Decryption
    - Digital signatures
    - Generating hashes

### Embedded Systems

- Embedded, specialized, mobile
- Fixed hardware
  - example: iPhone
- Specialized use
- Fixed, specialized operating system

### Types of Embedded Systems

- Raspberry Pi
  - System on chip (SoC)
    - CPU, RAM, Storage
  - Specialized OS (Raspberry Pi OS)
- Industrial Control System (ICS)
  - Controls manufacturing or utility systems
  - Runs real-time operating system (RTOS)
- Supervisory Control and Data Acquisition (SCADA)
  - Designed for remote large-scale, distributed processes
- Internet of Things (IoT)
  - Small computing devices
  - OS, CPU, RAM, storage, Internet connection
- Medical Systems
- In-vehicle computing systems
- Unmanned Aerial Vehicle (UAV)
  - AKA drone
- Smart meter
- Surveillance systems
  - Storage
  - Motion detection
  - infrared
  - Sound-based
  - Smart locks
- Voice over IP (VoIP)
  - Sends voice calls over a network
- Mobile Systems
  - Embedded devices that are mobile

# Chapter 11

## DNS Security

### Common Secure Protocols

- DNS
  - TCP/UDP port 53
  - Domain Hijacking
  - URL redirection
  - Cache poisoning
  - Domain Name System Security Extensions (DNSSEC)
    - All DNS zones have certificates
- Simple Network Management Protocol (SNMP)
  - UDP port 161/162
  - Version 1, 2, 3
- Secure Shell (SSH)
  - TCP 22
- Secured File Transfer Protocol/FTP over SSL (FTPS)
  - TCP port 990
- SSH FTP (SFTP)
  - TCP port 22
- Secure Real-Time Transport Protocol (SRTP)
  - UDP port 5004

> Port numbers will be on the exam

## Secure Web and Email

### Securing Web Apps

- Can be accessible internally or externally
- Hide true web server IP address
  - Load balancing
  - Reverse proxying
  - Network Address Translation (NAT)
- HTTPS
  - Enabled on the web server
  - Requires a server PKI certificate
  - Uses TCP port 443 instead of 80
  - TLS
    - Uses version 1.2 or higher

### Web App User Authentication

- Lightweight Directory Access Protocol Over SSL (LDAPS)
  - Directory service access protocol
  - Supported by Microsoft Active Directory
  - Requires a server PKI certificate
  - Uses TCP port 636 instead of 389
- On-premises and cloud

### Simple Mail Transfer Protocol (SMTP)

- Domain reputation
  - Determines if mail will be received by other SMTP hosts
- Secure/Multipurpose Internet Mail Extensions (S/MIME)
  - Encrypt and sign email messages
  - Requires a client PKI certificate

### Email Protocols

- SMTP
  - Email transfer protocol
- Post Office Protocol (POP)
  - Client email retrieval protocol
- Internet Message Access Protocol (IMAP)
  - Client email retrieval protocol
- Each can be secured with a server PKI certificate

## Request Forgery Attacks

### Request Forgeries

- Cross-site request forgery (CSRF)
  - Targets users and unchanging session tokens
  - Designed to hijack authenticated sessions between a client and a server
- Server-side Request Forgery (SSRF)
  - Targets web servers
  - Designed to have server make HTTP requests to other services
- Mitigation
  - Harden client devices
  - Use web application firewall (WAF)

## Cross-Site Scripting Attack (XSS)

- Starts with a web app that doesn't properly validate or sanitize input
  - All user input must be untrusted
- Attacker injects malicious code into vulnerable website
  - Javascript is commonly used
- Website visitors unknowingly execute malicious code

## Web Application Security

- For web app server admins and web app developers
- Harden public-facing and private web apps

### Injection Attacks

- Malicious user input is accepted by the web app
- Types
  - Structured Query Language (SQL)
  - Lightweight Directory Access Protocol (LDAP)
  - Extensible Markup Language (XML)
- Mitigation
  - Sanitize all user input

### Secure Coding

- Software development security best practices
  - Input validation
  - Secure web browser cookies
  - HTTP headers
  - Code signing
  - Use trusted components and APIs

### Continuous Integration and Continuous Delivery (CI/CD)

- Automate developer code changes
- Test for quality assurance
- Send update notifications to users for code version control
- Security issues
  - Attackers could make changes and inject into the update

### Infrastructure As Code

- VM templates
- Cloud templates
- Rapid and consistent provisioning/deprovisioning
  - Useful for sandbox testing
- Security issues
  - Attackers could modify templates

### Software Testing

- Static testing
  - Code review
  - Manually scanning code
- Dynamic testing
  - Observe runtime behavior
- Fuzzing
  - Provide app with unexpected data

### OWASP Top 10

- Broken Access Control
- Cryptographic Failures
- Injection
- Insecure Design
- Security Misconfiguration
- Vulnerable and Outdated Components
- Identification and Authentication Failures
- Software and Data Integrity Failures
- Security Logging and Monitoring Failures
- Server-Side Request Forgery

### Web App Vulnerability Scanning

[zapproxy.com](zaproxy.com)
