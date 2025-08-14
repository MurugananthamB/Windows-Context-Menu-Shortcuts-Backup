# Windows Context Menu Shortcuts Backup

This repository contains **Windows Registry (.reg) backup files** for restoring useful right-click context menu shortcuts on Windows 11.

## 📌 Included Shortcuts
- **Open with VS Code** – Opens the selected folder/file in Visual Studio Code.
- **Open Git Bash here** – Opens Git Bash terminal in the selected folder.
- **Open with Cursor** – Opens the selected folder/file in Cursor IDE.

## 🛠️ Usage
1. **Double-click** the `.reg` file to merge into Windows Registry.
2. Click **Yes** when prompted for confirmation.
3. **Restart Windows Explorer**:
   - Press `Ctrl + Shift + Esc` to open Task Manager.
   - Find **Windows Explorer** → Right-click → Restart.

## 💡 Notes
- These backups are tested on **Windows 11 (22H2+)**.
- If you reinstall or update Windows, you can restore all shortcuts instantly by running the `.reg` file.
- For **VS Code**, the registry points to:
```
C:\Program Files\Microsoft VS Code\bin\code.cmd
```
This ensures correct handling of folder names with spaces or special characters.

## 📂 Backup Contents
```

reg-backups/
├── context-menu-backup.reg   # Full backup for all shortcuts
├── vscode-context.reg        # VS Code context menu only
├── gitbash-context.reg       # Git Bash context menu only
└── cursor-context.reg        # Cursor IDE context menu only

```

## 🔄 Updating the Backup
1. Open **Registry Editor** (`regedit`).
2. Export the following keys:
   - `HKEY_CLASSES_ROOT\Directory\Background\shell\VSCode`
   - `HKEY_CLASSES_ROOT\Directory\shell\VSCode`
   - `HKEY_CLASSES_ROOT\Directory\Background\shell\git_shell`
   - `HKEY_CLASSES_ROOT\Directory\shell\git_shell`
3. Replace old `.reg` files with the new exports.
4. Commit and push changes to this repository.

---

**Author:** MURUGANANTHAM  
**Last Updated:** August 2025
