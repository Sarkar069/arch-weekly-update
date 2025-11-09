<h1 align="center">🛠️ Arch Weekly Update</h1>

<p align="center">
A simple, safe, and colorful <b>weekly update script</b> for Arch Linux 🐧<br>
Updates mirrors, system, and AUR — logs everything, trims old logs, and tells you when to reboot.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Arch%20Linux-blue?logo=arch-linux&logoColor=white" alt="Arch Linux">
  <img src="https://img.shields.io/badge/Bash-5.x-brightgreen?logo=gnu-bash&logoColor=white" alt="Bash">
  <img src="https://img.shields.io/badge/License-MIT-yellow?logo=open-source-initiative&logoColor=white" alt="MIT License">
</p>

---

## 🚀 Features

✅ **Safe** — Asks before updating, checks `.pacnew` files, and suggests reboot.  
✅ **Smart Logging** — Logs every run to `/var/log/arch-weekly-update.log` and trims old entries.  
✅ **Mirror Optimization** — Uses `reflector` to fetch the fastest regional mirrors.  
✅ **Full Maintenance** — Updates Pacman + AUR + cleans cache in one go.  
✅ **Colorful Output** — Easy to read, even during long updates.  

---

## ⚙️ Installation
**Clone the repo**
```bash 
git clone https://github.com/Sarkar069/arch-weekly-update.git
```
**move or copy the script**
``` bash
mkdir -p ~/bin
mv arch-weekly-update/archeekly ~/bin
chmod +x ~/bin/archeekly
```
Ensure ~/bin is in your PATH
``` bash 
echo $PATH | grep -q "$HOME/bin" || echo 'export PATH="$HOME/bin:$PATH"' >> ~/.bashrc # or .zshrc 
source ~/.bashrc 
```

## 🧩 Usage
Run it anytime with:
``` bash 
sudo ~/bin/archeekly
```
## 🧾 Checking Logs
View the most recent update:
```bash
sudo tail -n 30 /var/log/arch-weekly-update.log
```
Scroll through the full history:
```bash
sudo less /var/log/arch-weekly-update.log
```
Find warnings or errors:
```bash 
sudo grep -E "error|failed" /var/log/arch-weekly-update.log
```
