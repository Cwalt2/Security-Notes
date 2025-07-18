
# Security operations (28%)

- [ ] Computing resources: applying secure baselines, mobile solutions, hardening, wireless security, application security, sandboxing, and monitoring.
- [ ] Asset management: explaining acquisition, disposal, assignment, and monitoring/tracking of hardware, software, and data assets.
- [ ] Vulnerability management: identifying, analyzing, remediating, validating, and reporting vulnerabilities.
- [ ] Alerting and monitoring: explaining monitoring tools and computing resource activities.
- [ ] Enterprise security: modifying firewalls, IDS/IPS, DNS filtering, DLP (data loss prevention), NAC (network access control), and EDR/XDR (endpoint/extended detection and response).
- [ ] Identity and access management: implementing provisioning, SSO (single sign-on), MFA (multifactor authentication), and privileged access tools.
- [ ] Automation and orchestration: explaining automation use cases, scripting benefits, and considerations.
- [ ] Incident response: implementing processes, training, testing, root cause analysis, threat hunting, and digital forensics.
- [ ] Data sources: using log data and other sources to support investigations.

## Secure Baselines

- May require multiple deployment mechanisms
  - Active directory group policy, MDM, etc.
- Automation is key
- Rarely Change
- Other baselines may require ongoing updates
  - A new vulnerability is discovered
  - An updated application has been deployed
  - A new operating system is installed
- Test and measure to avoid conflicts
  - Some baselines may contradict others
  - Enterprise environments are complex

## Hardening Targets

- No system is secure with the default configurations
  - You need some guidelines to keep everything safe
- Hardening guides are specific to the software or platform
  - Get feedback from the manufacturer or internet group
  - They will have the best details

### Mobile Devices

- Always-connected mobile technologies
  - Phones, tablets, etc.
  - Hardening checklists are available from manufacturers
- Updates are critical
- Segmentation can protect data
  - Company and user data are separated
- Control with an MDM
  - Mobile device Manager

### Workstations

- User desktops and laptops
  - Windows, MacOS, Linux, etc.
- Constant monitoring and updates
  - Operating systems, applications, firmware, etc.
- Connect to a policy management system
  - Active directory group policy
- Remove unnecessary software
  - Limit the threats

### Network Infrastructure Devices

- Switches, routers, etc.
  - You never see them, but they are always there
- Purpose-built devices
  - Embedded OS, limited OS access
- Configure authentication
  - Don't use defaults
- Check with the manufacturer
  - Security updates
  - Not usually updated frequently
  - Updates are usually important

### Cloud Infrastructure

- Secure the cloud management workstation
  - The keys to the kingdom
- Least privilege
  - All services, network settings, application rights and permissions
- Configure Endpoint Detection and Response (EDR)
  - All devices accessing the cloud should be secure
- Always have backups
  - Cloud to Cloud (C2C)

### Servers

- User accounts
  - Minimum password lengths and complexity
  - Account limitations
- Network access and security
  - Limit network access
- Monitor and secure
  - Anti-virus, anti-malware

### SCADA

- Supervisory Control and Data Acquisition System
  - Large-scale, multi-site Industrial Control Systems (ICS)
- PC manages equipment
  - Power generation, refining, manufacturing equipment
  - Facilities, industrial, energy, logistics
- Distributed control systems
  - Real-time information
  - System control
- Requires extensive segmentation
  - No access from the outside

### Embedded systems

- Hardware and software designed for a specific function
  - Or to operate as part of a larger system
- Can be difficult to upgrade
  - Watches and televisions are relatively easy
  - Other devices may not be easily modified
- Correct vulnerabilities
  - Security patches to remove potential threats
- Segment and firewall
  - Prevent acccess from unauthorized users

### RTOS (Real-Time Operating System)

- An operating system with a deterministic processing schedule 
  - No time to wait for other processing schedule
  - Industrial equipment, automobiles, military environments
- Isolate the system
  - Prevent access from other areas
- Run with the minimum services
  - Prevent the potential for exploit
- Use secure communication
  - Protect with a host-based firewall

### IoT devices

- Heating and cooling, lighting, home automation, wearable technology, etc.
- Weak defaults
  - IoT manufacturers are not security professionals
  - Change those passwords
- Deploy updates quickly
  - Can be significant security concern
- Segmentation
  - Put IoT devices on their own VLAN

### Site Surveys

- Determine existing wireless landscape
  - Sample the existing wireless spectrum
