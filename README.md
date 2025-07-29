# RSA4096 Encryption/Decryption Tool

This is a Windows batch‑script tool based on OpenSSL, providing RSA‑4096 encryption/decryption capabilities for both text and files, with a user‑friendly menu interface.

**Read this in other languages: [Chinese](https://github.com/ttwe77/RSA4096-EncryptionDecryption-Tool/blob/main/README_ch)**

## Main Features

- 🔐 RSA‑4096 encryption/decryption
- 📝 Text encryption (Base64 output)
- 📄 Text decryption (Base64 input)
- 📁 File encryption/decryption
- 🔑 Key management (generate, view, copy)
- 🌐 UTF‑8 encoding support

## System Requirements

1. **Windows OS**
2. **OpenSSL** – [Download here](https://slproweb.com/products/Win32OpenSSL.html)

## Installation & Usage

1. Download and install OpenSSL (if not already installed)
2. Download 'RSA***.bat' from the releases
3. Double-click to run RSA.bat file

## Usage Guide

### Main Menu

```
===============================
  RSA‑4096 Encryption/Decryption Tool
===============================
Current directory: [your folder]
1. Encrypt text (Base64 output)
2. Decrypt text (Base64 input)
3. Encrypt file
4. Decrypt file
5. View/Copy public key
6. Generate new key pair (with passphrase)
0. Exit
```

### Feature Details

#### 1. Encrypt Text

- Select a public‑key file (from `public_keys` directory)
- Enter the plaintext to encrypt
- Outputs the encrypted result as Base64
- Optionally copy to clipboard

#### 2. Decrypt Text

- Select a private‑key file (from `private_keys` directory)
- Enter the Base64‑encoded ciphertext
- Enter the private‑key passphrase
- Displays the decrypted plaintext
- Optionally copy to clipboard

#### 3. Encrypt File

- Select a public‑key file
- Enter the full path of the file to encrypt
- Produces an encrypted file with a `.enc` extension

#### 4. Decrypt File

- Select a private‑key file
- Enter the full path of the `.enc` file
- Enter the private‑key passphrase
- Produces a decrypted file with a `.dec` extension

#### 5. View/Copy Public Key

- Lists all public‑key files
- View the contents of a public key
- Optionally copy to clipboard

#### 6. Generate New Key Pair

- Enter an identifier (letters, numbers, underscores)
- Set a private‑key passphrase (minimum 4 characters, no special characters)
- Generates the private key in `private_keys`
- Generates the public key in `public_keys`

## Directory Structure

When run, the tool will automatically create:

- `private_keys` – stores private‑key files
- `public_keys`  – stores public‑key files

## Notes & Limitations

1. **Key Security**
	- Keep private keys safe and never share them
	- Public keys may be freely distributed
2. **Passphrase Requirements**
	- At least 4 characters
	- Avoid special characters
	- Use a strong passphrase to protect private keys
3. **File‑Size Limitations**
	- RSA‑4096 can encrypt up to ~446 bytes at once
	- Suitable only for small files or text
	- After decryption, manually remove the `.dec` extension if desired
4. **Special Character Handling**
	- Avoid special characters in filenames and passphrases
	- Text encryption fully supports UTF‑8

## Examples

### Encrypting Text

1. Choose menu option 1
2. Select your public key
3. Enter `"Hello World"`
4. Receive the Base64‑encoded ciphertext
5. Optionally copy it to clipboard

### Decrypting a File

1. Choose menu option 4
2. Select your private key
3. Enter the path `D:\data\secret.txt.enc`
4. Enter your private‑key passphrase
5. Obtain the decrypted file `D:\data\secret.txt.dec`

## Disclaimer

This tool provides basic encryption functionality but does **not** guarantee absolute security. For critical data, please use a professional encryption solution. The author is not responsible for data loss or security vulnerabilities.

## Recommended Alternative

- [GnuPG](https://gnupg.org/)
