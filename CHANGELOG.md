## 1.0.1 (2026-11-18)
- New: FileScout now also comes as an installer, FileScout-Setup.exe. It asks whether to install for just you (no administrator needed) or for everyone on the PC, adds FileScout to the Start menu (and the Desktop if you like) and to Windows' Installed apps list, with an uninstaller.
- Installed copies update themselves through the installer, so the Installed apps list always shows the right version.
- The installer and uninstaller close a FileScout that's running in the tray by themselves (it saves its index first). Uninstalling also removes the start-with-Windows entry and the saved index, and asks before removing your settings.
- For IT: FileScout-Setup.exe /S installs silently; add /ALLUSERS (as administrator) for everyone, /DESKTOP for a Desktop shortcut, /NOUPDATES to switch off automatic update checks.
- The portable FileScout.exe is still available and works exactly as before.

## 1.0.0 (2026-11-18)
- First release of FileScout: find any file or folder on your PC by name, instantly, as you type.
- Reads each NTFS drive's file table directly (with administrator rights), using several threads at once: millions of files indexed in seconds.
- Every search uses all of your PC's CPU threads at once, with a fast SSE2 name scanner. Results come out already sorted.
- Live: new, renamed and deleted files show up within a quarter of a second (FileScout reads each drive's change journal 4 times a second).
- Folder sizes are shown for every folder, always up to date.
- The index is saved when FileScout closes, so the next start is instant - it only reads what changed since.
- Search syntax like Everything's: AND, | for OR, ! for NOT, wildcards, ext:, size:, dm: / dc: dates, file:, folder:, parent:, attrib:, regex:, case:, ww:, path:.
- Extras: dupe: and sizedupe: to find duplicates, empty: for empty folders, and a Tools tab with ready-made searches (Same Names, Same Size, Largest Files, Largest Folders, Recent Changes, Empty Folders, Most Opened).
- The words you type are shown in bold in the results. Right-click gives Windows' own menu; drag results straight into Explorer or an email.
- Works without administrator rights too (scans folders, then watches for changes), and indexes USB drives and network shares (Index tab > Add Folder).
- Lives in the tray with a hotkey (Ctrl+Alt+F), can start with Windows (no permission box at sign-in), and updates itself.
