
# Linux Administration Notes 🐧

## Commands 💻

### System Variables and Environment 🌱
- `set` - Shows all system variables.
- `env` - Displays environmental variables.

### Command Locations 🔍
- `type` - Displays information about a command.
- `whereis` - Locates the binary, source, and manual page for a command.
- `which` - Shows the path of the executable for a command.

### File and Directory Management 📂
- `rm -rf` - Deletes files and directories recursively (Use with caution!).
- `rmdir` - Deletes empty directories.
- `mkdir -p` - Creates directories along with necessary parent directories.
- `cp -p` - Copies files while preserving attributes.

### System Information 🖥️
- `uname` (`-r`, `-o`) - Provides kernel and OS information.
- `/etc/os-release`, `hostnamectl` - Displays detailed OS info.

---

## Disk Usage and Filesystem 🗄️

### Disk Space Monitoring 📊
- `df` (`-h`, `--total`, `-T`) - Displays disk usage by filesystems.
- `du` (`-s`, `-h`, `-a`) - Shows disk usage by files and directories.

### File Archiving and Compression 📦
- `tar -czf archive.tar.gz File1 File2` - Archives and compresses files using gzip.
- `tar -xf archive.tar.gz <destination>` - Extracts files from an archive.
- `tar -tf archive.tar.gz` - Lists files inside the archive.

---

## Permissions and Ownership 🛡️

### User and Group Management 👥
- `useradd`, `usermod` - Adds and modifies user accounts.
  - `-u` - User ID.
  - `-s` - Shell type.
- `groupadd`, `gpasswd` - Manages groups and their members.

### File and Directory Permissions 🔑
- `chmod` (`ugo+-rwx`) - Modifies file permissions.
- `chown` - Changes ownership of files and directories.
- `setfacl` - Sets Access Control Lists for advanced permissions.

---

## Networking 🌐

### Configuration and Monitoring 📡
- `nmcli con show` - Lists active connections.
- `/etc/NetworkManager/system-connections/` - Configuration files for interfaces.

### Diagnostic Tools 🛠️
- `ping`, `nslookup` - Network connectivity checks.
- `tcpdump` - Monitors network traffic.

---

## Software Management 📦

### Package Management 🛒
- `yum install <package>` - Installs a package.
- `rpm -qa` - Lists installed packages.
- `yum group install "<group name>"` - Installs a group of packages.

---

## Processes 🌀

### Process Management ⚙️
- `ps -aux` - Lists processes.
- `jobs` - Displays background jobs.
- `fg`, `bg` - Brings jobs to foreground or background.

### Scheduling Tasks 🗓️
- `crontab -e` - Edits cron jobs.
- `at` - Schedules tasks for a specific time.

---

## Storage Management 💾

### Logical Volume Management (LVM) 📈
- `pvcreate`, `vgcreate`, `lvcreate` - Create and manage physical, volume, and logical volumes.
- `lvextend` - Extends a logical volume.

### Mounting and Filesystems 📍
- `mount <disk> <mountpoint>` - Mounts a filesystem.
- `/etc/fstab` - Persistent mount configuration.

---

## Boot Process 🚀

### System Boot Sequence 🏁
- **BIOS/UEFI ➡️ POST ➡️ MBR ➡️ GRUB ➡️ Kernel ➡️ Systemd ➡️ Target**

### Grub Password Reset 🛠️
- Edit the kernel boot parameters with `init=/bin/bash`.

---

## Containers 🐳

### Podman Basics 🔧
- `podman pull <image>` - Downloads a container image.
- `podman run -d -p 8080:80 <image>` - Runs a container and maps ports.

---

## Firewall and Security 🔥

### Firewall Management 🔒
- `firewall-cmd --list-all` - Lists all rules.
- `firewall-cmd --add-service=http --permanent` - Adds HTTP service.

### SELinux 🛡️
- `sestatus` - Displays SELinux status.
- `semanage` - Manages SELinux rules and policies.

---

## Logs 🗂️
- `/var/log/` - System log directory.
- `journalctl` (`-b`, `-xeu`) - Views detailed system logs.

---

> ⚠️ **Note:** Always double-check commands before running them, especially those involving `rm`, `dd`, or disk management.

---

**Keep exploring and happy learning!** 🎉
