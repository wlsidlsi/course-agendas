**I. Linux Fundamentals**

*   Understanding the Linux Philosophy and History
*   Navigating the Linux Filesystem
    *   Absolute vs. Relative Paths
    *   Key Directories: `/`, `/home`, `/etc`, `/var`, `/tmp`, `/usr`
*   Basic Linux Commands
    *   Listing files: `ls`, `ls -l`, `ls -a`, `ls -lh`
    *   Changing directories: `cd`, `cd ..`, `cd ~`
    *   Creating directories: `mkdir`
    *   Removing files and directories: `rm`, `rm -r`, `rm -rf`, `rmdir`
    *   Copying files and directories: `cp`, `cp -r`
    *   Moving/renaming files and directories: `mv`
    *   Displaying file content: `cat`, `less`, `head`, `tail`
*   Working with Text Files
    *   Creating files: `touch`, `nano`, `vim`
    *   Editing files: `nano`, `vim` (basic commands: insert, save, quit)
    *   Searching within files: `grep`, `grep -i`, `grep -r`
*   File Permissions
    *   Understanding file permissions: read (r), write (w), execute (x)
    *   User, group, and others
    *   Changing file permissions: `chmod` (numeric and symbolic modes)
        *   `chmod 755 file.sh`, `chmod u+x file.sh`
    *   Changing file ownership: `chown`, `chgrp`

**II. User and Group Management**

*   User Accounts
    *   Creating user accounts: `useradd`, `adduser`
    *   Deleting user accounts: `userdel`
    *   Modifying user accounts: `usermod`
    *   Managing user passwords: `passwd`
    *   Understanding `/etc/passwd` and `/etc/shadow`
*   Group Accounts
    *   Creating group accounts: `groupadd`
    *   Deleting group accounts: `groupdel`
    *   Modifying group accounts: `groupmod`
    *   Understanding `/etc/group`
*   Switching Users
    *   Using `su` and `sudo`
    *   Configuring `sudo` access using `visudo`

**III. Package Management**

*   Understanding Package Managers
*   Debian-based Systems (Ubuntu, Debian)
    *   Using `apt` and `apt-get`
        *   Updating package lists: `apt update`
        *   Upgrading packages: `apt upgrade`, `apt dist-upgrade`
        *   Installing packages: `apt install package_name`
        *   Removing packages: `apt remove package_name`, `apt purge package_name`
        *   Searching for packages: `apt search keyword`
    *   Working with `.deb` files: `dpkg`
*   RPM-based Systems (Red Hat, CentOS, Fedora)
    *   Using `yum` and `dnf`
        *   Updating package lists: `yum update`, `dnf update`
        *   Installing packages: `yum install package_name`, `dnf install package_name`
        *   Removing packages: `yum remove package_name`, `dnf remove package_name`
        *   Searching for packages: `yum search keyword`, `dnf search keyword`
    *   Working with `.rpm` files: `rpm`

**IV. Process Management**

*   Understanding Processes
*   Viewing Processes
    *   Using `ps`, `top`, `htop` commands
    *   Understanding process states
*   Controlling Processes
    *   Sending signals to processes: `kill`, `killall`, `pkill`
        *   `SIGTERM`, `SIGKILL`, `SIGHUP`
    *   Running processes in the background: `&`
    *   Using `nohup` to prevent process termination
    *   Process priority: `nice`, `renice`

**V. Networking**

*   Basic Network Concepts
    *   IP addresses, subnet masks, gateways, DNS servers
*   Network Configuration
    *   Viewing network interfaces: `ip addr`, `ifconfig` (deprecated)
    *   Configuring network interfaces (using `ip` command or network configuration files)
    *   Setting hostname: `hostname`, `/etc/hostname`
    *   Configuring DNS: `/etc/resolv.conf`
*   Network Tools
    *   Ping: `ping`
    *   Traceroute: `traceroute`
    *   Netstat/ss: `netstat`, `ss`
    *   Dig/Nslookup: `dig`, `nslookup`
    *   Curl/Wget: `curl`, `wget`
*   Firewall Management
    *   Understanding `iptables` (legacy) and `firewalld`
    *   Configuring basic firewall rules using `firewalld`
        *   Opening ports: `firewall-cmd --add-port=80/tcp --permanent`
        *   Reloading firewall: `firewall-cmd --reload`

**VI. System Monitoring and Logging**

*   System Resource Monitoring
    *   CPU Usage: `top`, `htop`, `vmstat`
    *   Memory Usage: `free`, `vmstat`
    *   Disk Usage: `df`, `du`
    *   I/O Statistics: `iostat`
*   Log Files
    *   Understanding system logs: `/var/log`
    *   Key log files: `/var/log/syslog`, `/var/log/auth.log`, `/var/log/kern.log`, `/var/log/messages`
    *   Using `tail -f` to monitor log files in real-time
    *   Analyzing logs with `grep`, `awk`, and other tools
*   Log Rotation
    *   Understanding `logrotate` configuration

**VII. Shell Scripting Basics**

*   Shell Scripting Fundamentals
    *   Shebang: `#!/bin/bash`
    *   Variables: assignment, expansion
    *   Comments: `#`
    *   Basic Input/Output: `echo`, `read`
*   Control Flow
    *   Conditional statements: `if`, `then`, `else`, `elif`, `fi`
    *   Loops: `for`, `while`, `until`, `do`, `done`
*   Functions
    *   Defining functions
    *   Calling functions
    *   Passing arguments to functions
*   Basic Scripting Tasks
    *   Automating system administration tasks
    *   Creating simple monitoring scripts

**VIII. Automation and Scheduling**

*   Cron
    *   Understanding cron jobs
    *   Editing crontab: `crontab -e`
    *   Cron syntax: minute, hour, day of month, month, day of week
    *   System-wide cron jobs: `/etc/crontab`, `/etc/cron.d/`
*   Systemd Timers
    *   Understanding systemd timers as an alternative to cron
    *   Creating `.timer` and `.service` files for scheduled tasks
    *   Enabling and starting timers: `systemctl enable timer_name.timer`, `systemctl start timer_name.timer`

**IX. Security Fundamentals**

*   SSH Hardening
    *   Disabling password authentication: `PasswordAuthentication no` in `/etc/ssh/sshd_config`
    *   Using SSH keys for authentication
    *   Changing the default SSH port: `Port 2222` in `/etc/ssh/sshd_config`
    *   Restricting user access via `AllowUsers` and `DenyUsers` in `/etc/ssh/sshd_config`
*   Basic Security Practices
    *   Keeping the system updated
    *   Using strong passwords
    *   Regularly reviewing user accounts
    *   Enabling automatic security updates

**X. Virtualization (Introduction)**

*   Virtualization Concepts
    *   Hypervisors: Type 1 (bare metal), Type 2 (hosted)
    *   Virtual Machines (VMs)
*   Using VirtualBox or VMware Workstation
    *   Creating a new VM
    *   Installing a Linux distribution on a VM
    *   Networking between host and guest operating systems
*   Basic Docker Concepts
    *   Understanding Containers
    *   Dockerfile basics
    *   Building and running Docker containers
