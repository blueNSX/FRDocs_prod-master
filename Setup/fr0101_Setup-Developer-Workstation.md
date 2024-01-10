<!-- ------------------------------------------------------------------------- -->

<div class="page-back">

[BACK - formR Introduction](/_home.md.md)
</div><div class="page-next">

[Test NodeJS- NEXT](/Setup/fr0102_Test-Node.md)
</div><div style="margin-top:35px">&nbsp;</div>

<!-- ------------------------------------------------------------------------- -->

## 1.1 Build Workstation 2:30 <!-- {docsify-ignore} -->
<div class="notice-tip">
  <div class="notice-tip-header">
    Tip: <a href="../Setup/purposes/pfr0101_Setup-Developer-Workstation.md" target="_blank">Link to Background and Purposes</a> 
  </div>  
</div>

<div class="notice-tip">
  <div class="notice-tip-header">
    Tip: <a href="https://discord.com/channels/928752444316483585/932678480863305770" target="_blank">Link to Discord for Your Comments</a> 
  </div>  
</div>

#### Introduction <!-- {docsify-ignore} -->
- The following steps create the development environment on your workstation for developing an MERN stack (MySql, Express, React and Node) application. 

- You will access a repository on github and modify it, run it and push changes back to github. We will be using an empty 'Windows Pro N' VM in these instructions. You should be able to use any Windows 10 or above workstation. Just follow the steps. The total disk space required is about 6          GB.

<details class="notice-info">
    <summary class="notice-info-header">
More Info: Names, Caps, Picts, Code Copy
    </summary>
    <div class="notice-info-popup">

- In this tutorial please be careful to use the Exact Spelling and Capitalization. You will be using Windows, Unix and GitBash command prompts. Improper captialization will cause commands to fail. Some examples are: Local_Admin, myProject, repos, remotes and .ssh.

- This documentation was produced in 2021-2022. You will experience differences in some of the pictures due to the changes made over time by the developers of the softwares and web sites that are used.

- We recommend that you copy and paste code snippets from the documentation into your workstation/server. This will reduce the errors caused by hand typing.
Hover over the snippet and click copy, then paste as appropriate.

</div>
</details>

----
### 1. Create a new user, Local_Admin, on your workstation. 0:10
----

<div class="notice-warning">
  <div class="notice-warning-header">
    Warning: Use the Account Name: Local_Admin
  </div>

- It is not recommended to use another account name.

- This account name will be referenced throughout the tutorial.

- If you choose another account name, it cannot contain spaces in the name. This tutorial will fail, if spaces are found in the Windows user account name.

</div>

#### 1. Login to your Windows account
<br/>

![Windows-Login](./images/fr0101-00_Windows-Login.png "Windows-Login")

#### 2. Search for Control Panel
<br/>

![Windows-Controlpanel](./images/fr0101-00_Windows-Controlpanel.png "Windows-Controlpanel")

#### 3. Click Change account type under User Accounts
<br/>

![Windows-Useraccounts](./images/fr0101-00_Windows-Useraccounts.png "Windows-Useraccounts")

#### 4. Click Add New User...
<br/>

![Windows-Addnewuser](./images/fr0101-00_Windows-Addnewuser.png "Windows-Addnewuser")

#### 5. Click the (+) Add someone else...
<br/>

![Windows-Addsomeoneelse](./images/fr0101-00_Windows-Addsomeoneelse.png "Windows-Addsomeoneelse")

#### 6. Click I don't have this person's...
<br/>

![Windows-Idonthave](./images/fr0101-00_Windows-Idonthave.png "Windows-Idonthave")

#### 7. Click Add a user without a Microsoft account
<br/>

![Windows-Addauserwithout](./images/fr0101-00_Windows-Addauserwithout.png "Windows-Addauserwithout")

#### 8. Create a user by filling in the information for:
<br/>

- User name:
``` 
Local_Admin
```
- Password:
```
FormR!1234
```

- Select the secret questions and answers to complete the form.

![Windows-Createauser](./images/fr0101-00_Windows-Createauser.png "Windows-Createauser")

#### 9. Go to Control Panel -> User Accounts -> Change Account Type and select the Local_Admin account
<br/>

![Windows-Selectlocaladmin](./images/fr0101-00_Windows-Selectlocaladmin.png "Windows-Selectlocaladmin")

#### 10. Click Change Account Type
<br/>

![Windows-Changelocaladmintype](./images/fr0101-00_Windows-Changelocaladmintype.png "Windows-Changelocaladmintype")

