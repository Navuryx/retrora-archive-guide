# Retrora Archive Guide

How to keep a copy of the Fortnite builds you own on every platform, and the **Fortnite Archive Tool** that identifies, checks and packs those copies.

- **Website:** `index.html` (static, no build step; deploy the repository root on Vercel as-is).
- **Downloads:** `downloads/`. The tool for Windows, Linux and Steam Deck, Linux ARM, macOS (Apple Silicon and Intel), and Android (Termux).
- **Guides:** on the site. PC, Mac, Linux and Steam Deck; iOS (ipatool recommended); Android; Xbox; PlayStation; Switch.

## The tool

| command | what it does |
|---|---|
| `identify <file or folder> [--json]` | Platform, container, release, version and changelist, read from the build itself |
| `manifest <folder> <file.json>` | Every file with its size, SHA-1 and SHA-256 |
| `verify <folder> <file.json>` | Missing, changed and extra files against a manifest |
| `paks <file.pak or folder>` | Files inside Unreal paks whose index is not encrypted |
| `extract <zip, ipa or apk> <folder>` | Safe unpacking |
| `pack <folder> <file.zip>` | A build and its manifest in one file |

It never decrypts: console packages, App Store copies and encrypted pak indexes are named as encrypted and left closed.

Retrora is unofficial and not affiliated with or endorsed by Epic Games.
