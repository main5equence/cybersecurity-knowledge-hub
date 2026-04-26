# IoT Security Basics

## Overview

The Internet of Things (IoT) refers to a network of interconnected devices that collect and exchange data.

IoT security focuses on protecting these devices and the data they process from unauthorized access and attacks.

<img width="1021" height="674" alt="image" src="https://github.com/user-attachments/assets/fc54f82c-4560-4153-a75d-2fcd4fa05e6b" />


---

## What is IoT?

IoT includes devices such as:
- Smart home devices (e.g., cameras, thermostats)  
- Wearables (e.g., smartwatches)  
- Industrial sensors  

These devices often communicate over the internet and operate with minimal human interaction.

---

## Common IoT Security Challenges

- Limited device resources (low processing power)  
- Weak or default passwords  
- Lack of regular updates  
- Insecure communication  

---

## Common Attack Vectors

### Device Hijacking

Unauthorized takeover of a device by an attacker.

How it happens:
- weak or default credentials
- vulnerabilities in firmware
- lack of security updates

What attackers can do:
- change device configuration
- use the device as an entry point into the network
- disrupt or disable the device (DoS)

Example:
Compromising an IP camera and using it for surveillance or further attacks.

 

### Botnets (e.g., Mirai botnet)

Large networks of infected devices controlled by an attacker.

How it works:
- malware scans the internet for vulnerable IoT devices
- exploits default credentials
- automatically infects devices and adds them to a botnet

Used for:
- DDoS attacks
- spam distribution
- spreading additional malware

Why IoT is vulnerable:
- weak security
- lack of updates
- massive number of devices


### Unauthorized Access

Gaining access to systems or devices without permission.

How it happens:
- weak or stolen credentials
- lack of multi-factor authentication (MFA)
- misconfigurations (e.g., open ports)

Impact:
- access to sensitive data
- manipulation of systems
- privilege escalation

In OT environments:
Can lead to changes in physical processes (e.g., industrial operations).

### Data Interception

Capturing data as it travels between devices.

How it happens:
- unencrypted communication (HTTP, Telnet)
- Man-in-the-Middle (MITM) attacks
- network sniffing

What can be intercepted:
- login credentials
- operational data
- control commands

Risks:
- data theft
- manipulation of communication
- potential system takeover



---

## Best Practices

- Change default credentials  
- Keep devices updated  
- Use secure communication protocols  
- Segment networks  

---

## Key Takeaways

- IoT devices increase the attack surface  
- Security is often overlooked in IoT environments  
- Proper configuration and updates are critical  

---

## Notes

IoT security is a growing field due to the rapid expansion of connected devices.
