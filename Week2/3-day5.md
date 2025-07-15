# Chapter 6

## Weak Configurations

- Biggest reason is convience
- On-premises vs Cloud solutions
- Open permissions
  - Open wireless networks
  - Guest user accounts
  - No intruder lookout settings
  - Too many file or app permissions

### Weak Configuration Example

- Linux Root Account
  - Don't sign in with root account
  - Use sudo to run privileged commands
  - Disallow remote access as root
  - Use su to temporarily switch to root

### Insecure Cryptographic Solutions

- Wi-Fi Wired Equivalent Privacy (WEP)
  - Use WPA2 or WPA3
- Digital Encryption Standard (DES)
  - Use AES
- Secure Sockets Layer (SSL)
  - Use TLS
- Transport Layer Security (TLS)
  - Not secure
    - Versions 1.0 and 1.1
  - Secure
    - Versions 1.2 and 1.3

### Change Default Settings

- IP Address
- Open port numbers
- Web server root filesystem location
  - Directory traversal attacks
- Username/password policies

## Common Attacks

### Zero-Day (0-day) Attacks

- An exploit unknown by the vendor and the public
- Zero Day Initiative (ZDI)
  - Encourages the private reporting of vulnerablities to vendors

### DNS sinkholing

- return false DNS query results

### Privilege Escalation

- Attacker acquires a higher level of access
- Example: compromising an admin account that has a weak password

### Replay attack

- Attacker intercepts and later retransmits or uses sensitive data
- Sometimes called MITM attack

### Pointer/object Dereference

- Attacker manipulates memory pointers to point to unexpected memory locations
- Normally causes software to crash (DoS Attack)

### Error Handling

- Improper handling can crash a system
- Disclosure of too much information

### Dynamic Link Library (DLL) injection

- Attacker places malicious DLL in the file system
- Legitimate running processes call malicious code within the DLL

### Resource Exhaustion

- DoS or DDoS
- Memory leaks

### Race Conditions

- Code runtime phenomenon
- Action that might occur before security control is in effect
- Based on timing

## Overflow Attacks

### Memory Injection

### Buffer Overflow

### Time of check

### Target of Evaluation

### Time of use

## Password Attacks

### Offline vs. Online

### Tools

- John the Ripper
- Cain and Abel
- Hydra

### Dictionary

- Uses common username/password files
- Tries thousands or millions of likely possibilities to login to a user account

### Brute-force

- Try every possible combination of characters
- Multiple attempts should trigger an account lockout

### Password Spraying

- Blast many accounts with a best guess common password before trying a new password
- Slower (per-user account basis) than traditional attacks
- Less likely to trigger account lockout thresholds

## Bots and Botnets

### Bot

- Single infected device under attacker control
- AKA "zombie"
- Periodically talks to command and control (C2/C&C) attacker server
  - Mitigate with IDS
  - Attacker might have directions stored in a DNS TXT Record
    - Network IDS might detect this
- Command and Control Bot
  - Bot/Zombie -> network anonymization and encryption over the Tor network -> C&C Server
    - Anonymization technique

### Botnet

- Collection of infected devices under attacker control
