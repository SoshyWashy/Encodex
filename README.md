# Encodex

**Encodex** is a personal encryption tool I created to securely encode text in a way that’s easy for me to use, but difficult for others to reverse-engineer.

I’ve always liked the simplicity of Base64 encoding, but I didn’t like that anyone could decode my text using an online tool — or just write a quick script to do it. So I built Encodex:

- It first encodes the input using Base64
- Then, it applies an additional encryption layer using a hardcoded internal key
- Optionally, the user can provide their own encryption key to add a second layer of security

This means your encoded text will **look like normal Base64**, but **only Encodex can decode it** — and if a user key is applied, it can only be decoded with that key.

### Features
- Base64 + internal-key encryption
- Optional user key encryption (layered on top)
- AES password-protected export & import
- Desktop GUI with dark mode
- Auto-update (when enabled)
- Portable and installer versions

---

### Versions
- **Encodex Lite** – a fully portable `.exe` (no installation)
- **Encodex Installer** – a full installer version with optional config

---

###  Note
This tool is for personal use or lightweight obfuscation. While it uses AES for export, it is not intended for high-security, enterprise-grade encryption.

### Releases
See the [Releases](https://github.com/SoshyWashy/Encodex/releases) tab for downloads and changelogs.
