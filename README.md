# 🔐 PASSWORD-CRACKING-JOHN-THE-RIPPER (JTR)

![Cybersecurity](https://img.shields.io/badge/Field-Cybersecurity-red)
![Tool](https://img.shields.io/badge/Tool-John%20the%20Ripper-blue)
![Tool](https://img.shields.io/badge/GUI-Johnny-green)
![Platform](https://img.shields.io/badge/Platform-Windows%2010-lightgrey)
![Lab](https://img.shields.io/badge/Lab-Educational-orange)

## 📌 Project Overview

The objective of the project was to recover the password of a protected PDF file using **John the Ripper (JTR)** and **Johnny**, the graphical interface for John the Ripper.

The practical work was performed inside an authorized **Windows 10 virtual machine running in VirtualBox**.

The project focused on understanding how password-cracking tools can be used in a controlled cybersecurity lab to test password strength and understand the importance of strong passwords.

---

## 🎯 Objectives

The main objectives of this project were to:

* Use John the Ripper to perform password recovery on a protected PDF.
* Use Johnny as the graphical interface for John the Ripper.
* Extract the password hash from the protected PDF.
* Save the extracted hash in a text file.
* Run a password-cracking attack against the hash.
* Verify the recovered password by opening the protected PDF.
* Document the practical process, challenges, and solutions.

---

## 🧪 Lab Environment

| Component              | Details                                |
| ---------------------- | -------------------------------------- |
| Host System            | Windows                                |
| Virtualization         | Oracle VirtualBox                      |
| Virtual Machine        | Windows 10                             |
| Password Cracking Tool | John the Ripper                        |
| GUI Tool               | Johnny                                 |
| PDF Hash Extractor	   | Online tool used to extract the hash from the protected PDF for John the Ripper|
| Website	               | OnlineHashCrack PDF Hash Extractor     |
| Target File            | `My Locked PDF1.pdf`                   |
| Hash File              | `hash1.txt`                            |

---

## 📂 Project Setup

The protected PDF file was transferred from the host Windows machine to the Windows 10 virtual machine using a **VirtualBox Shared Folder**.

The shared folder allowed the file to be transferred into the isolated Windows 10 lab environment.

### VirtualBox Shared Folder

<img width="1128" height="649" alt="image" src="https://github.com/user-attachments/assets/0196f3e2-46cd-4dbe-9b4b-e8617447cd51" />

The protected PDF was then available inside the Windows 10 virtual machine.

---

## 🔒 Protected PDF

The target file used for the practical exercise was:

```text
My Locked PDF1.pdf
```

The file was password protected and could not be opened without the correct password.

### 📸Locked PDF
<img width="1356" height="604" alt="image" src="https://github.com/user-attachments/assets/227a5731-cfef-4f07-b17b-732bcdffe8f5" />

This screenshot demonstrates that the PDF was password protected before performing the password-recovery process.

---

## 🔑 Convert PDF to make Hash Extraction

The protected PDF was uploaded to the OnlineHashCrack PDF Hash Extractor to extract the password hash required by John the Ripper.

The extracted hash was then copied into a text file and saved as:

```text
hash1.txt
```
The hash1.txt file was later loaded into John the Ripper for password cracking.

### 📸  Extracted Hash Text

<img width="861" height="347" alt="image" src="https://github.com/user-attachments/assets/64264904-e3f8-43c1-b604-38d3cb80ab3d" />

The hash file was then used as the input for John the Ripper.

## 📄 Creating `hash1.txt`

The extracted hash was copied into a text file named:

```text
hash1.txt
```

The file was saved in the Windows 10 virtual machine and used as the input file for John the Ripper.

### 📸 hash1.txt

<img width="1346" height="377" alt="image" src="https://github.com/user-attachments/assets/2389ce71-a01b-4506-a832-4ae849878e58" />

The screenshot should show that the hash was saved successfully.

---

## 💻 John the Ripper

John the Ripper was opened from its `run` directory.

The executable used was:

```text
john.exe
```

The installation was verified before starting the password-recovery process.

### 📸 John Setup file directory

<img width="1354" height="649" alt="image" src="https://github.com/user-attachments/assets/75a7bbd0-537d-4f75-adb1-05101d3432cc" />

---

## 🖥️ Johnny GUI

Johnny was also used to perform the same password-recovery process through a graphical interface.

The John executable was configured in Johnny before starting the attack and the hash.txt was uploaded.

### 📸 Johnny Hash File

<img width="829" height="586" alt="image" src="https://github.com/user-attachments/assets/fe70949f-55d4-4603-9f09-7f8843999181" />

---

## ▶️ Starting the Attack

A new attack was started from the Johnny interface.

### 📸 Screenshot 10 — Johnny Attack

<img width="820" height="594" alt="image" src="https://github.com/user-attachments/assets/426bbcca-f601-424c-a956-2450ebba88b0" />

---

## ✅ Password Recovery

John the Ripper/Johnny successfully recovered the password for the protected PDF.

The recovered password was then used to open the original PDF file.

### 📸 Recovered Password

<img width="1361" height="638" alt="image" src="https://github.com/user-attachments/assets/5f196f51-0d70-471d-b17d-8359ecb7063a" />

---

### 📖 Password Verification

The recovered password was entered into the protected PDF.

The PDF successfully opened, confirming that the recovered password was correct.

### 📸 PDF Successfully Opened

<img width="1365" height="693" alt="image" src="https://github.com/user-attachments/assets/58fba48e-6595-4254-a60f-6181ddc3bc45" />

---

## ⚠️ Problems Encountered & Solutions
The My Locked PDF1.pdf file was stored in the Downloads folder on the host Windows machine, but it needed to be transferred into the Windows 10 virtual machine to complete the password-cracking assignment.

Initially, the file was not accessible from inside the Windows 10 VM.

**Cause:**

The VirtualBox Shared Folder was not initially configured correctly, and the required VirtualBox Guest Additions were not available. As a result, the Windows 10 guest could not access the host machine's shared Downloads folder.

**Resolution:**

The VirtualBox Guest Additions were installed in the Windows 10 virtual machine. A Shared Folder was then configured in VirtualBox using the host machine's Downloads folder.

The shared folder was configured with:

Host Folder:
C:\Users\DELL\Downloads

Shared Folder Name:
Downloads

Options:
✓ Auto-mount
✓ Make Permanent

The shared folder was then accessed from inside the Windows 10 VM using:

\\VBOXSVR\Downloads

The My Locked PDF1.pdf file was successfully located in the shared folder and copied into the Windows 10 VM.

This resolved the file-transfer issue and allowed the protected PDF to be used for the John the Ripper password-recovery exercise.

**Result:**

The file was successfully transferred from the host Windows machine to the Windows 10 virtual machine, allowing the practical assignment to continue.

---

## 🧠 What I Learned

Through this project, I gained practical experience with:

* Password-protected PDF files.
* Password hash extraction.
* John the Ripper.
* Johnny GUI.
* Password-cracking workflows.
* Using VirtualBox Shared Folders.
* Verifying password-recovery results.
* Understanding the importance of strong passwords.
---

## 🔐 Ethical Considerations

This project was completed in an **authorized educational cybersecurity lab environment**.

Password-cracking tools should only be used against systems, files, and accounts that you own or have explicit permission to test.

The purpose of this project was to understand password security and demonstrate how weak passwords can potentially be recovered using password-auditing techniques.

---
## ⚖️ Disclaimer

This repository is for **educational and cybersecurity training purposes only**.

All activities were performed in an authorized lab environment.
---

## 👩🏽‍💻 Author

**Malehloa Seroke Cybersecurity Professional B082**

LinkedIn: [www.linkedin.com/in/malehloa-seroke]

## 📌 Project Information
Program Name: Cybersecurity at Networkwalks | Week: 03 | Project: WK3-PM1-Footprinting-Reconnaissance-with-Kali-Linux | Repository: GitHub

---


