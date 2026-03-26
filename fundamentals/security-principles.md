# Security Principles

## Overview

Security principles are fundamental guidelines used to design, implement, and evaluate secure systems. They help ensure that systems are resilient against threats and vulnerabilities.

These principles are often applied alongside the CIA Triad and form the basis of secure system design.

---

## Least Privilege

### Description

Users, applications, and systems should only have the minimum level of access necessary to perform their tasks.

<img width="600" height="410" alt="image" src="https://github.com/user-attachments/assets/50813d7b-5c04-4dc0-ad04-602f4e0cbca8" />


### Examples

- A user can view data but cannot modify it
- A developer has access to a test environment but not production
- An application can read files but cannot delete them

### Benefits
- Reduces the risk of misuse or accidental damage
- Limits the impact of compromised accounts

### How to implement
- Role-Based Access Control (RBAC)
- Separate admin and user accounts
- Temporary privilege elevation (just-in-time access) 

---

## Defense in Depth

### Description

Security should be implemented in multiple layers, so that if one control fails, others still provide protection.

<img width="600" height="410" alt="image" src="https://github.com/user-attachments/assets/dbcd97db-5d21-41ad-b04d-d8c31bbe31d9" />

### Examples
- Firewall + antivirus + authentication
- Password + multi-factor authentication (MFA)
- Network segmentation + monitoring

### Benefits
- Increases system resilience
- Reduces single points of failure

### Key idea
No single security mechanism should be trusted on its own.

---

## Fail Securely

### Description

Systems should default to a secure state in case of failure.

<img width="600" height="410" alt="image" src="https://github.com/user-attachments/assets/1b7a8acb-1354-47e6-83e8-6582524925e7" />


### Examples
- Access is denied if authentication fails
- A system error results in restricted access, not open access

### Benefits
- Prevents unintended or unauthorized access
- Protects systems during unexpected errors

### Common mistake
Designing systems that “fail open” instead of “fail closed”.

---

## Separation of Duties

### Description
Critical tasks should be divided among multiple individuals or systems.

<img width="600" height="410" alt="image" src="https://github.com/user-attachments/assets/773e5783-870a-4d29-b3e7-3e1c343840dd" />


### Examples
- One person approves a transaction, another executes it
- A developer writes code, another reviews and deploys it

### Benefits
- Reduces the risk of fraud and abuse
- Prevents a single point of control 

---

## Security by Design

Security should be considered from the beginning of system design, not added later.

<img width="600" height="410" alt="image" src="https://github.com/user-attachments/assets/5c3675cb-9f4c-4dd2-98d3-229d1c9df3e1" />

### Example:
- Designing authentication and authorization early
- Performing threat modeling during architecture design
- Using secure coding practices

### Benefits
- Stronger and more reliable systems
- Lower cost compared to fixing security issues later

---

## Zero-Trust

### Description
The Zero Trust model assumes that no user, device, or system should be trusted by default, even if they are inside the network perimeter.

<img width="600" height="410" alt="image" src="https://github.com/user-attachments/assets/747829ff-7f69-484d-8b98-d114c21582b6" />

# “Never trust, always verify”

### Key Concepts
- Continuous authentication and authorization
- Verification based on identity, device, and context
- Micro-segmentation of networks
- Least privilege access enforcement

### Examples
- A user inside the corporate network must still authenticate via MFA
- Access to a resource is re-evaluated on every request
- A device must meet security requirements (e.g., updated OS) before access

### Benefits
- Reduces risk of lateral movement inside networks
- Limits impact of compromised accounts
- Strong protection against insider threats
  
---
## Complete Mediation

### Description
Every access to every resource must be checked and authorized, not just the first time.

<img width="600" height="410" alt="image" src="https://github.com/user-attachments/assets/d1ae24f9-a36d-429e-a6a9-8fbecf116031" />

# No caching of permissions without validation.

### Key Concepts
- Every request = authorization check
- No implicit trust after initial login
- Enforcement at every layer (API, DB, system)

### Examples
- API verifies a token on every request, not just at login
- File access is checked each time, not cached
- Middleware validates permissions per operation

### Common mistake
- “User logged in once → give full access forever” 

### Benefits
- Prevents privilege escalation
- Stops attackers using stale sessions
- Ensures consistent enforcement of policies

---
## Economy of Mechanism

### Description
Security mechanisms should be as simple as possible, minimizing complexity.


<img width="600" height="410" alt="image" src="https://github.com/user-attachments/assets/eac4d1a3-7ef6-4f3d-b215-1042d34ebd7d" />


# “Keep it simple, keep it secure”

### Key Concepts
- Smaller codebase = fewer bugs
- Simpler logic = easier to audit
- Avoid unnecessary features

### Examples
- Simple authentication flow instead of custom complex logic
- Using well-tested libraries instead of writing your own crypto
- Clear and minimal access control rules

### Why complexity is dangerous
- Harder to test and verify
- More edge cases → more vulnerabilities
- Easier to misconfigure

### Benefits
- Easier auditing and maintenance
- Lower risk of hidden vulnerabilities
- Faster incident response
- Real-world insight

Most critical vulnerabilities come from: verly complex systems, not simple ones







---


## Key Takeaways

- Security principles guide how systems should be designed  
- They reduce vulnerabilities and improve system resilience  
- Applying multiple principles together increases effectiveness  

---

## Notes

These principles are widely used in cybersecurity frameworks and best practices across industries.