#### 11. Click Administrator radio button and then the Change Account Type button
<br/>

![Windows-Selectadministrator](./images/fr0101-00_Windows-Selectadministrator.png "Windows-Selectadministrator")

![Windows-Selectadministrator-1](./images/fr0101-00_Windows-Selectadministrator-1.png "Windows-Selectadministrator-1")

#### 12. Sign out

- Click the Start charm on the taskbar
- then click your login name 
- then click Sign out

![Windows-Signout](./images/fr0101-00_Windows-Signout.png "Windows-Signout")

#### 13. Sign in as Local_Admin

![Windows-Signin](./images/fr0101-00_Windows-Signin.png "Windows-Signin")

----
### 2. Install any updates to your workstation.0:05
----

![Windows-Update](./images/fr0101-01_Windows-Update.png "Windows-Update")

----
### 3. Create new folders, change View Options, setup ssh and create keys 0:15
----
#### 1. In C:\, add folder: repos 

- The repos folder has local copies of your gitHub repositories files

![Create-folders](./images/fr0101-02_Create-folders.png "Create-folders")

#### 2. In C:\users\Local_Admin\, add folder: .ssh 

- The .ssh folder holds your ssh key related files

![Create-folders2](./images/fr0101-02_Create-folders2.png "Create-folders2")

#### 3. Change View Options in File Explorer

- Enable Extentions and Hidden Files

![Change-View-Options](./images/fr0101-02_Change-View-Options.png "Change-View-Options")

#### 4. Test if OpenSSH client is installed.

- From DOS command prompt run ssh.

![OpenSSH-not-installed](./images/fr0101-02_OpenSSH-not-installed.png "OpenSSH-not-installed")

- If .ssh IS installed, skip to step 7.

#### 5.  If OpenSSH client is Not installed

- Install OpenSSH in Apps & Features - Optional Features

![Install-OpenSSH1](./images/fr0101-02_Install-OpenSSH1.png "Install-OpenSSH1")

![Install-OpenSSH2](./images/fr0101-02_Install-OpenSSH2.png "Install-OpenSSH2")

![Install-OpenSSH3](./images/fr0101-02_Install-OpenSSH3.png "Install-OpenSSH3")

#### 6. OpenSSH client at the command prompt enter:

```
ssh
```

![OpenSSH-is-installed](./images/fr0101-02_OpenSSH-is-installed.png "OpenSSH-is-installed")


#### 7. Create 3 ssh keys. 

<div class="notice-tip">
  <div class="notice-tip-header">
Note:

-  These keys will be used for GitHub, your Cloud Provider and your Remote server.

-  Run from the Windows command prompt.

  </div>  
</div>

<div class="notice-tip">
  <div class="notice-tip-header">Format for all 3 ssh keys:

- ssh-keygen -t rsa -f
"local user folder/.ssh/
key owner name@host name_host user initials_vdate_key"
-C "key owner name@host name_host user initials_vdate"

Example: 

- ssh-keygen -t rsa -f "c:/Users/Local_Admin/.ssh/mickey.mouse@github_mick_v210713_key" -C "mickey.mouse@github_mick_v210713"

- In the following "mickey mouse snippets" change the following to your info:

- "mickey.mouse" to your Key Owner Name i.e. bruce.troutman
- "mick" to your initials i.e. kff or cbt or bill, etc.
-"v210713" to the "v" + current date  YYMMDD

  </div>  
</div>


##### 1. Key pairs for Github:

- Paste the following code into Notepad and modify it to your information:


```
ssh-keygen -t rsa -f "c:/Users/Local_Admin/.ssh/mickey.mouse@github_mick_v210713_key" -C "mickey.mouse@github_mick_v210713"
```

<div class="notice-tip">
  <div class="notice-tip-header">
    Note: Do not enter a passphase, when prompted.
  </div>  
</div>

![Create New ssh key1](./images/fr0101-03_Create-New-ssh-key1.png "Create New ssh key1")

##### 2. Key pairs for Cloud Provider:

- Paste the following code into Notepad and modify it to your information:

```
ssh-keygen -t rsa -f "c:/Users/Local_Admin/.ssh/mickey.mouse@Vultr_mick_v210713_key" -C "mickey.mouse@Vultr_mick_v210713"
```

<div class="notice-tip">
  <div class="notice-tip-header">
    Note: Do not enter a passphase, when prompted.
  </div>  
</div>

