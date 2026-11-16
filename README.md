# Password Cracking Exercise – Networkwalks Cybersecurity Program

## 📌 Overview
This repository documents a hands-on password-cracking exercise completed as part of the **Networkwalks Academy** cybersecurity training program. The objective was to recover passwords protecting a set of PDF files using offline password-cracking techniques, reinforcing core penetration testing skills around hash extraction, identification, and credential recovery.

> **Note:** Flags, cracked passwords, and original hash/PDF files are intentionally excluded from this repo, as they are used by Networkwalks to verify individual completion. This document focuses on methodology and lessons learned, not on reproducing the exercise answers.

## 🎯 Objective
- Extract the hash from password-protected PDF files
- Identify and verify the correct hash type/protection scheme
- Use dictionary and brute-force attack techniques to recover the original passwords
- Build practical familiarity with offline password-cracking tools and workflows — entirely on a Windows machine

## 🛠️ Tools Used
- **[John the Ripper (JTR) for Windows](https://www.openwall.com/john/)** – offline password cracking tool used to run dictionary and incremental attacks against extracted hashes
- **[OnlineHashCrack PDF Hash Extractor](https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php)** – used to extract the crackable hash from each password-protected PDF
- **[Networkwalks Password Cracker](https://networkwalks.com/password-cracker/)** – used during the exercise for password recovery
- **[Networkwalks Hash Calculator](https://networkwalks.com/hash-calculator/)** – used to generate/verify hash values
- **Windows 10/11 PC** – entire exercise was carried out on Windows, no Linux/Kali VM required

## 🔍 Methodology
1. **Hash Extraction** – Uploaded each password-protected PDF to the OnlineHashCrack PDF Hash Extractor tool to generate a crackable hash string in a format compatible with John the Ripper.
2. **Hash Verification** – Cross-checked the extracted hash using the Networkwalks Hash Calculator to confirm the correct hash format before attempting to crack it.
3. **Dictionary Attack** – Ran John the Ripper for Windows against the extracted hash using a wordlist, starting with common/weak password lists.
4. **Cross-Tool Cracking** – Used the Networkwalks Password Cracker tool as an additional/parallel method to recover the password.
5. **Verification** – Confirmed the recovered password by successfully opening the PDF and capturing the corresponding flag on the Networkwalks platform.

## 💡 Key Takeaways
- Weak or commonly-used passwords are cracked almost instantly with a good wordlist — reinforcing why strong, unique passwords matter in real-world document security.
- Password cracking is as much about **patience and wordlist selection** as it is about raw computing power.
- A full offline password-cracking workflow — hash extraction, verification, and cracking — can be done entirely on Windows, without needing a Linux environment.
- This exercise builds toward a core offensive-security skill: assessing credential strength as part of a broader penetration test.

## 📸 Proof of Completion
Screenshots of successful flag captures are included in `/screenshots` (redacted where necessary).

## 🎓 Program
Part of ongoing cybersecurity training with [Networkwalks Academy](https://networkwalks.com), as I transition from a background in operations management into cybersecurity and IT.

---
**Author:** Prince ([@vindicatedprince](https://github.com/vindicatedprince))
