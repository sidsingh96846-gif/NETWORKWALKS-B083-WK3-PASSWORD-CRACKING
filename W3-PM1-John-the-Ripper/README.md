# 🔐 PM1 — PDF Password Cracking with John the Ripper

## Objective

To understand how an authorized password-protected PDF can be tested against a dictionary of candidate passwords using John the Ripper on Kali Linux.

## Environment

- Operating System: Kali Linux
- Tool: John the Ripper
- Hash Extraction Tool: pdf2john
- GUI: Johnny
- Attack Type: Dictionary Attack
- Wordlist: RockYou

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
```

## Commands Used

### 1. Go to the Downloads folder

```bash
cd ~/Downloads
```

### 2. Check the files

```bash
ls
```

### 3. Extract the PDF hash

```bash
pdf2john "My-Locked-PDF1.pdf" > hash1.txt
```

### 4. View the extracted hash

```bash
cat hash1.txt
```

### 5. Run John the Ripper

```bash
john --wordlist=/usr/share/wordlists/rockyou.txt hash1.txt
```

### 6. Show the recovered password

```bash
john --show hash1.txt
```

### 7. Open Johnny GUI

```bash
johnny
```

## Result

The authorized lab PDF was tested successfully using the John the Ripper password-recovery workflow.

## Learning Outcomes

- Extracting a PDF password hash using pdf2john.
- Performing a dictionary-based password audit with John the Ripper.
- Using John the Ripper from the command line.
- Exploring the Johnny graphical interface.
- Understanding the basic PDF password-auditing workflow.

## Evidence

Screenshots from my own Kali Linux practical:

### 1. PDF hash extraction with pdf2john

![PDF hash extraction](evidence/01-pdf-hash-extraction.png)

### 2. John the Ripper dictionary attack

![John dictionary attack](evidence/02-john-dictionary-attack.png)

### 3. Recovered password with john --show

![Recovered password](evidence/03-john-show-password.png)

### 4. Johnny GUI showing the cracked PDF

![Johnny cracked result](evidence/04-johnny-cracked.png)

The screenshots are stored in the repository `evidence/` directory.

## Ethical Use

This practical is performed only on an authorized lab PDF for cybersecurity training. Password-cracking techniques must not be used against files or systems without permission.

## Author

**Siddharth Singh**
