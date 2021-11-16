<!-- ------------------------------------------------------------------------- -->

<div class="page-back">

[BACK - Setup-Vultr-Ubuntu](/Setup/fr0301_Setup-Vultr-Ubuntu.md)
</div><div class="page-next">

[Install Web Server - NEXT](/Setup/fr0303_Setup-Web-Server-Ubuntu.md)
</div>

<!-- ------------------------------------------------------------------------- -->

## Instructions for Hardening the Ubuntu server.

- IMPORTANT:  Copy the code lines from the documentation, then click the Send Clipboard button to paste to the console.

- Tip: To clear the console at the console prompt enter: clear

### 1. Restart your Vultr VM and Login

 - Login the your Vultr FormR1 console and click the Restart button

![Restart VM](./images/fr0300-01_restart-vm.png "Restart VM")

 - From your Vultr FormR1 console
 - Copy the root password
 - Click View Console button
 
![Restart VM](./images/fr0300-01_restart-vm1.png "Restart VM")

Login as root using the Send Clipboard button

![Restart VM](./images/fr0300-01_restart-vm2.png "Restart VM")

### 2. Create a new sudo user
- Create a new user alias with root privileges. This user will login remotely.

```
useradd -ou 0 -g 0 -d /root -s /bin/bash -G sudo nimda
```

![New User](./images/fr0302-02_Ubuntu-New-User.png "New User")


- Add the nimda password: FormR!1234

```
passwd nimda

FormR!1234
```

![New User](./images/fr0302-02_Ubuntu-New-User1.png "New User")


- Check to see if nimda is in sudo group

```
grep '^sudo' /etc/group
```

![New User](./images/fr0302-02_Ubuntu-New-User2.png "New User")

- Check user info
```
cat /etc/passwd
```

![New User](./images/fr0302-02_Ubuntu-New-User3.png "New User")


![Check User Info](./images/fr0302-03_Ubuntu-Check-User-Info.png "Check User Info")

### 3. Update and upgrade server

- Enter Y when asked by the following:

```
apt-get update && apt-get upgrade
```

![Update and Upgrade](./images/fr0302-04_Ubuntu-Update-Upgrade.png "Update and Upgrade")

### 4. Install and Configure unattended-updates

- Install
```
apt-get install unattended-upgrades
```

![Install Unattended Upgrades](./images/fr0302-05_Ubuntu-Install-Unattended-Upgrades.png "Install Unattended Upgrades")

- Check installation
```
systemctl status unattended-upgrades
```

![Check Unattended Upgrades](./images/fr0302-06_Ubuntu-Check-Unattended-Upgrades.png "Check Unattended Upgrades")

- Using the nano editor, modify apt.conf.d/50unattended-upgrades

```
nano /etc/apt/apt.conf.d/50unattended-upgrades
```

- Uncomment the “updates” line by deleting the two slashes at the beginning of it:

```
"${distro_id}:${distro_codename}-updates";
```

![Modify apt.conf.d](./images/fr0302-07_Ubuntu-Modify-apt-conf-d.png "Modify apt.conf.d")

- Uncomment and modify:
```
Unattended-Upgrade::Remove-Unused-Kernel-Packages "true";
Unattended-Upgrade::Remove-Unused-Dependencies "true";
Unattended-Upgrade::Automatic-Reboot "true";
Unattended-Upgrade::Automatic-Reboot-Time "02:38";
```

![Modify apt.conf.d-2](./images/fr0302-08_Ubuntu-Modify-apt-conf-d-2.png "Modify apt.conf.d-2")

- Save the file by pressing Ctrl-X, then Y and then Enter to save the file name.

- Using nano, enable Automatic Updates
```
nano /etc/apt/apt.conf.d/20auto-upgrades
```
- Add these lines:
```
APT::Periodic::Update-Package-Lists "1";
APT::Periodic::Download-Upgradeable-Packages "1";
APT::Periodic::AutocleanInterval "7";
APT::Periodic::Unattended-Upgrade "1";
```

![Modify apt.conf.d-3](./images/fr0302-09_Ubuntu-Modify-apt-conf-d-3.png "Modify apt.conf.d-3")

- Save the file by pressing Ctrl-X, then Y and then Enter to save the file name.

- Check if Unattended Upgrades works

```
unattended-upgrades --dry-run --debug
```

![Check Unattended Upgrades](./images/fr0302-10_Ubuntu-Check-Unattended-Upgrades.png "Check Unattended Upgrades")

- Reboot the server

```
From the console prompt enter:

clear
reboot (or you can Click the Send CtrlAltDel button)

After reboot login again as root, copy the password from the Vultr and click the Send Clipboard button
```

### 5. Secure Shared Memory

- Edit  fstab

```
nano /etc/fstab
```

- Add the following line to the bottom of that file:

```
tmpfs /run/shm tmpfs defaults,noexec,nosuid 0 0  
``` 

![Secure Shared Memory](./images/fr0302-11_Ubuntu-secure-shared-memory.png "Secure Shared Memory")

- Save the file by pressing Ctrl-X, then Y and then Enter to save the file name.

- Reboot the server

```
From the console prompt enter:

clear

reboot  (or you can Click the Send CtrlAltDel button)

After reboot login again as root, copy the password from the Vultr and click the Send Clipboard button
```

### 6. Enable SSH Login for Specific Users Only

Get your IP address at:

```
https://whatismyipaddress.com/
``` 

