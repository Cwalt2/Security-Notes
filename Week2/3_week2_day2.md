# Week 2 Day 2

## Physical Security Chapter 3

> Locks, doors, guards, etc. not just breaking through software

### IT services rely on underlying hardware

- On-premises
- Cloud

### Local access to IT systems is a security risk

- Encrypt data at rest

### Personnel

- Guards
- Badges
- Visitor Logs
- Robot Sentries
  - Robot Guards
  - Wireless Security Guards
- Reception

### Facility Security

- Location
  - Undisclosed address
  - Protection from natural disasters
- Signage
- Fencing
  - Height
  - Periodic inspection
- Bollards/barricades
- Industrial camouflage
- Motion detection
  - Lighting
  - Alarm systems
- Server Room
  - Locked equipment racks
  - Safe
  - Protected cable distribution
  - Door lock
    - Physical
    - Electronic
    - Biometric
  - Security cameras
  - Class C fire suppression
  - Access control vestibule
- Air gapped networks
  - Can't be accessed from the outside
  - Can be bypassed by physical means
    - USB drives
    - take home laptops
    - Employee 

## Environmental Security

### Server Room Airflow Management

- Keep incoming cool air separated from outgoing warmer air
- Draw in cool air to equipment
- Draw hot air from equipment out
- Containment panels/curtains
  - Prevent cool and warm air from mixing
- Blanking panels
  - Fill empty rack slots to optimize airflow
- Bad airflow can cause shutdown/overheat

### Environmental Monitoring

- Sensors
  - Temperature
  - Pressure
  - Humidity
  - Noise
  - Proximity
- Monitoring Software

### Review Question

> ARP cache poisoning: ARP cache update on the network using a message to update the specific MAC address that is the attacker

### Physical Security Concerns

- Computer left unattended (even if locked)
- Computer left logged in
- Unlocked doors and windows
- Access to a server room or wiring closet/panel
- Workstations near windows
- Unencrypted storage media
- USB ports on computers that are not disabled

# Identity and Account Management Chapter 4

> Triple A, AAA Authentication, Authorization, and Accounting

## Identity, Authentication, and Authorization

- Identification
  - Username
  - Drivers License
- Authentication
  - Password
  - Proof of purchase/insurance
- Authorization
  - Make sure you're actually supposed to be there
  - Are you in the right seat? Are you on the registration?

### Authentication

- Using more than one factor of authentication
- Factors
  - Something you know
  - Something you are
  - Something you have
- Authentication Attributes
  - Something you do
    - Signature
  - Something you exhibit
    - testing typing speed
  - Something you know
    - Trust
    - Certificates from websites
  - Somewhere you are
    - Physical location
    - Zip code when using a credit card

## Enabling Multifactor Authentication

- Identification
- Authentication
- Authorization
- Accounting
  - Auditing

## Authorization

- Based on permissions granted
- Determines resource permissions
- Can only occur after authentication
- Resources
  - Targets that have permissions applied to them
  - Example: files, database rows, web app
- Accounting/Auditing
  - Track permissions usage for accountability purposes
  - Who or what accessed which resource, how long, on what date?

## Accounting/Auditing

- Often called auditing
- Track activity
- Must have separate user accounts for each user
- Types of auditing
  - Resource access
  - Failed logon attempts
  - Changes to files/database records
- Anything with a public IP will be attacked

## Authentication Methods

### Password Vaults

- Also called "Password Managers"
- Example: Lastpass, cloud-based vaults to store password keys
- A master key protects the vault
  - Don't forget it!

### One-Time Password (OTP)

- Unique password (code) generated for single use
  - Static code sent via email or sms text
- Time-based OTP (TOTP)
  - Code is only valid for a short period of time
- Software notification methods (push notification)
  - Phone call
  - Short message service (SMS) text
  - Email
- HMAC-based one-time password (HOTP)
  - HMAC encrypts a hash to ensure authenticity

### Certificate-Based Authentication 

- PKI certificates are issued by a trusted authority to an individual entity
  - Device, VPN, app access
  - Can be stored on a smart card
    - Called a Personal Identity Verification (PIV) card
    - Common access card (CAC) can authenticate to everything

