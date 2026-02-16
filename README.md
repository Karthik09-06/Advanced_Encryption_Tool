# AES-256 File Encryption Tool

## Overview

A secure file encryption and decryption tool developed using AES-256 (CBC mode) with password-based key derivation. The application enables users to encrypt and decrypt files of any format while preserving the original file extension. A simple graphical interface ensures ease of use and accessibility.

---

## Features

* AES-256 encryption in CBC mode
* Password-based key derivation using PBKDF2 with SHA-256
* Random salt and initialization vector (IV) for each encryption
* PKCS7 padding with error detection
* Automatic recovery of original file extension
* Error handling for incorrect password or corrupted file
* Supports multiple file formats (images, PDFs, videos, documents, etc.)
* Graphical user interface built using Tkinter

---

## Technology Stack

* Python
* Cryptography library
* Tkinter (GUI)

---

## Project Structure

```
aes_encryption_tool/
├── aes_tool.py     # Core encryption and decryption logic
├── gui.py          # Graphical user interface
└── README.md       # Project documentation
```

---

## Installation and Setup

### 1. Clone the Repository

```
git clone https://github.com/Karthik09-06/Advanced_Encryption_Tool.git
cd Advanced_Encryption_Tool
```

### 2. Install Dependencies

```
pip install cryptography tkinterdnd2
```

### 3. Run the Application

```
python gui.py
```

---

## Working Mechanism

### Encryption Process

1. User selects a file and enters a password.
2. A 256-bit key is derived using PBKDF2 with a random salt.
3. File is padded and encrypted using AES-256 (CBC mode).
4. Output format:
   `[salt][IV][extension][encrypted_data]`
5. Encrypted file is saved as a `.bin` file.

### Decryption Process

1. User selects the encrypted `.bin` file.
2. Password is entered for authentication.
3. Salt, IV, and extension metadata are extracted.
4. File is decrypted and padding is removed.
5. Original file is restored with the correct extension.

---

## Security Considerations

* Uses industry-standard AES-256 encryption
* Unique salt and IV generated for every encryption
* Passwords are not stored or logged
* Decryption requires the correct password
* Ensures confidentiality and data integrity

---

## Author

Karthik G
MCA (Gen), Jain University

GitHub: https://github.com/Karthik09-06
LinkedIn: https://www.linkedin.com/in/karthik-g-44957a354/
