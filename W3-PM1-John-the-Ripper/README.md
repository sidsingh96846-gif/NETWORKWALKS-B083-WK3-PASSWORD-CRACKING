# 🔐 PM1 — PDF Password Cracking with John the Ripper

## 🎯 Objective

To test the password of the authorized Networkwalks lab PDF using **John the Ripper** on Kali Linux and understand the basic dictionary-attack workflow.

## 🖥️ Environment

- OS: Kali Linux
- Target: `My Locked PDF1.pdf`
- Hash extraction: `pdf2john`
- Cracking tool: John the Ripper
- Wordlist: RockYou
- GUI: Johnny
- Attack type: Dictionary attack

## 🔄 Workflow

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
        ↓
      Johnny GUI
```

## 💻 Commands Used

### 1. Locate the lab files

```bash
ls /media/sf_network_walks_week_3
```

### 2. Extract the PDF hash

```bash
pdf2john "/media/sf_network_walks_week_3/My Locked PDF1.pdf" > hash1.txt
cat hash1.txt
```

### 3. Check the RockYou wordlist

```bash
ls /usr/share/wordlists/rockyou.txt
```

### 4. Run the dictionary attack

```bash
john --wordlist=/usr/share/wordlists/rockyou.txt hash1.txt
```

### 5. Verify the recovered password

```bash
john --show hash1.txt
```

### 6. Open Johnny

```bash
johnny
```

## ✅ Result

The authorized lab PDF password was successfully recovered as:

```text
good-luck
```

The result was verified both from the John CLI output and the Johnny GUI.

## 🧠 Learning Outcomes

- Extracting a crackable PDF hash with `pdf2john`
- Using a dictionary wordlist with John the Ripper
- Verifying recovered passwords with `john --show`
- Using Johnny as a graphical interface for John
- Understanding why password strength matters

## ⚠️ Ethical Use

This practical was performed only against the authorized lab PDF supplied for cybersecurity training. These techniques must not be used against files or systems without permission.

## 👨‍💻 Author

**Siddharth Singh**
