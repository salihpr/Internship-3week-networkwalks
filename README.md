# 🛡️ Cyber Security Internship – 3 Week Project (NetworkWalks)

![Kali Linux](https://img.shields.io/badge/Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-000000?style=for-the-badge&logo=hackaday&logoColor=red)
![John the Ripper](https://img.shields.io/badge/John%20the%20Ripper-FF0000?style=for-the-badge&logo=gnuprivacyguard&logoColor=white)
![Password Cracking](https://img.shields.io/badge/Password%20Cracking-orange?style=for-the-badge&logo=keepassxc&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

## 👨‍💻 Author

**Muhammed Salih CV**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/muhammed-salih-cv-9a292433a)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/salihpr)

---

## 📌 About This Project

This repository documents a **3-week Cyber Security Internship project** at **NetworkWalks**, focused on **PDF password hash extraction and password cracking** using **John the Ripper** on **Kali Linux**, along with NetworkWalks' own online hash & password-cracking tools.

The project covers:
- 🔍 Identifying hash types from encrypted files
- 🔓 Extracting hashes from password-protected PDF files (`pdf2john`)
- 🧨 Cracking passwords using `john` with wordlists
- ⚡ Cracking multiple PDFs at once using a `.pot` file for faster results
- 🌐 Using NetworkWalks' own online **Hash Calculator** and **Password Cracker** tools

---

## 🧰 Tools Used

| Tool | Purpose |
|------|---------|
| **Kali Linux** | Penetration testing OS environment |
| **John the Ripper (CLI)** | Offline password/hash cracking |
| **pdf2john** | Extracts crackable hash from PDF files |
| **OnlineHashCrack** | Identify hash/encryption type |
| **NetworkWalks Hash Calculator** | Custom online hash generator |
| **NetworkWalks Password Cracker** | Custom online password cracking tool |

---

## 🚀 Step-by-Step Walkthrough

### 1️⃣ Identify the Hash / Encryption Type

Before cracking anything, the encryption type of the file was identified using the online tool below:

🔗 [OnlineHashCrack – PDF Hash Extractor](https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php)

![Identify Hash](screenshorts/VirtualBox_kali%20linux_21_09_2026_15_38_06.png)

The extracted hash was copied and saved locally in a text file:

```bash
nano hash.txt
# paste the copied hash here and save
```

---

### 2️⃣ Open John the Ripper on Kali Linux

Searched for **John the Ripper** in the Kali Linux applications menu and launched it via the CLI.

![Search John the Ripper](screenshorts/VirtualBox_kali%20linux_21_09_2026_15_25_37.png)

![Open John CLI](screenshorts/VirtualBox_kali%20linux_21_09_2026_15_25_55.png)

---

### 3️⃣ Extract Hash from a Single PDF & Crack It

```bash
pdf2john <PDF_FILE> > hash.txt
john --wordlist=<PASSWORD_LIST> hash.txt
john --show hash.txt
```

![John Command Single PDF](screenshorts/VirtualBox_kali%20linux_21_09_2026_15_48_09.png)

---

### 4️⃣ Extract & Crack Multiple PDFs Together (Faster Method)

To speed up cracking when working with **two or more PDF files**, hashes were combined into a single file and cracked together using a `.pot` file:

```bash
pdf2john <PDF_FILE_1> <PDF_FILE_2> > <HASH_FILE>
john --pot=./<POT_FILE> --wordlist=<PASSWORD_LIST> <HASH_FILE>
```

![John Command Multiple PDFs](screenshorts/VirtualBox_kali%20linux_21_09_2026_15_51_52.png)

---

### 5️⃣ NetworkWalks Own Tools

**🔗 Hash Calculator:** [networkwalks.com/hash-calculator](https://networkwalks.com/hash-calculator/)

![NetworkWalks Hash Calculator](screenshorts/VirtualBox_kali%20linux_21_09_2026_15_53_01.png)

**🔗 Password Cracker:** [networkwalks.com/password-cracker](https://networkwalks.com/password-cracker/)

![NetworkWalks Password Cracker](screenshorts/VirtualBox_kali%20linux_21_09_2026_15_53_48.png)

---

## 🛠️ Troubleshooting Faced During the Project

While working with **John the Ripper** exe tool, the following issue occurred:

> ⚠️ **Issue:** The system started lagging heavily, multiple browser tabs began opening automatically on a single click, and a VPN application was silently auto-downloaded/installed in the background.
>
> ✅ **Fix / Action Taken:** Immediately disconnected the internet connection to stop the auto-downloads and unwanted redirects, closed the suspicious tabs and the auto-installed VPN, then re-checked the system before resuming work.

**⚡ Lesson Learned:** When using free/third-party online hash-cracking or password tools, always be cautious of pop-ups, redirect ads, and auto-download prompts. It's recommended to:
- Use an ad-blocker and pop-up blocker while browsing such tools
- Avoid clicking on unexpected download prompts
- Prefer running cracking tools **offline** (like John the Ripper on Kali Linux) over online services when handling sensitive files
- Monitor network activity if unexpected downloads occur, and disconnect immediately if something suspicious is detected

---

## 📂 Repository Structure

```
Internship-3week-networkwalk/
│
├── screenshorts/          # All process screenshots
├── README.md               # Project documentation (this file)
```

---

## 🤝 Thank You

Thank you for checking out this project! Feel free to connect with me on LinkedIn for feedback, collaboration, or opportunities.

**Project made by Muhammed Salih CV** ✨

[![LinkedIn](https://img.shields.io/badge/Connect%20with%20me-LinkedIn-blue?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/muhammed-salih-cv-9a292433a)