![Create New ssh key2](./images/fr0101-03_Create-New-ssh-key2.png "Create New ssh key2")


##### 3. Key pairs for access to Remote Server on Cloud Provider:

- Paste the following code into Notepad and modify it to your information:

```
ssh-keygen -t rsa -f "c:/Users/Local_Admin/.ssh/mickey.mouse@Vultr-FormR0_mick_v210713_key" -C "mickey.mouse@Vultr-FormR0_mick_v210713"
```

<div class="notice-tip">
  <div class="notice-tip-header">
    Note: Do not enter a passphase, when prompted.
  </div>  
</div>

![Create New ssh key3](./images/fr0101-03_Create-New-ssh-key3.png "Create New ssh key3")

##### 4. View created key files:
<br/>

![Create New ssh key4](./images/fr0101-03_Create-New-ssh-key4.png "Create New ssh key4")

----
### 4. Install or open Chrome browser 0:10
----

- If Chrome is installed, skip to step 2.

#### 1. Download and install Chrome from:

```
https://google.com/chrome
```

![Chrome-extensions](./images/fr0101-03_Chrome-install.png "Chrome-extensions")

#### 2. Make Chrome your default browser

- Search for "Settings" in the Windows tray, then Apps

<div class="notice-tip">
  <div class="notice-tip-header">
    Note: This only applies to the Local_Admin account.
  </div>  
</div>
<br/>

![Chrome-extensions](./images/fr0101-03_Chrome-make-default.png "Chrome-extensions")


#### 3. Install Chrome Extensions

- These tools will be useful in development.

```
https://chrome.google.com/webstore/category/extensions?hl=en-US
```

![Chrome-extensions](./images/fr0101-03_Chrome-extensions.png "Chrome-extensions")

#### 4. Add Markdown Preview Plus

- This extension will allow chrome to display Markdown files

![Chrome-extensions1](./images/fr0101-03_Chrome-extensions1.png "Chrome-extensions1")

#### 5. Allow access to file URLs

- This setting will allow Chrome to view Markdown (.md) files from File Explorer

```
chrome://extensions/?id=febilkbfcbhebfnokafefeacimjdckgl
```

![Chrome-extensions2](./images/fr0101-03_Chrome-extensions2.png "Chrome-extensions2")

#### 6. Add React Developers Tools

- This extensions adds debugging assistance to Chrome for React applications

```
https://chrome.google.com/webstore/category/extensions?hl=en-US
```

![Chrome-extensions3](./images/fr0101-03_Chrome-extensions3.png "Chrome-extensions3")

#### 7. Check the installations

<div class="notice-tip">
  <div class="notice-tip-header">
    Note: Google Docs Offline was installed with Chrome.
  </div>  
</div>


```
chrome://extensions/
```

![Chrome-extensions4](./images/fr0101-03_Chrome-extensions4.png "Chrome-extensions4")

----
### 5. Create Github account or sign in to GitHub then Add your ssh key. 0:15
----
#### 1. Sign in to GitHub. (Create an account, if you don't have one.)

```
https://github.com
```

![Login to Github](./images/fr0101-04_Login-to-github.png "Login to GitHub")

#### 2. Add your Github ssh key from your .ssh folder to your github account.

```
https://github.com/settings/ssh
```

#### 3. Click New SSH Key button

![Add New ssh key](./images/fr0101-04_Add-New-ssh-key.png "Add New ssh key")

![Add New ssh key-1](./images/fr0101-04_Add-New-ssh-key-1.png "Add New ssh key-1")


#### 4. In notepad open your github public key from your .ssh folder, then copy the contents to the clipboard.

![Add New ssh key-2](./images/fr0101-04_Add-New-ssh-key-2.png "Add New ssh key-2")

![Add New ssh key-3](./images/fr0101-04_Add-New-ssh-key-3.png "Add New ssh key-3") 


#### 5. Paste the clipboard contents into the Key box in the github SSH Keys/ Add someone elseow.

#### 6. Copy the last part of the key and paste it into the Title box.

#### 7. Click the Add SSH key button when finished.


![Add New ssh key-4](./images/fr0101-04_Add-New-ssh-key-4.png "Add New ssh key-4")

![Add New ssh key-5](./images/fr0101-04_Add-New-ssh-key-5.png "Add New ssh key-5")


#### 8. Create a new repository: 'myProject'.

```
https://github.com/new
```

#### 9. Add Repository Name "myProject", select Private and check ReadMe file, then click Create Repository.


