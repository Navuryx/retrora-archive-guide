# Retrora Archive Guide

How to keep a copy of the Fortnite builds you own on every platform, and the **Fortnite Archive Tool** that identifies, checks and packs those copies.

## Download the Fortnite Archive Tool

| platform | download |
|---|---|
| Windows 10 and 11 (x64) | [Fortnite-Archive-Tool-windows-x64.exe](https://github.com/Navuryx/retrora-archive-guide/releases/latest/download/Fortnite-Archive-Tool-windows-x64.exe) |
| Linux and Steam Deck (x64) | [Fortnite-Archive-Tool-linux-x64-steamdeck](https://github.com/Navuryx/retrora-archive-guide/releases/latest/download/Fortnite-Archive-Tool-linux-x64-steamdeck) |
| Linux ARM64 | [Fortnite-Archive-Tool-linux-arm64](https://github.com/Navuryx/retrora-archive-guide/releases/latest/download/Fortnite-Archive-Tool-linux-arm64) |
| macOS (Apple Silicon and Intel) | [Fortnite-Archive-Tool-macos.dmg](https://github.com/Navuryx/retrora-archive-guide/releases/latest/download/Fortnite-Archive-Tool-macos.dmg) |
| Android (ARM64, in Termux) | [Fortnite-Archive-Tool-android-arm64-termux](https://github.com/Navuryx/retrora-archive-guide/releases/latest/download/Fortnite-Archive-Tool-android-arm64-termux) |

All of them are also on the [latest release](https://github.com/Navuryx/retrora-archive-guide/releases/latest), and in `downloads/`.

## In-depth guides

On Windows a build is just a folder to copy. Everywhere else there are a few more steps:

- [iOS (iPhone and iPad)](guides/ios.html): ipatool (recommended), old iTunes copies, Apple Configurator
- [Android](guides/android.html): adb, the split APKs, the downloaded game files, the tool in Termux
- [Xbox One and Series X|S](guides/xbox.html): copy to a USB drive formatted for games, and image the drive
- [PS4 and PS5](guides/playstation.html): USB Extended Storage on PS5, Back Up and Restore on PS4
- [Nintendo Switch](guides/switch.html): move to microSD and keep the card's `Nintendo` folder
- [macOS](guides/macos.html): running the tool past Gatekeeper, and the Mac builds of Fortnite
- [Linux and Steam Deck](guides/linux-steamdeck.html): Desktop Mode, Konsole, external drives

## The tool

| command | what it does |
|---|---|
| `identify <file or folder> [--json]` | Platform, container, release, version and changelist, read from the build itself |
| `manifest <folder> <file.json>` | Every file with its size, SHA-1 and SHA-256 |
| `verify <folder> <file.json>` | Missing, changed and extra files against a manifest |
| `paks <file.pak or folder>` | Files inside Unreal paks whose index is not encrypted |
| `extract <zip, ipa or apk> <folder>` | Safe unpacking |
| `pack <folder> <file.zip>` | A build and its manifest in one file |

It never decrypts: console packages, App Store copies and encrypted pak indexes are named as encrypted and left closed. The guides use only each device's own features.

## The website

`index.html`, `guides/` and `style.css` are a static site with no build step: deploy the repository root on Vercel as it is.

Retrora is unofficial and not affiliated with or endorsed by Epic Games, Apple, Microsoft, Sony or Nintendo.
