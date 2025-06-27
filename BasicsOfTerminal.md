# Basics of Terminal

A cross-platform collection of essential terminal commands for navigating and managing files, folders, and systems.

> ⚠️ Notes:
> - `CMD` refers to Windows Command Prompt  
> - `PowerShell` is a more advanced shell on Windows  
> - `Unix/Linux/macOS` refers to Bash-like environments  
> - Commands marked with 🔒 may require admin or elevated privileges

---

## 📁 Navigation Commands

**1. Show Current Directory**  
- CMD / PowerShell / Unix: `pwd`

**2. List Files and Folders**  
- CMD: `dir`  
- PowerShell / Unix: `ls`  
- PowerShell (detailed): `ls -Force`

**3. Navigate to a Folder**  
- All: `cd folderName`

**4. Go Back One Directory**  
- All: `cd ..`

**5. Go Back Two or More Directories**  
- All: `cd ../..`

**6. Go to a Specific Path**  
- All: `cd path/to/folder`

**7. Go to Home Directory**  
- PowerShell: `cd ~`  
- Unix/macOS: `cd ~`  
- CMD: `cd %HOMEPATH%`

---

## 📂 File & Folder Management

**8. Create a New Folder**  
- CMD: `mkdir folderName`  
- PowerShell / Unix: `mkdir folderName`

**9. Create Nested Folders**  
- CMD: `mkdir parent\child\grandchild`  
- PowerShell / Unix: `mkdir -p parent/child/grandchild`

**10. Create a File**  
- CMD: `echo. > filename.txt`  
- PowerShell / Unix: `touch filename.txt`

**11. View File Content**  
- CMD / PowerShell: `type filename.txt`  
- Unix/macOS: `cat filename.txt`

**12. Rename or Move a File**  
- CMD / PowerShell / Unix: `mv old.txt new.txt`

**13. Move File to Another Folder**  
- CMD / PowerShell / Unix: `mv file.txt folderName/`

**14. Copy a File**  
- CMD / PowerShell / Unix: `copy file.txt copy.txt` (CMD uses `copy`, Unix uses `cp`)

**15. Copy to Another Folder**  
- CMD: `copy file.txt folderName\`  
- Unix/macOS: `cp file.txt folderName/`

**16. Delete a File**  
- CMD / PowerShell: `del file.txt`  
- Unix/macOS: `rm file.txt`

**17. Delete a Folder and Its Contents**  
- CMD / PowerShell: `rmdir /s /q folderName`  
- Unix/macOS: `rm -rf folderName/`

---

## 👤 User & System Info

**18. Show Current User**  
- All: `whoami`

**19. Show Current Date and Time**  
- CMD: `date /T` and `time /T`  
- PowerShell: `Get-Date`  
- Unix/macOS: `date`

**20. Show System Uptime**  
- CMD: `systeminfo` → look for "System Boot Time"  
- PowerShell: `Get-Uptime`  
- Unix/macOS: `uptime`

**21. Show Logged In Users**  
- CMD: `query user`  
- Unix/macOS: `who`

---

## 🧰 Search & History

**22. Search for a File by Name**  
- PowerShell: `Get-ChildItem -Recurse -Filter "filename.txt"`  
- Unix/macOS: `find . -name "filename.txt"`

**23. Search Inside a File**  
- PowerShell: `Select-String -Path filename.txt -Pattern "text"`  
- Unix/macOS: `grep "text" filename.txt`

**24. Show Command History**  
- CMD / PowerShell: Use up/down arrows or `doskey /history`  
- Unix/macOS: `history`

---

## 🧹 Miscellaneous

**25. Clear the Terminal Window**  
- CMD: `cls`  
- PowerShell / Unix: `clear`  
- Shortcut (most): `Ctrl + L`

**26. Repeat Last Command**  
- Unix/macOS: `!!`  
- CMD: Up arrow  
- PowerShell: Up arrow

**27. Run Command as Admin / Superuser 🔒**  
- CMD: Run terminal as Administrator  
- PowerShell: Use **Run as Administrator**  
- Unix/macOS: `sudo command`

---

🧾 _These commands are foundational for any developer or system user working across operating systems. Use responsibly, especially with delete and move operations._

