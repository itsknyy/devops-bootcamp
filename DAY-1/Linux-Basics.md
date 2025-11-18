# Linux File System 

|Folder|                        Description                                  |                     
|------|---------------------------------------------------------------------|
|/     |The root of everything. The top-most folder.                         |
|/home |User's personal files. Each user gets a folder here (like C:\Users). |
|/root |Home folder for root (admin) user.                                   |
|/bin  |Basic commands like ls, cp, mv (essential tools).                    |
|/sbin |systemctl, fdisk, mount                                              |        
|/usr  |Contains most of the tools installed using apt / yum.                |
|/etc  |Configuration files (network, SSH, users, services).                 |
|/var  |Data that keeps changing (logs, cache, databases).                   |
|/tmp  |Temporary files (deleted automatically).                             |
|/opt  |Software installed manually (extra apps).                            |
|/proc |System info (CPU, RAM)                                               |
|/dev  |Devices (disks, USB, network)                                        |

# Linux Commands

| Category    | Command                     | Description             |
| ----------- | --------------------------- | ----------------------- |
| Navigation  | `pwd`                       | Show current directory  |
|             | `ls`, `ls -la`              | List files (all/hidden) |
|             | `cd /path`, `cd ..`, `cd ~` | Change directory        |
| Files       | `touch file.txt`            | Create empty file       |
|             | `mkdir folder`              | Create folder           |
|             | `mkdir -p a/b/c`            | Create nested folders   |
|             | `rm file`, `rm -rf folder`  | Delete file/folder      |
|             | `cp src dest`               | Copy file               |
|             | `cp -r dir1 dir2`           | Copy folder             |
|             | `mv old new`                | Move/rename             |
| Viewing     | `cat file`                  | Show full file          |
|             | `less file`                 | Scroll view             |
|             | `head file`                 | First 10 lines          |
|             | `tail file`                 | Last 10 lines           |
|             | `tail -f log`               | Live logs               |
| Search      | `grep "text" file`          | Search text             |
|             | `grep -R "txt" /path`       | Recursive search        |
|             | `find / -name file`         | Find by name            |
| Permissions | `chmod 755 file`            | Change permissions      |
|             | `chown user:group file`     | Change owner            |
| System      | `top`, `htop`               | CPU/memory usage        |
|             | `ps aux`                    | All processes           |
|             | `kill -9 ID`                | Kill process            |
|             | `df -h`                     | Disk usage              |
|             | `du -sh *`                  | Folder size             |
| Network     | `ip a`                      | Show IP                 |
|             | `ip r`                      | Route table             |
|             | `ping 8.8.8.8`              | Test network            |
|             | `curl google.com`           | Get URL                 |
|             | `wget URL`                  | Download                |
|             | `ss -tulnp`                 | Listening ports         |
|             | `telnet IP PORT`            | Connectivity check      |