![GitHub-myProject](./images/fr0101-04_GitHub-myProject.png "GitHub-myProject")

#### 10. Edit the Readme.md file

- Click the pencil


![GitHub-myProject-readme](./images/fr0101-04_GitHub-myProject-readme.png "GitHub-myProject-readme")

#### 11. Change file to:

```
# myProject was created on mm/dd/yyyy.
```

![GitHub-myProject-readme2](./images/fr0101-04_GitHub-myProject-readme2.png "GitHub-myProject-readme2")

#### 12. Commit changes

- Go to the bottom of the edit page to the Commit Changes section.

- A description is required: Update README.md

- Click commit Changes

![GitHub-myProject-readme3](./images/fr0101-04_GitHub-myProject-readme3.png "GitHub-myProject-readme3")

![GitHub-myProject-readme4](./images/fr0101-04_GitHub-myProject-readme4.png "GitHub-myProject-readme4")

- Close your browser.

#### 13. Configure ssh Access to Github on your Windows workstation

- Create a Host for github connection in the .ssh/config file.


- Create .ssh/config file in C:/users/Local_Admin/.ssh. Make sure it is saved without the .txt extention, then open with notepad and add the following:

```
Host github-mick
    HostName       github.com
    IdentityFile   C:/Users/Local_Admin/.ssh/mickey.mouse@github_mick_v210713_key
    User           git
```

- Be sure to change:
    - "github-mick"  to "github-(your initials)"
    - IdentityFile to the name of your github key file in C:/Users/Local_Admin/.ssh


![Add Host to config](./images/fr0101-03_Add-host-to-config.png "Add Host to config")

#### 14. From the DOS command window, test the connection to github.

- Replace mick with your initials

```
ssh github-mick
```

<div class="notice-tip">
  <div class="notice-tip-header">
    Note: On the first try when prompted enter "yes"
  </div>  
</div>
 


![Test ssh to github-1st-yes](./images/fr0101-03_Test-ssh-to-github-1st-yes.png "Test ssh to github-1st-yes") 

- Change directory to repos, connect again and you will be successfully authenticated.

```
ssh github-your initials
```

![Test ssh to github](./images/fr0101-03_Test-ssh-to-github.png "Test ssh to github")

----
### 6. Download Git, if not already installed 0:10
----

```
 https://git-scm.com/download/win
```

![Git-for-Windows](./images/fr0101-06_Git-for-Windows.png "Git-for-Windows")

#### 1. Allow changes

![Git-for-Windows1](./images/fr0101-06_Git-for-Windows1.png "Git-for-Windows1") 

#### 2. Accept **all the defaults** and install

![Git-for-Windows2](./images/fr0101-06_Git-for-Windows2.png "Git-for-Windows2")

#### 3. Finish Install check Launch Git Bash

![Git-for-Windows3](./images/fr0101-06_Git-for-Windows3.png "Git-for-Windows3")


#### 4. Open Git Bash

![Git-for-Windows4](./images/fr0101-06_Git-for-Windows4.png "Git-for-Windows4")


#### 5. From Git Bash prompt add Username for github

- Change Mickey Mouse to (your name)

```
git config --global user.name = "Mickey Mouse"
```

![Git-for-Windows5](./images/fr0101-06_Git-for-Windows5.png "Git-for-Windows5")


#### 6. Add User Email for github

- Change mickey.mouse@gmail.com to <your email in github>:    

```
git config --global user.email = "mickey.mouse@gmail.com"
```

![Git-for-Windows6](./images/fr0101-06_Git-for-Windows6.png "Git-for-Windows6")

#### 7. Add git to System path: 

- Enter env from Windows search charm, then click Edit the System Environment Variables

![Git-for-Windows7](./images/fr0101-06_Git-for-Windows7.png "Git-for-Windows7")

- Click Environment Variables on System Properties window

![Git-for-Windows8](./images/fr0101-06_Git-for-Windows8.png "Git-for-Windows8")

-In the System (not user) Variables section click Path and then the Edit button

![Git-for-Windows9](./images/fr0101-06_Git-for-Windows9.png "Git-for-Windows9")

- Click the New button, then add:

```
C:\Program Files\Git\bin
```

![Git-for-Windows10](./images/fr0101-06_Git-for-Windows10.png "Git-for-Windows10")

- Then click the OK button and close the next 2 windows

- Close the git bash window

----
### 7. Open or Install VSCode  0:10
----

```
https://code.visualstudio.com/download
```

