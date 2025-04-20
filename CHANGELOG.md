# Changelog

All notable changes to **Encodex** will be documented in this file.

---

## [1.1] – 2024-04-19

### Added
- AES Export: password-protected encryption of text
- AES Import: load `.enc` files into the input box
- GUI buttons for Export AES and Import AES
- Portable version (Encodex Lite)

### Changed
- Decrypted `.enc` files now load into the **input** field (instead of output)
- Updated UI layout for feature consistency
- Internal version set to `1.1` with GitHub update support

---

## [1.0] – 2024-04-19

### Added
- Base64 + hardcoded key encryption pipeline
- Optional user-defined encryption key
- GUI with dark mode (Tkinter-based)
- Auto-update support via GitHub version check
- Installer created with Inno Setup
