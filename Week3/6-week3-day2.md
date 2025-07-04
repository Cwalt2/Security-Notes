# Chapter 6

## Disk RAID levels

### Redundant Array of Inexpensive Disks (RAID)

- Groups disks together to work as one
  - Better Performance
  - Data high availability
- Hardware RAID controller
  - Much quicker than software RAID
- Software RAID
  - Slower and less reliable than hardware RAID

### Storage Area Network (SAN)

- Storage out on a network
- Storage Area Network (SAN) Multipathing
  - Windows Server Fiber Channel HBA
  - Linux Server Fibre Channel HBA
  - Both servers are connected to the same 2 fiber channel switches that connects to a disk array configured with LUNs
  - Prevent drive failure

### RAID Levels

- Raid 0
  - Disk Striping
  - Better Performance
  - No availability benefit, if one drive fails all can fail also
- RAID 1
  - Disk Mirroring
  - Data in its entirety is written to two separate disks
- RAID 5
  - Disk Striping with distributed parity
  - Performance increase
  - Data Striped (D) and the related parity (P) are stored on separate disks
- RAID 6
  - Requires at least 4 disks
  - Stores 2 parity striped on each disk
  - Can tolerate failure of 2 disks
- RAID 10
  - RAID level 1, then 0
  - Disk Mirroring, then striping
  - Required at least 4 disks

## Securing Hardware Lesson

### Securing Hardware

- Limit Physical Access
  - Alarms, Sensors, locks
  - Card/RDIF cloning or skimming
- User vendor/technology diversity
- Limit USB storage device use
- Group Policy on Windows is an effective way of securing hardware
  - gpedit.msc
- Apply firmware patches
- Use USB data blocker
  - Mitigate infection via USB port
    - Prevents data transfer from other devices
    - USB Ninja cables
      - Immediate infection via USB with a virus
  - Allows recharging but not data transfer
- Trusted Platform Module (TPM)
  - Used as basis for hardware root of trust
  - Boot integrity
    - UEFI Secure Boot
    - Measured Boot
    - Boot Attestation
  - Disk Volume Encryption
    - Microsoft Bitlocker
- Failed Machine Boot
  - Causes
    - File corruption
    - Malware
    - Failing Disks
    - Misconfiguration
  - Remediation
    - Boot from alternative media
      - Live boot media
      - Be sure to require password
      - Revert to known state or last known-good configuration
- Redundancy
  - Hardware Redundancy
    - RAID
    - NIC teaming
    - Uninterruptible power supply (UPS)
    - Power distribution unit (PDU)
    - Dual power supplies
  - Cloud Redundancy
    - Network connection to the cloud
    - Load balancing
    - Cross-region storage replication

## Securing Endpoints

### Antivirus/Anti-Malware

- Endpoint detection and response (EDR)
  - Alarms for detected anomalies or malware infections
  - Shows up in central SIEM console
- Host-based firewalls
- Host Intrusion Detection System (HIDS)
  - Looks for suspicious activity
  - Analyzes host activity/logs
  - Detects and alerts on anomalies
    - Write to log
    - Send Notifications
      - Email
      - SMS text
      - SIEM console
- Host Intrusion System (HIPS)
  - HIDS functionality plus ability to block suspicious activity
- Next-Generation Firewall (NGFW)
  - Packet Filtering firewall
    - Up to OSI layer 4
  - Deep packet inspection firewall
    - Up to OSI layer 7
  - Intrusion detection
  - Intrusion Prevention
- Allow Lists
  - Sometimes called whitelist
  - Lists only allowed
  - Can be circumvented with DLL injection attacks
  - Can prevent users from
    - Installing and running malware
    - Making windows registry changes
- Block/Deny Lists
  - Sometimes called blacklist
  - Lists only disallowed

## Securing Data with Encryption

### Types of Encryption

- Full Disk
  - Full-Disk Encryption (FDE)
    - Ensures all data on a drive is encrypted
- Partitions
  - Partition Encryption
    - Encrypts individual partitions (sections) of a drive
    - Can have some encrypted and some unencrypted
- Files
  - File Encryption
    - Encrypts individual files
    - Protects specific sensitive files
- Volumes
  - Volume Encryption
    - Encrypts an entire volume (Logical data unit) of a drive
    - Can be done on a drive, external drive, or virtual drive
- Databases
  - Database encryption
    - Encrypts an entire database
    - Protects the whole collection of data in a database
- Records
  - Record Encryption
    - Encrypts individual entries in a database
    - Records are a single set of data in a database, like a row in the table