![VSCode](./images/fr0101-07_VSCode.png "VSCode")

#### 1. Accept **all the defaults**

![VSCode](./images/fr0101-07_VSCode1.png "VSCode")

#### 2. Pin it to Task Bar

![VSCode2](./images/fr0101-07_VSCode2.png "VSCode2")


#### 3. Open VSCode and Install Extensions

![VSCode3](./images/fr0101-07_VSCode3.png "VSCode3")

#### 4. GitLens  -- Supercharged

![VSCode4](./images/fr0101-07_VSCode4.png "VSCode4")

#### 5. Prettier

![VSCode5](./images/fr0101-07_VSCode5.png "VSCode5")

#### 6. Live Server

![VSCode6](./images/fr0101-07_VSCode5-1.png "VSCode6")

#### 7. React Snippets

![VSCode6](./images/fr0101-07_VSCode6.png "VSCode6")

![VSCode6a](./images/fr0101-07_VSCode6a.png "VSCode6a")

#### 8. Change default terminal and add Autosave

- Using File Explorer create or edit settings.json: 

```
 C:\Users\Local_Admin\AppData\Roaming\Code\User\settings.json
```

- Delete all lines and Add these lines:

```
{
    "files.autoSave": "afterDelay",

    "terminal.integrated.profiles.windows": {
        "Git-Bash": {
        "path": "C:\\Program Files\\Git\\bin\\bash.exe",
        "args": ["-l"]
        }    
    },

    "terminal.integrated.defaultProfile.windows": "Git-Bash",

    "files.associations": {
        "*.njs": "javascript"
    }
}
```
 
![VSCode11](./images/fr0101-07_VSCode11.png "VSCode11")

![VSCode11a](./images/fr0101-07_VSCode11a.png "VSCode11a")

#### 9. From VSCode open a new Terminal

![VSCode11b](./images/fr0101-07_VSCode11b.png "VSCode11b")

- This is your bash terminal

![VSCode11c](./images/fr0101-07_VSCode11c.png "VSCode11c")

#### 10. Close VSCode

----
### 8. Clone myProject 0:05
----
#### 1. Using File Explorer 

- Navigate to repos folder, right click and select Git Bash here


![Open-git-bash](./images/fr0101-08_Open-git-bash.png "Open-git-bash")

![Open-git-bash](./images/fr0101-08_Open-git-bash1.png "Open-git-bash")

#### 2. Clone myProject from github into the local repos folder

- Copy to Notpad for editing:

```
git clone github-mick:mickeymouse/myProject.git
```

- Change:

    - github-mick to github-(your initials) that you created in step 1.1.3 above

    - mickeymouse to (your github account name)

    - Copy to git-bash

![Clone-from-GitHub](./images/fr0101-08_Clone-from-GitHub.png "Clone-from-GitHub")

#### 3. Open myProject in VScode

- Remember captialization counts

```
cd myProject
```
```
code .
```

![Open-in-VsCode](./images/fr0101-08_Open-in-VsCode.png "Open-in-VsCode")

#### 4. Trust the authors

![Trust-authors](./images/fr0101-08_Trust-authors.png "Trust-authors")

#### 5. Close the Welcome window

![Close-welcome](./images/fr0101-08_Close-welcome.png "Close-welcome")


#### 6. Click File.. then Save Workspace as: myProject.code-workspace


![VSCode9](./images/fr0101-08_VSCode9.png "VSCode9")

![VSCode9a](./images/fr0101-08_VSCode9a.png "VSCode9a")

----
### 9. Markdown Preview Test 0:05
----
#### 1.  Open MyProject in VSCode and click on the ReadMe.md file and add these lines:

```
    1. My first update was changed locally.

    2. I previewed it in VSCode and Chrome.
```

![Markdown-Preview](./images/fr0101-09_Markdown-Preview.png "Markdown-Preview")

![Markdown-Preview2](./images/fr0101-09_Markdown-Preview2.png "Markdown-Preview2")

#### 2. Click View.. Command Palette and type: >Markdown: Open Preview to the Side, your preview will display.

![Markdown-Preview3](./images/fr0101-09_Markdown-Preview3.png "Markdown-Preview3")

![Markdown-Preview4](./images/fr0101-09_Markdown-Preview4.png "Markdown-Preview4")

#### 3. From File Explorer right click on Readme.md then Open With and navigate to Chrome.exe, your preview will display.

![Markdown-Preview5](./images/fr0101-09_Markdown-Preview5.png "Markdown-Preview5")