### SSH Public Key Authentication

- Sign in with username and password (passphrase) as well as a private key
- Public key stored on the server
- Private key stored on admin device

### Biometrics

- Fingerprint
- Retina
- Iris
- Facial
- Voice
- Vein
- Gait Analysis
- Efficacy rates
  - False acceptance
  - False rejection
  - Crossover error rate

## Access Control Schemes

### Credential Policies

#### Defines who gets access to what

- Employees
- Contractors
- Devices
- Service Accounts
- Administrator/root accounts
  - Privileged Access Management (PAM)

### Attribute Based Access Control (ABAC)

- Uses attributes to determine permissions
  - Example: date of birth or device type

### Role-Based Access Control (RBAC)

- A role is a collection of related permissions
- Role occupants get permissions of the role

### Rule-Based Access Control (RBAC)

- Uses conditional access policies
- Examples
  - MFA
  - Device Type
  - Location

### Mandatory Access Control (MAC)

- Resources are labeled
  - Devices, files, databases, network ports, etc.
- Permission assignments are based on resource labels and security clearance

### Discretionary Access Control

- Data custodian sets permissions at their discretion

## Account Management

### User Accounts

- Unique account per user
- Assign permissions to groups
- Principle of least privilege
- User Account Auditing
- Disablement

### Account Management

- Rights/privileges
- Account types
  - User, device, service
  - Administrator/root
  - Privileged
  - Guest

### Account Policies

- Employee onboarding
- Password policies
  - Complexity
  - History
  - Reuse
- Account lockout
- Time-based logins
  - Enforce login/logout times
- Geolocation
  - Where a user is located
  - Geofencing
    - User geolocation determines resource access
  - Geotagging
    - Adding location metadata to files and social media posts
- Impossible travel time
- Risky login
  - A baseline of normal activity is required first

## Network Authentication

### Network Authentication Protocols

- Password Authentication Protocols (PAP)
  - Outdated
  - Cleartext Transmissions
- Microsoft Challenge Handshake Authentication Protocol (MS-CHAPv2)
> Client requests authentication from server
> Server sends challenge to the client
> Client responds to challenge by hashing response with user's password
> Server compares response to its own computed hash and authenticates if they match

### Microsoft New Technology LAN Manager (NTLM)

- Supersedes older LANMAN protocol
- Used on Windows workgroup computers
- Password hashes with NTLM are not salted
- NTLM v2 passwords are salted
> Windows group environment question it will be NTLM

### Kerberos

- Microsoft Active Directory authentication
- Kerberos Key Distribution Center (KDC)
- Authentication Service (AS)
- Ticket-Granting Service (TGS)
- Ticket-Granting Ticket (TGT)

### Extensible Authentication Protocol (EAP)

- Network Authentication Framework
- Examples
  - PKI certificate authentication
  - Smart card authentication
- Uses TLS transport
- Applies to wired and wireless networks

### IEEE 802.1x

- Port based network access control
- Centralized RADIUS server authentication
- Wired and wireless network edge devices
  - Ethernet switches
  - Wi-Fi routers
  - VPN appliances

### Remote Access Dial-in User Service (RADIUS)

- Centralized authentication
- RADIUS clients
  - Network switch
  - VPN appliance
  - Wireless router
- RADIUS supplicant

#### RADIUS Variations

- Terminal Access Controller Access Control System (TACACS)
- Terminal Access Controller Access Control System Plus (TACACS+)
- Extended TACACS (XTACACS)

> Supplicant -> WiFi access point (IEEE 802.1x compliant) -> RADIUS authentication server

## Identity Management Systems

### Single Sign-On (SSO)

- User credentials are not requested after initial authentication
- Protocols
  - OpenID
  - OAuth

### Identity Federation

- Multiple resources that trust a single authentication source
- Centralized trusted identity provider (IdP)
  - Trusted by resource provider
- Security Assertion Markup Language (SAML)
  - SAML token is a digital security token that proves identity
> User connects to web app -> Resource provider (RP) -> "I dont do authentication" to user -> User authenticates to IdP -> IdP provides user with digitally signed authentication token -> User connects to web app

> Review term Captive Portal


