# NETWORKWALKS-Faisal-B083E-WK3-PM-FINAL-PASSWORD-CRACKING
# Penetration Testing Report: Password Cracking & Credential Security (W3-PM-FINAL)

Evaluating offline password cracking methodologies, hash extraction, and dictionary brute-force defense using John the Ripper and Networkwalks utility tools.


| **Networkwalks Cybersecurity Internship** | **B083E** | **Muhammad Faisal Rahman** | **September 2026** |

---

## 1. Liability Disclaimer
All credential testing and password recovery activities documented in this report were performed strictly on authorized lab assets, self-extracted sample hashes, and documents personally owned for educational and defensive training purposes.

---

## 2. Project Overview & Methodology
This project covers Week 3 security modules focusing on credential vulnerability assessment:
- **Module W3-PM1 (Password Cracking with JTR):** Extracted crackable hashes from encrypted PDF documents using online extraction utilities and executed dictionary/brute-force attacks using John the Ripper (CLI & Johnny GUI).
- **Module W3-PM2 (Networkwalks Tools):** Utilized custom lab web tools (`hash-calculator` and `password-cracker`) to verify hashes, run automated wordlists, and recover master credentials to capture completion flags.

---

## 3. Environment & Tools Used
| Tool / Platform | Purpose |
| :--- | :--- |
| **Kali Linux / Windows 10 Host** | Execution environment for security labs and web browsers |
| **John the Ripper / Johnny GUI** | Offline password cracking and hash analysis suite |
| **Networkwalks Hash Calculator** | PDF hash extraction tool (`pdf2john` compatible format) |
| **Wordlists (`rockyou.txt`)** | Common dictionary wordlists for brute-force evaluation |

---

## 4. Step-by-Step Implementation & Evidence

### Step 1: PDF Hash Extraction (`40060.jpg`)
Extracted crackable hashes from the password-protected document (`My Locked PDF1.pdf`) using online hash extractor tools to convert the document structure into a format compatible with cracking suites.

<img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/0fac637a-668c-4aa6-b97a-e4752710849e" />



---

### Step 2: John the Ripper & Johnny GUI Execution (`40061.jpg`)
Imported the extracted hash into Johnny (the graphical front-end for John the Ripper) and initiated a dictionary attack against the target structure.

<img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/b4a61c1d-f779-4727-8b5d-cdfd1d94816c" />



---

### Step 3: Password Cracking & Match Verification (`40064.jpg`)
Executed wordlist checks against the extracted hash until a successful match was found, recovering the plaintext password to unlock the file.

<img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/584b9f0a-2bbd-4c5a-a4e5-3ce37d74a746" />


---

### Step 4: Flag Capture & Verification (`40062.jpg`)
Unlocked the secure PDF document using the recovered password, revealing the official completion flag (`nw{cybersecurity_flag...}`).

<img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/e47f9603-ed42-49e9-a796-5428891855a8" />



---

## 5. Risk Analysis & Findings Summary
- **Weak Master Passwords:** Standard dictionary words or short PINs are easily compromised within seconds using automated wordlist attacks.
- **Offline Brute-Force Vulnerability:** Once a password hash is captured or extracted from a file, attackers can attempt offline cracking indefinitely without generating network traffic or alerting host intrusion detection systems.
- **Mitigation Recommendations:** Enforce complex multi-character passwords, implement strict account lockout policies, and utilize robust modern hashing algorithms (e.g., Argon2, bcrypt) with proper salting.

---

## 6. Troubleshooting Experience & Key Lessons
- **Issue:** Aligning hash format structures (`pdf2john` output formatting) to ensure compatibility with local and GUI-based cracking tools.
- **Resolution:** Utilized specialized web extractors and graphical wrappers (Johnny) to correctly parse hash strings and stream dictionary wordlists efficiently, resulting in successful recovery of the target credentials.