![Get-IP](./images/fr0302-12_Ubuntu-Get-IP.png "Get-IP")
 
- Edit sshd_config

```
nano /etc/ssh/sshd_config
```

- At the bottom of the file, add the line: (Use your own workstation's IP address. 


```
AllowUsers nimda@xxx.xxx.xxx.xxx
```

![SSH-AllowUsers](./images/fr0302-12_Ubuntu-ssh-allowusers.png "SSH-AllowUsers")

- Save the file by pressing Ctrl-X, then Y and then Enter to save the file name.

- Restart sshd with this command:

```
systemctl restart sshd
```

#### - Test local access to your Vultr FormR VM. 
- Get the VM IP address from your Vultr FormR1 console i.e 45.76.252.191
- Open the Windows command prompt on your Develper Workstation
- Paste the following:

```
ssh nimda@<your VM IP address>
```

- Enterb the password: FormR!1234

![SSH-AllowUsers](./images/fr0302-12_Ubuntu-ssh-allowusers1.png "SSH-AllowUsers")

### 7. Include a Security Login Banner

- Create a banner file
```
nano /etc/issue.net
```
- Add a warning message

```
************************************************************************

 Warning!!! This server is dedicated for FormR purposes.
     
 Malicious users will be subject to civil and/or criminal prosecution.
     
************************************************************************
```

- Save the file by pressing Ctrl-X, then Y and then Enter to save the file name.

![SSH-Banner Issue.net](./images/fr0302-13_Ubuntu-ssh-banner-issue-net.png "SSH-Banner Issue.net")

- Disable the banner message from Message Of The Day (motd).

```
nano /etc/pam.d/sshd
```

- Comment out the following two lines (adding a # to the beginning of each line):
```
#session optional pam_motd.so motd=run/motd.dynamic
#session optional pam_motd.so noupdate
```

![SSH-Comment Out](./images/fr0302-14_Ubuntu-ssh-comment-out-pam-d.png "SSH-Comment Out")
     
- Save the file by pressing Ctrl-X, then Y and then Enter to save the file name.

- Edit sshd_config

```
nano /etc/ssh/sshd_config
```
- Replace

```
#Banner none   with    

Banner  /etc/issue.net
```

![SSH-Banner Config](./images/fr0302-15_Ubuntu-ssh-banner-config.png "SSH-Banner Config")


- Save the file by pressing Ctrl-X, then Y and then Enter to save the file name.

- Restart the sshd service
     
```
systemctl restart sshd
```

- When someone logs into your server using SSH, they see your newly added banner warning them of any consequences of further action. 

### 8. Fail2ban

- Install (Enter Y or y when asked to continue.)

```
apt-get install fail2ban
```

![Install Fail2Ban](./images/fr0302-16_Ubuntu-install-fail2ban.png "Install Fail2Ban")

- Configure Fail2Ban
```     
nano /etc/fail2ban/jail.local
```

- In this new file, add the following contents:
```
[sshd]
enabled = true
port = 22
filter = sshd
logpath = /var/log/auth.log
maxretry = 3
```

![SSH-jail-local](./images/fr0302-17_Ubuntu-ssh-jail-local.png "SSH-jail-local")

- This configuration enables the jail, sets the SSH port to be monitored to 22, uses the sshd filter, sets the max login tries, and sets the log file to be monitored.


- Save the file by pressing Ctrl-X, then Y and then Enter to save the file name.

- Restart fail2ban with the command:
```
systemctl restart fail2ban
```
- Attempts to login to the server and fail the three times, access is blocked from the IP address. 

### 9. Enable firewall

- Allow ssh connections through firewall
```
ufw allow OpenSSH
```

- Enable firewall
```
ufw --force enable
```

- Check firewall status

```
ufw status
```

![Enable Firewall](./images/fr0302-18_Ubuntu-enable-firewall.png "Enable Firewall")
### 10. Set the server time zone
```
timedatectl set-timezone America/New_York 
```
- Check TimeZone
```
timedatectl
```

![Set Time Zone](./images/fr0302-19_Ubuntu-set-timezone.png "Set Time Zone")

### 11. Test local access after Hardening

- Test local access to your Vultr FormR VM. 
- Get the VM IP address from your Vultr FormR1 console i.e 45.76.252.191
- Open the Windows command prompt on your Develper Workstation
- Paste the following:

```
ssh nimda@<your VM IP address>
```

![SSH-AllowUsers](./images/fr0302-12_Ubuntu-ssh-allowusers1.png "SSH-AllowUsers")

### 12. Create Snapshot of server in Vultr 

(Note: Snapshots can take up to 20 minutes to complete)

- From Vultr console select snapshots

![Select Snapshots](./images/fr0302-20_Ubuntu-select-snapshots.png "Select Snapshots")

- Add a label, take snapshot

```
FormR-Hardened-Server
```

![Take Snapshot](./images/fr0302-21_Ubuntu-take-snapshot.png "Take Snapshot")

- List Snapshots

![List Snapshots](./images/fr0302-22_Ubuntu-list-snapshots.png "List Snapshots")

<!-- ------------------------------------------------------------------------- -->

<div class="page-back">

[BACK - Setup-Vultr-Ubuntu](/Setup/fr0301_Setup-Vultr-Ubuntu.md)
</div><div class="page-next">

[Install Web Server - NEXT](/Setip/fr0303_Setup-Web-Server-Ubuntu.md)
</div>

<!-- ------------------------------------------------------------------------- -->
