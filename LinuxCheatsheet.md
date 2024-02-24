# Linux and Linux server CheatSheet

This is a thorough guide to commands for interacting with Linux via the command line.


| Command | Description | Usage Example |
|---------|-------------|---------------|
| `sudo` | Execute a command as another user, typically the superuser. This is useful when certain commands require elevated permissions. | `sudo apt-get update` |
| `root` | The superuser account in Unix and Linux. It has full access to the system and can perform any operation. | `su root` |
| `ls` | List directory contents. It can display additional information such as file permissions, number of links, owner, group, size, and modification time when used with options like `-l`. | `ls -l` |
| `cd` | Change the shell working directory. It's used to navigate between directories. | `cd /home/user` |
| `mkdir` | Create a new directory. This command takes the name of the directory to be created as argument. | `mkdir new_directory` |
| `nano` | A simple, user-friendly text editor in Unix and Linux systems. It's used to create and edit text files. | `nano file.txt` |
| `rm` | Remove files or directories. Be careful with this command, especially when used with options like `-r` (recursive delete) and `-f` (force delete without confirmation). | `rm file.txt` |
| `tab` | Auto-complete files, directories, and command names. It's a feature of the shell that saves typing. | Press `tab` after typing part of the name. |
| `cat` | Concatenate and display file content. It's used to view the contents of a file. | `cat file.txt` |
| `&&` | Execute two commands sequentially, the second one only if the first one succeeds. It's a control operator in the shell. | `cd /home/user && ls` |
| `""` | Define a string. It's used in various commands to specify a string of characters. | `echo "Hello, World!"` |
| `/` | Directory separator. It's used in specifying paths. | `cd /home/user` |
| `grep` | Search for a pattern in files. It's a powerful text search tool that uses regular expressions. | `grep "Hello" file.txt` |
| `less` | View file content page by page. It's a more advanced version of the `more` command, allowing both forward and backward navigation. | `less file.txt` |
| `\|` | Pipe output of one command to another. It's used to create pipelines. | `ls -l \| grep "Aug"` |
| `mv` | Move or rename files. It's used to change the location or the name of files and directories. | `mv old.txt new.txt` |
| `cp` | Copy files. It's used to create copies of files and directories. | `cp source.txt dest.txt` |
| `rsync` | Remote file copy (Synchronize file trees). It's a fast and versatile file copying tool, which can copy locally, to/from another host over any remote shell, or to/from a remote rsync daemon. | `rsync -a /source_folder /dest_folder` |
| `shutdown` | Shutdown or restart the system. It's a powerful command that should be used carefully. | `shutdown -r now` |
| `telinit` | Change SysV runlevel. It's used to change the system runlevel, which is a state of a SysV-like operating system that defines what services are available. | `telinit 0` |
| `su` | Substitute user identity. It's used to change the current user identity to another user. | `su username` |
| `sudoers` | File that defines which users can use `sudo` and what they can do. It's edited using the `visudo` command for syntax checking. | `visudo` |
|`touch`|Create a new empty file. This command takes the name of the file to be created as argument.|touch new_file.txt|
|`chmod`|Change file permissions. It’s used to modify the read, write, and execute permissions of files and directories.|chmod 755 script.sh|
|`chown`|Change file owner and group. It’s used to change the user and/or group ownership of files and directories.|chown user:group file.txt|
|`df`|Report file system disk space usage. It’s used to get an overview of available and used disk space.|df -h|
|`du`|Estimate file and directory space usage. It’s used to check the disk usage of files and directories.|`du -sh /home/user`|
|`find`|Search for files in a directory hierarchy. It’s a powerful tool to find files and directories based on different search criteria.|`find / -name "*.txt"`|
|`ps`|Report a snapshot of the current processes. It’s used to monitor the processes running on the system.|`ps aux`|
|`top`|Display Linux processes. It provides a dynamic real-time view of the running system.|`top`|
|`kill`|Send a signal to a process. It’s used to terminate, hang up, or restart processes.|`kill -9 12345`|
|`tar`|Archive utility. It’s used to store and extract files from an archive file known as tarball.|`tar -cvf archive.tar /home/user`|
|`gzip`|Compress or expand files. It’s used to reduce the file size.|`gzip file.txt`|
|`gunzip`|Decompress files. It’s used to restore compressed files to their original form.|`gunzip file.txt.gz`|
|`ping`|Send ICMP ECHO_REQUEST to network hosts. It’s used to check the network connectivity to another host on the network.|`ping www.google.com`|
|`netstat`|Network statistics. It’s used to display network connections, routing tables, interface statistics, etc.|`netstat -a`|
|`ifconfig`|Display or configure a network interface. It’s used to configure, or display the configuration of, a network interface.|`ifconfig eth0`|
|`iwconfig`|Configure a wireless network interface. It’s used to check or set the parameters of a wireless network interface.|`iwconfig wlan0`|
|`ssh`|OpenSSH SSH client (remote login program). It’s used for secure remote administration of systems.|`ssh user@hostname`|
|`scp`|Secure copy (remote file copy program). It’s used to securely transfer files between hosts on a network.|`scp user@hostname:/path/to/file /local/path`|
|`wget`|Non-interactive network downloader. It’s used to download files from the internet.|`wget http://example.com/file.txt`|
|`curl`|Transfer data from or to a server. It’s used for making requests and transferring data using various protocols.|`curl -O http://example.com/file.txt`|
|`apt-get`|APT package handling utility (command-line interface). It’s used for handling packages in Linux distributions based on Debian.|`sudo apt-get install package_name`|
|`yum`|Package manager for RPM-based Linux distributions. It’s used for managing packages in Linux distributions based on Red Hat.|`sudo yum install package_name`|
|`dnf`|Next-generation package manager for RPM-based Linux distributions. It’s used for managing packages in Fedora and its derivatives.|`sudo dnf install package_name`|
|`pacman`|Package manager utility for Arch Linux. It’s used for installing, upgrading, configuring, and removing software.|`sudo pacman -S package_name`|
|`zypper`|Command line package manager for openSUSE. It’s used for managing packages in openSUSE and its derivatives.|`sudo zypper install package_name`|
|`systemctl`|Control the systemd system and service manager. It’s used to manage services and the system itself.|`sudo systemctl start service_name`|
|`journalctl`|Query the systemd journal. It’s used to view the logs collected by systemd.|`journalctl -u service_name`|
|`crontab`|Maintain crontab files for individual users. It’s used to schedule tasks to run at fixed times.|`crontab -e`|
|`alias`|Create an alias for a command. It’s used to create a shortcut or a more memorable/meaningful name for a command.|`alias ll='ls -l'`|
|`unalias`|Remove an alias. It’s used to remove a previously created alias.|`unalias ll`|
|`history`|Command history. It’s used to view the previously executed commands.|`history`|
|`clear`|Clear terminal screen. It’s used to clean up the terminal window.|`clear`|
|`exit`|Exit the shell. It’s used to end the terminal session.|`exit`|