![Markdown-Preview6](./images/fr0101-09_Markdown-Preview6.png "Markdown-Preview6")

----
### 10. From VSCode push and pull with GitHub 0:10
----
#### 1. From VSCode.. Click the Control Source icon with the number of changes. In this case there are 2 files that have been changed.

![Github-push](./images/fr0101-10_Github-push.png "Github-push")

#### 2. In the Message textbox, type: 

```
Added Workspace and Updated Readme.md
```

![Github-push-1](./images/fr0101-10_Github-push-1.png "Github-push-1")

![Github-push-1a](./images/fr0101-10_Github-push-1a.png "Github-push-1a")

#### 3. If this shows then, Select Always at the There are no staged changes... box 

![Github-always](./images/fr0101-10_Github-always.png "Github-always") 

--- Fix needed show Commit Button
#### 4. Click on the Commit checkmark above the Message textbox

![Github-push-2](./images/fr0101-10_Github-push-2.png "Github-push-2")

--- Fix needs picture of Yes not No
#### 5. If this shows then, Select Yes at the Git fetch box

![Github-no](./images/fr0101-10_Github-no.png "Github-no")

#### 6. Click the Sync Changes button to push to github

![Github-push-3](./images/fr0101-10_Github-push-3.png "Github-push-3")

#### 7. Login to GitHub and select the myProject repository then click Readme.md, it should be updated.

![Github-push-4](./images/fr0101-10_Github-push-4.png "Github-push-4")

#### 8. Modify Readme.md in Github by adding these lines:

- Remember the pencil!

```
3. I updated it in GitHub.

4. I pulled it to my local repo using VScode
```

![Github-push-5](./images/fr0101-10_Github-push-5.png "Github-push-5")

--- Fix needed Committ Changes Button has moved new pict
#### 9. Commit changes

- Go to the bottom of the edit page to the Commit Changes section.

- A description is required: 

```
Update README.md added 3. and 4.
```

- Click commit Changes

![Github-push-6](./images/fr0101-10_Github-push-6.png "Github-push-6")

![Github-push-6a](./images/fr0101-10_Github-push-6a.png "Github-push-6a")

#### 10. Click the Sync Changes button to push to github

![Github-push-7](./images/fr0101-10_Github-push-7.png "Github-push-7")

#### 11. The Github changes will now appear in the Readme.md file. 

![Github-push-8](./images/fr0101-10_Github-push-8.png "Github-push-8")


--- Fix needed show picture of push / pull alert see Snagit
----
### 11. Install Node Version Selector for Windows 0:05

----
#### 1. Close VSCode

<div class="notice-warning">
  <div class="notice-warning-header">
    Warning: Be sure to CLOSE VSCode before installing NVS
  </div>
</div>

#### 2. To download NVS browse to this URL and click to open the downloaded .msi file: 

```
https://github.com/jasongin/nvs/releases/download/v1.6.0/nvs-1.6.0.msi
```

![Nodejs-install-0](./images/fr0101-11_Nodejs-install-0.png "Nodejs-install-0")

#### 3. From your Downloads folder click the .msi file to Install nvs as follows:

![Nodejs-install-1](./images/fr0101-11_Nodejs-install-1.png "Nodejs-install-1")

![Nodejs-install-1](./images/fr0101-11_Nodejs-install-1-1.png "Nodejs-install-1")

![Nodejs-install-1](./images/fr0101-11_Nodejs-install-1-2.png "Nodejs-install-1")

![Nodejs-install-1](./images/fr0101-11_Nodejs-install-1-3.png "Nodejs-install-1")

![Nodejs-install-1](./images/fr0101-11_Nodejs-install-1-4.png "Nodejs-install-1")

![Nodejs-install-1](./images/fr0101-11_Nodejs-install-2.png "Nodejs-install-1")

#### 4. Open Windows command as Administrator 

![Nodejs-install-1](./images/fr0101-11_Nodejs-install-2-1.png "Nodejs-install-1")

![Nodejs-install-1](./images/fr0101-11_Nodejs-install-2-2.png "Nodejs-install-1")

![Nodejs-install-1](./images/fr0101-11_Nodejs-install-2-3.png "Nodejs-install-1")

- Choose the latest EVEN numbered release. To see the version list enter:

```
 nvs menu
```

--- Fix needed new pict of versions see snagit
![Nodejs-install-check](./images/fr0101-11_Nodejs-install-6.png "Nodejs-install-check")

