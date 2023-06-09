# PGP Encryption in Python using GnuPG

This repository shows how to integrate file encryption and decryption using OpenPGP standard in Python. Here Symmetric encryption is used.

## OpenPGP

OpenPGP (Pretty Good Privacy) is a free and open-source encryption standard used to secure email communication, files, and other data. It provides end-to-end encryption, which means that the data is encrypted on the sender's device and can only be decrypted by the intended recipient with their private key. OpenPGP uses public key cryptography to encrypt and decrypt data, and digital signatures to verify the authenticity and integrity of the data. It is widely used by individuals, businesses, and organizations to protect sensitive information and ensure secure communication.

Link: https://www.openpgp.org

## GnuPG

GnuPG (GNU Privacy Guard) is a free and open-source software application used for encrypting, decrypting, and signing data, including files, email messages, and other types of digital communication. It provides a secure and private way to protect sensitive information and ensure the authenticity and integrity of digital data. GnuPG is based on the OpenPGP standard and supports various encryption algorithms, such as AES, RSA, and DSA. It is available for a wide range of operating systems, including Linux, macOS, and Windows, and can be integrated with various email clients and other software applications. GnuPG is widely used by individuals, businesses, and organizations to protect their sensitive information and ensure secure communication.

Link: https://gnupg.org

## Python-GnuPG

Python-GnuPG is a Python module that provides a high-level interface for working with GnuPG (GNU Privacy Guard) in Python. It allows developers to perform various GnuPG operations, such as encryption, decryption, signing, and verifying digital signatures, directly from Python scripts. Python-GnuPG is built on top of the GnuPG software and provides a more user-friendly and Pythonic way to interact with GnuPG. It supports both synchronous and asynchronous operations, and can be used with Python 2 and 3. Python-GnuPG is widely used by developers who need to integrate GnuPG functionality into their Python applications, such as email clients, backup software, and other security-related applications.

Library Documentation: https://gnupg.readthedocs.io/en/latest

## Usage

### Encrypt

```
with open(path, 'rb') as file:
        encryptionStatus = gpg.encrypt_file(file, recipients=Any, symmetric=True, passphrase=symmetricKey, output=path + ".encrypted", armor=False, extra_args=extra_args_encryption)

```

### Decrypt

```
with open(encryptedFilePath, 'rb') as file:
        decryptionStatus = gpg.decrypt_file(file, passphrase=symmetricKey, output=path + ".decrypted")
```

## License

MIT License

Copyright (c) 2023 Sumit Sahoo

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

