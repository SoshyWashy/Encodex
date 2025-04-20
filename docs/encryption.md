# Encodex Encryption Breakdown

This document explains how Encodex encodes and decodes text securely, while keeping the process invisible to external decoders.

---

## Encoding Pipeline

1. **Base64 Encode**  
   The input text is first encoded using Base64. This step keeps the result visually similar to common encoding schemes.

2. **Shift Encrypt (Internal Key)**  
   The Base64 string is then encrypted character-by-character using a hardcoded key and a safe printable range (ASCII 32–126).

3. **Optional User Key Layer**  
   If a user provides a custom key, another shift cipher is applied on top of the already-encrypted text.

4. **Obfuscation**  
   The encrypted string is obfuscated by inserting random characters at regular intervals. The interval is stored as a prefix (e.g. `#4#`) and removed on decode.

---

## AES Export/Import

Encodex also supports secure export using **AES encryption** (Fernet):

- A password is converted into a 256-bit AES key using SHA-256
- The text is encrypted and saved to a `.enc` file
- Users must enter the same password to decrypt the file

This method ensures strong protection for exported strings but is optional.

---

## Why Not Just Base64?

Base64 is easy to reverse — anyone can decode it using a browser or simple script. Encodex disguises your data by adding:
- Internal key encryption
- Optional user key
- Obfuscation
- AES-based file encryption (for sharing or storage)

---

Encodex keeps your text safe from casual inspection while remaining easy and quick to use for you.
