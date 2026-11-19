# FileScout

**Find any file or folder on your PC by name, instantly, as you type.** For Windows 10 and 11, as an installer or a single portable EXE.
By Dialsoft LLC.

## Download

FileScout 1.0.1 comes two ways. Both are the same program.

- **[FileScout-Setup.exe](https://github.com/Dialsoft/filescout-releases/raw/main/FileScout-Setup.exe)**: the installer (0.7 MB). Adds FileScout to the Start menu and to Windows "Installed apps", with an uninstaller. It asks whether to install for **just you** (no administrator needed) or for **everyone who uses the PC** (asks for an administrator).
- **[FileScout.exe](https://github.com/Dialsoft/filescout-releases/raw/main/FileScout.exe)**: the portable copy (1.6 MB). Nothing to install: put it somewhere like your Desktop or `C:\Tools` (not Program Files, so it can keep itself up to date) and double-click it.

When FileScout starts, Windows asks for administrator permission; say **Yes** for the fastest indexing.

**For IT / remote deployment:** `FileScout-Setup.exe /S` installs silently for the account running it; add `/ALLUSERS` (run as administrator) to install for everyone, `/DESKTOP` for a Desktop shortcut, and `/NOUPDATES` to switch off automatic update checks. `"C:\Program Files\FileScout\Uninstall.exe" /S` removes it silently.

Windows may show a blue "Windows protected your PC" box the first time: click **More info**, then **Run anyway**.

SHA-256: FileScout-Setup.exe `44ba557ffe6cfc15a135484f7f809604817ff1690ccb81b34831bfe400821b11` · FileScout.exe `20e9d2984f4bd00db8759686fed1e50beb4b06f60233b7e9af642cdd00d7dfe6`

## Learn FileScout

- **[User Guide](GUIDE.md)**: everything FileScout can do, with pictures.
- In the program: **Help > How to Use** (F1) and **Help > Search Tricks**.

## Why it's fast

- Reads each NTFS drive's file table (the MFT) directly, with several threads at once: about 1.4 million files in around 11 seconds on a cloud test server, where Everything took about 15.
- Every search uses all of your PC's CPU threads, with an SSE2 name scanner, and results come out already sorted.
- Notices new, renamed and deleted files within a quarter of a second (Everything checks once a second), including every hard link.
- Saves its index when it closes, so the next start takes a fraction of a second.

## What it does

- Search as you type, with words shown in bold in the results; the same search tricks as Everything (AND, `|` OR, `!` NOT, wildcards, `ext:`, `size:`, `dm:`/`dc:` dates, `file:`, `folder:`, `parent:`, `attrib:`, `regex:`, `case:`, `ww:`, `path:`)
- Extras: `dupe:` and `sizedupe:` to find duplicates, `empty:` for empty folders, and a Tools tab with ready-made searches (Same Names, Same Size, Largest Files, Largest Folders, Recent Changes, Empty Folders, Most Opened, Speed Test)
- Folder sizes for every folder, always up to date
- Windows' own right-click menu; drag results into Explorer or an email; copy files or paths; Recycle Bin
- Works without administrator rights too (scans folders, then watches for changes); indexes USB drives and network shares
- Tray icon, hotkey (Ctrl+Alt+F), start with Windows, export (CSV / TXT / Everything EFU)
- Keeps itself up to date automatically (checks at start and every 6 hours; you choose when to install)

© 2026 Dialsoft LLC, Marc Frega, Wharton NJ. Built with Claude by Anthropic.