- Identify existing access points
  - You amy not control all of them
- Work around existing frequencies
  - Layout and plan for interference
- Plan for ongoing site surveys
  - Thing will certainly change
- Heat maps
  - Identify wireless signal strengths

### Wireless survey tools

- Signal coverage
- Potential interference
- Built-in tools
- 3rd-party tools
- Spectrum analyzer

### Mobile Device Management (MDM)

- Manage company-owned and user-owned mobile devices
  - BYOD - Bring Your Own Device
- Centralized management of the mobile devices
  - Specialized functionality
- Set policies on apps, data, camera, etc.
  - Control the remote device
  - The entire device or a "partition"
- Manage access control
  - Force screen locks and PINs on these single user devices

### BYOD
  
- Bring Your Own Device
- Bring Your Own Technology
- Employee owns the device
  - Need to meet the company's requirements
- Difficult to secure
  - It's both a home device and a work device
  - How is data protected?
  - What happens to the data when a device is sold or traded in?

### COPE

- Corporate owned, personally enabled
  - Company buys the device
  - Used as both a corporate device and a personal device
- Organization keeps full control of the device
  - Similar to company-owned laptops and desktops
- Information is protected using corporate policies
  - Information can be deleted at any time
- CYOD - Choose Your Own Device
  - Similar to COPE, but the user's choice of device

### Cellular networks

- Mobile devices
  - "Cell" phones
  - 4G, 5G
- Separate land into "cells"
  - Antenna coverages a cell with certain frequencies
- Security concerns
  - traffic monitoring
  - location tracking
  - worldwide access to a mobile device

### WiFi

- Local network access
  - Local security problems
- Same security concerns as other WiFi devices
- Data capture
  - Encrypt your data!
- On-path attack
  - Modify and/or monitor data
- Denial of service
  - Frequency interference

### Bluetooth

- High speed communication over short distances
  - PAN (Personal Area Network)
- Connects our mobile devices
  - Smartphones, tethering, headsets and headphones, smartwatches, etc.
- Do not connect to known bluetooth devices
  - There's a formal pairing process to prevent unauthorized connections

### Securing a wireless network

- An organization's wireless network can contain confidential information
  - Not everyone is allowed access
- Autheticate the users before granting access
  - Who gets access to the wireless network?
  - Username, password, multi-factor authentication
- Ensure that all communication is confidential
  - Encrypt the wireless data
- Verify the integrity of all communication
  - The received data should be identical to the original sent data
  - A message integrity check (MIC)

### The WPA2 PSK problem

- WPA2 has a PSK brute-force problem
  - Listen to the four-way handshake
    - Some methods can derive the PSK hash without the handshake
  - Capture the hash
- With the hash, attackers can brute force the pre-shared key (PSK)
- This has become easier as technology improves
  - A weak PSK is easier to brute force
  - GPU processing speeds
  - Cloud-based password cracking
- Once you have the PSK, you have everyone's wireless key
  - There's no forward secrecy

### WPA3 and GCMP

- WiFi Protected Access 3 (WPA3)
  - Introduced in 2018
- GCMP block cipher mode
  - Galois/Counter cipher mode
  - A stronger encryption than WPA2
- GCMP security services
  - Data confidentiality with AES
  - Message Integrity check (MIC) with Galois Message Authentication Code (GMAC)

### SAE

- WPA3 changes the PSK authentication process
  - Includes mutual connection
  - Creates a shared session key without sending that key across the network
  - No more four-way handshakes, no hashes, no brute force attacks
- Simultaneous Authentication of Equals (SAE)
  - A Diffie-Hellman derived key exchange with an authentication component
  - Everyone uses a different session key, even with the same PSK
  - An IEEE standard - the dragonfly handshake

### Wireless Authentication Methods

- Gain access to a wireless network
  - Mobile users
  - Temporary users
- Credentials
  - Shared password / pre-shared key (PSK)
  - Centralized authentication (802.1x)
- Configuration
  - Part of the wireless network connection
  - Prompted during the connection process

### Wireless security modes

- Configure the authentication on your wireless access point/wireless router
- Open system
  - No authentication password is required
- WPA3-Personal/WPA3-PSK
  - WPA2 or WPA3 with a pre-shared key
  - Everyone uses the same 256-bit key
- WPA3-Enterprise / WPA3-802.1x
  - Authenticates users individually with an authentication server (i.e., RADIUS)