- Add and use the latest EVEN Node Version i.e. 18

```
    nvs add 20
```
```
    nvs use 20
```
```    
    nvs link
```

- nvs link sets version 20 to default

--- Fix Needed new picture
![Nodejs-install-check](./images/fr0101-11_Nodejs-install-3.png "Nodejs-install-check")


#### 5. Test from Windows command prompt:

```
node --version
```
```
npm --version
```

--- Fix Needed new picture
![Nodejs-install-check](./images/fr0101-11_Nodejs-install-4.png "Nodejs-install-check")

- then close Windows Command window

----
### 12. Install MySql for Windows 0:45
----
#### 1. Browse to: 

```
dev.mysql.com/downloads
```

- then click: MySql Installer for Windows

--- Fix needed new pict Snagit
![MySQL-installer](./images/fr0101-12_MySQL-installer.png "MySQL-installer")


#### 2. Choose the MySQL version: 

<div class="notice-tip">
  <div class="notice-tip-header">
    Note: Do not choose the web version.
  </div>
</div>

--- Fix needed new pict Snagit
![MySQL-community](./images/fr0101-12_MySQL-community.png "MySQL-community")

#### 3. Click on "No thanks, just start my download"

![MySQL-no-thanks](./images/fr0101-12_MySQL-no-thanks.png "MySQL-no-thanks")

- Then click on the downloaded .msi file to start 

- If you are presented with the follow, click No

![MySQL-custom](./images/fr0101-12_MySQL-mandatory.png "MySQL-custom")

#### 4. Choose Setup Type: Full

--- Fix needed new pict Snagit
![MySQL-custom](./images/fr0101-12_MySQL-custom.png "MySQL-custom")

#### 5. Select Products 

- MySQL Server
- MySQL Workbench
- MySQL Shell
- Connector/ODBC x64
- Connector/J
- MySQL Documentation
- Samples and Examples

#### 6. Select from the "Available Products" column

- then click the +'s to reach the product 

- then click the right pointing arrow in the middle column

- your product will be shown in the Products to be Installed column.

--- Fix needed new pict Snagit
![MySQL-select-products](./images/fr0101-12_MySQL-select-products.png "MySQL-select-products")

![MySQL-select-products-1](./images/fr0101-12_MySQL-select-products-1.png "MySQL-select-products-1")

![MySQL-select-products-2](./images/fr0101-12_MySQL-select-products-2.png "MySQL-select-products-2")

#### 7. Product Configuration

--- Fix needed new pict Snagit
![MySQL-product-configuration](./images/fr0101-12_MySQL-product-configuration.png "MySQL-product-configuration")

![MySQL-product-configuration-1](./images/fr0101-12_MySQL-product-configuration-1.png "MySQL-product-configuration-1")

![MySQL-product-configuration-2](./images/fr0101-12_MySQL-product-configuration-2.png "MySQL-product-configuration-2")

- Use the password: 

```
FormR!1234
```

![MySQL-product-configuration-3](./images/fr0101-12_MySQL-product-configuration-3.png "MySQL-product-configuration-3")

<div class="notice-tip">
  <div class="notice-tip-header">
    Note: Remember to write your passwords in a safe place.
  </div>  
</div>


![MySQL-product-configuration-4](./images/fr0101-12_MySQL-product-configuration-4.png "MySQL-product-configuration-4")

![MySQL-product-configuration-5](./images/fr0101-12_MySQL-product-configuration-5a.png "MySQL-product-configuration-5")

![MySQL-product-configuration-5](./images/fr0101-12_MySQL-product-configuration-5.png "MySQL-product-configuration-5")

![MySQL-product-configuration-6](./images/fr0101-12_MySQL-product-configuration-6a.png "MySQL-product-configuration-6")

- Use the password: 

```
FormR!1234
```

![MySQL-product-configuration-6](./images/fr0101-12_MySQL-product-configuration-6a1.png "MySQL-product-configuration-6")

<div class="notice-tip">
  <div class="notice-tip-header">
    Note: Remember to write your passwords in a safe place.
  </div>  
</div>


![MySQL-product-configuration-6](./images/fr0101-12_MySQL-product-configuration-6a2.png "MySQL-product-configuration-6")

![MySQL-product-configuration-6](./images/fr0101-12_MySQL-product-configuration-6a3.png "MySQL-product-configuration-6")


![MySQL-product-configuration-6](./images/fr0101-12_MySQL-product-configuration-6b.png "MySQL-product-configuration-6")

