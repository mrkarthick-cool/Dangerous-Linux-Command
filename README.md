# ⚠️ Dangerous Linux Command: `sudo rm -rf */*`

## 🔹 What each part means
- **sudo** → runs the command with root privileges (full system control)  
- **rm** → remove (delete) files  
- **-rf** →  
  - `-r` = recursive (delete directories and their contents)  
  - `-f` = force (ignore warnings, delete without asking)  
- **`*/*`** → matches all subdirectories inside the current directory and deletes everything inside them  

---

## 🔹 What happens if you run it
- Every folder in your current working directory will be wiped out  
- Because you used `sudo`, it will delete files even if they are protected  
- If you run this from a high‑level directory (like `/home`, `/`, or `/etc`), you could **destroy your entire system** — all user files, configs, and even system binaries  
- Once executed, there’s no easy recovery unless you have backups  

---

## ⚠️ Critical Warning
This is **not** a harmless test command. On Kali Linux (or any Linux), running:

```bash
sudo rm -rf */*
 
