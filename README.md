# FileScout

**Find any file or folder on your PC by name, instantly, as you type.** One portable EXE for Windows 10 and 11, nothing to install.
By Dialsoft LLC.

## Download

**[FileScout.exe](https://github.com/Dialsoft/filescout-releases/raw/main/FileScout.exe)**: version 1.0.0 (1.6 MB). Put it somewhere like your Desktop or `C:\Tools` (not Program Files, so it can keep itself up to date) and double-click it. Windows asks for administrator permission; say **Yes** for the fastest indexing.

Windows may show a blue "Windows protected your PC" box the first time: click **More info**, then **Run anyway**.

SHA-256: `f270996e1478f3b08730a576951013b5967a3beb7f666c6623c1f8e6299219eb`

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