![MySQL-product-configuration-6](./images/fr0101-12_MySQL-product-configuration-6c.png "MySQL-product-configuration-6")



- MySQL Shell and MySQL WorkBench are automatically opened.

![MySQL-shell-workbench](./images/fr0101-12_MySQL-shell-workbench.png "MySQL-shell-workbench")

#### 8. Workbench

- Select the Workbench window and click Local Instance 

![MySQL-workbench-login](./images/fr0101-12_MySQL-workbench-login.png "MySQL-workbench-login")

- Enter credentials

- Use the password: 

```
FormR!1234
```

- Click Save password in vault

![MySQL-workbench-login-1](./images/fr0101-12_MySQL-workbench-login-1.png "MySQL-workbench-login-1")


<div class="notice-tip">
  <div class="notice-tip-header">
    Note: Remember to write your passwords in a safe place.
  </div>  
</div>

#### 9. Create and Grant Privileges to a new user account: nimdas with host %


<div class="notice-tip">
  <div class="notice-tip-header">
    Note: root@localhost has all rights and nimdas@% will have all rights.
  </div>  
</div>
 

- Open New Query tab

![MySQL-workbench-nimdas](./images/fr0101-12_MySQL-workbench-nimdas.png "MySQL-workbench-nimdas")

- Paste the following

```
CREATE USER 'nimdas'@'%' IDENTIFIED WITH mysql_native_password BY 'FormR!1234
';
GRANT ALL PRIVILEGES ON *.* TO 'nimdas'@'%';
SELECT user,authentication_string,plugin,host FROM mysql.user;
```

![MySQL-workbench-nimdas1](./images/fr0101-12_MySQL-workbench-nimdas1.png "MySQL-workbench-nimdas1")

- Click the execute icon

![MySQL-workbench-nimdas2](./images/fr0101-12_MySQL-workbench-nimdas2.png  "MySQL-workbench-nimdas2")

#### 10. Select the MySql Shell window

- Enter:  
```
\connect root@localhost
```
- Password: 
```
FormR!1234
```
- Enter: Y to save password
```
Y
```

![MySQL-shell-login](./images/fr0101-12_MySQL-shell-login.png "MySQL-shell-login")

#### 11. Shell SHOW DATABASES

Enter: 

```
\sql SHOW DATABASES;  
```
- Don't forget the \ and ; 

![MySQL-shell-show-databases](./images/fr0101-12_MySQL-shell-show-databases.png "MySQL-shell-show-databases")


----
### 13. Install Bitvise ssh client 0:05
----
#### 1. Install Bitvise from: 

```
https://bitvise.com/ssh-client-download
```

![Bitvise-download](./images/fr0101-13_Bitvise-download.png "Bitvise-download")

![Bitvise-download-1](./images/fr0101-13_Bitvise-download-1.png "Bitvise-download-1")

![Bitvise-download-2](./images/fr0101-13_Bitvise-download-2.png "Bitvise-download-2")

![Bitvise-download-3](./images/fr0101-13_Bitvise-download-3.png "Bitvise-download-3")

![Bitvise-start](./images/fr0101-13_Bitvise-start.png "Bitvise-start")

#### 2. Configure Bitvise

<div class="notice-tip">
  <div class="notice-tip-header">
    These 2 configuration changes will allow Bitvise to cleanly logout when you close your terminal and SFTP windows.
  </div>  
</div>


- Start Bitvise then click the Options tab then the check box "Logout when session activity is over".


![Bitvise-Options-Logout](./images/fr0101-13_Bitvise-options-logout.png "Bitvise-Options-Logout")

- Click on the Terminal Tab and choose "Always"

![Bitvise-terminal-always](./images/fr0101-13_Bitvise-terminal-always.jpg "Bitvise-terminal-always")

- Exit Bitvise to Save your changes to the Default profile.

![Bitvise-Exit](./images/fr0101-13_Bitvise-exit.jpg "Bitvise-Exit")

----
<div class="notice-success">
  <div class="notice-success-header">
    Congratulations! Your Developer Workstation is setup.
  </div>
</div>

----

 - After all installations on a new Windows 10 machine, 7 GB was added to Drive C:.

----
<!-- ------------------------------------------------------------------------- -->

<div class="page-back">

[BACK - formR Introduction](/_home.md.md)
</div><div class="page-next">

[Test NodeJS - NEXT](/Setup/fr0102_Test-Node.md)
</div>

<!-- ------------------------------------------------------------------------- -->
