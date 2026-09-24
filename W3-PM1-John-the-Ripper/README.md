
# 🔐 PM1 — PDF Password Cracking with John the Ripper

## Objective

To understand the process of recovering the password of an authorized password-protected PDF using John the Ripper.

## Environment

- Operating System: Kali Linux
- Tool: John the Ripper
- Hash Extraction Tool: pdf2john
- GUI: Johnny
- Attack Type: Dictionary Attack

## Lab Workflow

```text
Password-Protected PDF
        ↓
     pdf2john
        ↓
    PDF Hash
        ↓
John the Ripper
        ↓
Dictionary Attack
        ↓
 Password Recovery
