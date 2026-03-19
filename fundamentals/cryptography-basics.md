# Cryptography Basics

## Overview

Cryptography is the practice of securing information by transforming it into an unreadable format, accessible only to authorized parties.

It plays a key role in protecting data confidentiality, integrity, and authenticity.

---

## Encryption

Encryption converts readable data (plaintext) into an unreadable format (ciphertext).

### Types:
- Symmetric encryption (same key)  
- Asymmetric encryption (public and private keys)  

### Example:
- HTTPS uses encryption to secure communication  

---

## Decryption

Decryption is the process of converting ciphertext back into readable data using a key.

---

## Hashing

Hashing transforms data into a fixed-length value (hash).

### Features:
- One-way function (cannot be reversed)  
- Same input always produces the same output  

### Example:
- Password storage  

---

### Example (Python – SHA-256)

```python
import hashlib

password = "my_secure_password"
hashed = hashlib.sha256(password.encode()).hexdigest()

print("Hashed password:", hashed)
```

```
Hashed password: 5e884898da28047151d0e56f8dc6292773603d0d6aabbddf...
```

### Important Note: Hashing alone is not enough for password security.

Better approach: Use salting. Use secure algorithms like bcrypt or Argon2

```python
import hashlib
import os

password = "my_secure_password"
salt = os.urandom(16)

hashed = hashlib.sha256(salt + password.encode()).hexdigest()

print("Hashed password with salt:", hashed)
```
```
Salt: b'\x93\xab\x1f\x8c...'
Hashed password with salt: a3f5d7c9e8b1...
```

### Bcrypt (Secure Password Hashing)
Bcrypt is a hashing algorithm specifically designed for storing passwords securely.

Advantages:
- Built-in salting
- Resistant to brute-force attacks
- Adjustable complexity (cost factor)

```python
import bcrypt

password = b"my_secure_password"

hashed = bcrypt.hashpw(password, bcrypt.gensalt())

print("Hashed password:", hashed)

# Verify password
if bcrypt.checkpw(password, hashed):
    print("Password is correct")
```
```
Hashed password: b'$2b$12$KIXQ...'
Password is correct
```

### AES Encryption (Symmetric Encryption)

AES (Advanced Encryption Standard) is widely used for encrypting data.

```python
from Crypto.Cipher import AES
from Crypto.Random import get_random_bytes

# Generate key
key = get_random_bytes(16)

# Create cipher
cipher = AES.new(key, AES.MODE_EAX)

data = b"secret data"

ciphertext, tag = cipher.encrypt_and_digest(data)

print("Ciphertext:", ciphertext)

# Decrypt
cipher_dec = AES.new(key, AES.MODE_EAX, nonce=cipher.nonce)
plaintext = cipher_dec.decrypt(ciphertext)

print("Decrypted:", plaintext)
```

```
Ciphertext: b'\x8f\x9a\x12...'
Decrypted: b'secret data'
```

### Mini Password Cracking Demo (Dictionary Attack)

This demonstrates how weak passwords can be cracked using a simple dictionary attack.

```python
import hashlib

# Target hashed password
target_hash = hashlib.sha256("password123".encode()).hexdigest()

# Simple password list
wordlist = ["123456", "password", "password123", "admin"]

for word in wordlist:
    hashed = hashlib.sha256(word.encode()).hexdigest()
    if hashed == target_hash:
        print("Password found:", word)
        break
```
```
Password found: password123
```

## Security Insight

- Weak passwords can be cracked quickly
- Hashing alone is not enough without salting
- Strong passwords + bcrypt significantly increase security


## Digital Signatures
Digital signatures verify the authenticity and integrity of data.

Example:
- Signed emails
- Software verification


## Common Threats

- Weak encryption algorithms
- Poor key management
- Brute-force attacks
- Dictionary attacks


## Key Takeaways

- Cryptography protects sensitive data
- Hashing is essential for password security
- Bcrypt improves resistance to attacks
- Encryption protects data in transit and storage
- Weak passwords remain one of the biggest risks

## Notes

Cryptography is a fundamental component of modern cybersecurity systems and is widely used in communication, authentication, and data protection.


















