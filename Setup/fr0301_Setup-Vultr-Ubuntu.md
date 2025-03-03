<!-- ------------------------------------------------------------------------- -->

<div class="page-back">

[BACK - Test NodeJS](/Setup/fr0102_Test-Node.md)
</div><div class="page-next">

[Harden Ubuntu - NEXT](/Setup/fr0302_Setup-Hardening-Ubuntu.md)
</div><div style="margin-top:35px">&nbsp;</div>

<!-- ------------------------------------------------------------------------- -->

## 2.1 Create Vultr Ubuntu 0:25 <!-- {docsify-ignore} -->
<div class="notice-tip">
  <div class="notice-tip-header">
    Tip: <a href="../Setup/purposes/pfr0301_Setup-Vultr-Ubuntu.md" target="_blank">Link to Background and Purposes</a> 
  </div>  
</div>

<div class="notice-tip">
  <div class="notice-tip-header">
    Tip: <a href="https://discord.com/channels/928752444316483585/931217076885008495" target="_blank">Link to Discord for Your Comments</a> 
  </div>  
</div>

#### Introduction <!-- {docsify-ignore} -->
- In order to test our formR apps on the Internet [label](http://localhost:5502/#%2FSetup%2Ffr0302_Setup-Hardening-Ubuntu%3Fid%3D_5-uncomment-and-modify-note-use-your-down-arrow-to-find-these-items-they-are-near-the-bottom-of-the-file) we will create an Ubuntu server on the cloud provider, Vultr.com. 
- Vultr costs under $10 per month. 
- Please use the following link when you begin:

```
https://www.vultr.com/?ref=9024374-8H
```

<details class="details-style">
    <summary class="summary-style">
More Info: Names, Caps, Picts, Code Copy
    </summary>
    <div class="popup">

- In this tutorial please be careful to use the Exact Spelling and Capitalization. You will be using Windows, Unix and GitBash command prompts. Improper captialization will cause commands to fail. Some examples are: Local_Admin, myProject, repos, remotes and .ssh.

- This documentation was produced in 2021-2022. You will experience differences in some of the pictures due to the changes made over time by the developers of the softwares and web sites that are used.

- We recommend that you copy and paste code snippets from the documentation into your workstation/server. This will reduce the errors caused by hand typing.
Hover over the snippet and click copy, then paste as appropriate.

</div>
</details>


----
### 1. Create New Ubuntu Instance  0:10
----
#### 1. Signin or create an account on vultr.com 


<div class="notice-tip">
  <div class="notice-tip-header">
    Note: the ref=9024374-8H below tells Vultr and us that you are doing the formR tutorial.
  </div>  
</div>

- Browse to:

```
https://www.vultr.com/?ref=9024374-8H
```

#### 2. Deploy New Server 

![Vultr Deploy New Server](./images/fr0301-01_Vultr-Deploy-New-Server.png "Deploy New Server")

<div class="notice-tip">
  <div class="notice-tip-header">
    Summary: Vultr changes its deploy steps from time to time, so our pictures below may be different. Here is a list of configurations that you need:<br/><br/>
    Server = Cloud Compute<br/>
    CPU and Storage = Intel High Performance<br/>
    Server Location = Choose one near you<br/>
    Server Image = Ubuntu (choose highest numbered version)<br/>
    Server Size = Choose smallest available and lowest price<br/>
    Auto Backup = Off<br/>
    Additional features = Enable IPv6<br/>
    Server Hostname and Label = Vultr-FormR0 
  </div>  
</div>


#### 3. Choose Server: Cloud Compute

![Vultr Cloud Compute](./images/fr0301-02_Vultr-Cloud-Compute.png "Cloud Compute")

#### 4. CPU and Storage

![Vultr Server Location](./images/fr0301-03_Vultr-Server-CPU.png "Server Location")

#### 5. Server Location

<div class="notice-tip">
  <div class="notice-tip-header">
    Tip: Select a location near to you.</a> 
  </div>
</div>

![Vultr Server Location](./images/fr0301-03_Vultr-Server-Location.png "Server Location")

#### 6. Server Image: Ubuntu choose the highest version for the formR tutorial.

![Vultr Server Type](./images/fr0301-04_Vultr-Server-Type.png "Server Type")

#### 7. Server Size: 25GB

![Vultr Server Size](./images/fr0301-05_Vultr-Server-Size.png "Server Size")

#### 8. Add SSH Key

- Select your Vultr public key in C:\users\Local_Admin\\.ssh

![Vultr-Select-Key](./images/fr0301-06_Vultr-Select-Key.png "Vultr-Select-Key")

- Open the file in Notepad and copy the key 

![Vultr-Copy-Key](./images/fr0301-06_Vultr-Copy-Key.png "Vultr-Copy-Key")

- Paste the key value into the Vultr SSH Key box and give the key a name.

![Vultr-add-SSH-key-pasted](./images/fr0301-06_Vultr-add-SSH-key-pasted.png "Vultr-add-SSH-key-pasted")

#### 9. Auto Backup = Off

<div class="notice-tip">
  <div class="notice-tip-header">
    Hint: Turn backup off for now. Turn on if you are going to keep this server after completing the tutorial.
.</a> 
  </div>
</div>

![Vultr-Host-Label](./images/fr0301-07_Vultr-Auto-Backup.png "Vultr-Host-Label")

#### 10. Additional Features

- Enable IPv6

![Vultr-IPv6](./images/fr0301-07_Vultr-IPv6.png "Vultr-IPv6")

#### 11. Server Hostname and Label: 

- Use for both Hostname and Label:

```
Vultr-FormR0 
```

![Vultr-Host-Label](./images/fr0301-07_Vultr-Host-Label.png "Vultr-Host-Label")


#### 12. Click Deploy Now

<div class="notice-tip">
  <div class="notice-tip-header">
    Info: Deploy now takes a few minutes to complete.</a> 
  </div>
</div>

![Vultr Deploy Now](./images/fr0301-07_Vultr-Deploy-Now.png "Deploy Now")

- Installing

![Vultr Installing](./images/fr0301-08_Vultr-Installing.png "Installing")

#### 13. Connect from Your Workstation via ssh

<div class="notice-tip">
  <div class="notice-tip-header">
    Info: This connection confirms your access from workstation to server.</a> 
  </div>
</div>

- Open a command window on your workstation

![Vultr ssh 1](./images/fr0301-09_Vultr-ssh1.png "Vultr ssh1")

- At the command prompt enter:

```
ssh root@(your Vultr server ip address-copy from Vultr)
```

![Vultr ssh 2](./images/fr0301-09_Vultr-ssh2.png "Vultr ssh2")

- Enter yes for Continue connecting

![Vultr ssh 3](./images/fr0301-09_Vultr-ssh3.png "Vultr ssh3")

- Enter your Vultr password (copy from Vultr)

![Vultr ssh 4](./images/fr0301-09_Vultr-ssh4.png "Vultr ssh4")

- Right click in the command window and Edit Paste the password

![Vultr ssh 4](./images/fr0301-09_Vultr-ssh5.png "Vultr ssh4")

- Success

![Vultr ssh 4](./images/fr0301-09_Vultr-ssh6.png "Vultr ssh4")

----
### 2. Use Bitvise to access Vultr-FormR0  0:15
----
#### 1. Open Bitvise

![Vultr Open-Bitvise](./images/fr0301-09_Vultr-Open-Bitvise.png "Vultr Open-Bitvise")

#### 2. Click New Profile

![Vultr New-Profile](./images/fr0301-09_Vultr-New-Profile.png "Vultr New-Profile")

#### 3. Enter new profile name

```
Vultr-FormR0-root.tlp
```

![Vultr New-Profile-Name](./images/fr0301-09_Vultr-New-Profile-Name.png "Vultr New-Profile-Name")

#### 4. Fill in the following:

- Host = Vultr-FormR0 IP Address (copy from Vultr web page)

- Port = 22

- Username = root

- Initial Method = password

- Click Checkbox - Store encrypted password in profile

- Password = Vultr-FormR0 root password (copy from Vultr web page)

![Vultr New-Profile-Copy](./images/fr0301-09_Vultr-New-Profile-Copy.png "Vultr New-Profile-Copy")

![Vultr New-Profile-Login](./images/fr0301-09_Vultr-New-Profile-Login.png "Vultr New-Profile-Login")

#### 5. Click Login

![Vultr New-Profile-Host](./images/fr0301-09_Vultr-New-Profile-Host.png "Vultr New-Profile-Host")

![Vultr New-Profile-Auth](./images/fr0301-09_Vultr-New-Profile-Auth.png "Vultr New-Profile-Auth")

#### 6. Save Profile

<div class="notice-warning">
  <div class="notice-warning-header">
    Important: Save Profile -- Don't Lose Your Work
  </div>
</div>  


![Vultr New-Profile-Save](./images/fr0301-09_Vultr-New-Profile-Save.png "Vultr New-Profile-Save")

![Vultr New-Profile-Save1](./images/fr0301-09_Vultr-New-Profile-Save1.png "Vultr New-Profile-Save1")



#### 6. Click New terminal console button

![Vultr New-Profile-Console](./images/fr0301-09_Vultr-New-Profile-Console-root.png "Vultr New-Profile-Console")

#### 7. You will see the Welcome screen for Ubuntu and the command prompt:

    root@Vultr-FormR0:~#

![Vultr Welcome](./images/fr0301-13_Vultr-Welcome.png "Welcome")

----
<div class="notice-success">
  <div class="notice-success-header">
    Congratulations! You have created your Ubuntu server on Vultr.
  </div>
</div>

----


<!-- ------------------------------------------------------------------------- -->

<div class="page-back">

[BACK - Test NodeJS](/Setup/fr0104_Test-Node.md)
</div><div class="page-next">

[Harden Ubuntu - NEXT](/Setup/fr0302_Setup-Hardening-Ubuntu.md)
</div>



