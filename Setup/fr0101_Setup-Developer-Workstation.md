<!-- ------------------------------------------------------------------------- -->

<div class="page-back">

[BACK - Create SSH Keys](/Setup/fr0050_Setup-SSH-Key-Files.md)
</div><div class="page-next">

[Create a Simple NodeJS App - NEXT](/Setup/fr0102_Simple-Node-Apps.md)
</div>

<!-- ------------------------------------------------------------------------- -->

## Instructions for setting up a MERN stack Development Workstation

#### Introduction
The following steps create the development environment on your workstation for developing an MERN stack (MYSql, Express, React and Node) application. You will access a repository on github and modify it, run it and push changes back to github. We will be using an empty 'Windows Pro N' VM in these instructions. You should be able to use any workstation. Just follow the steps.

#### Important Note about names and capitalization

- In this tutorial please be careful to use the exact spelling and capitalization. You will be using Windows, Unix and GitBash command prompts. Improper captialization will cause commands to fail. Some examples are: Local_Admin, myProject, repos, remotes and .ssh.
<br/>

### 1. Create a new user, Local_Admin on your workstation.

- This account will be used througout the documentation. 

- IMPORTANT--If you use another account, it cannot contain spaces in the name. This tutorial will fail, if spaces are found in the Windows user account name.

1. Login to your Windows account

![Windows-Login](./images/fr0101-00_Windows-Login.png "Windows-Login")

2. Search for Control Panel

![Windows-Controlpanel](./images/fr0101-00_Windows-Controlpanel.png "Windows-Controlpanel")

3. Click User Accounts

![Windows-Useraccounts](./images/fr0101-00_Windows-Useraccounts.png "Windows-Useraccounts")

4. Click Change Account Type

![Windows-Changeaccounttype](./images/fr0101-00_Windows-Changeaccounttype.png "Windows-Changeaccounttype")

5. Click Add New User...

![Windows-Addnewuser](./images/fr0101-00_Windows-Addnewuser.png "Windows-Addnewuser")

6. Click the (+) Add someone else...

![Windows-Addsomeoneelse](./images/fr0101-00_Windows-Addsomeoneelse.png "Windows-Addsomeoneelse")

7. Click I don't have this person's...

![Windows-Idonthave](./images/fr0101-00_Windows-Idonthave.png "Windows-Idonthave")

8. Click Add a user without...

![Windows-Addauserwithout](./images/fr0101-00_Windows-Addauserwithout.png "Windows-Addauserwithout")

9. Create a user by filling in the information for:

```
 User name = Local_Admin

 password = FormR!1234
```

![Windows-Createauser](./images/fr0101-00_Windows-Createauser.png "Windows-Createauser")

10. Go to Control Panel -> User Accounts -> Change Account Type and select the Local_Admin account

![Windows-Selectlocaladmin](./images/fr0101-00_Windows-Selectlocaladmin.png "Windows-Selectlocaladmin")

11. Click Change Account Type

![Windows-Changelocaladmintype](./images/fr0101-00_Windows-Changelocaladmintype.png "Windows-Changelocaladmintype")

12. Click Administrator radio button and then the Change Account Type button

![Windows-Selectadministrator](./images/fr0101-00_Windows-Selectadministrator.png "Windows-Selectadministrator")

![Windows-Selectadministrator-1](./images/fr0101-00_Windows-Selectadministrator-1.png "Windows-Selectadministrator-1")

13. Sign out

![Windows-Signout](./images/fr0101-00_Windows-Signout.png "Windows-Signout")

14. Sign in as Local_Admin

![Windows-Signin](./images/fr0101-00_Windows-Signin.png "Windows-Signin")


### 2. Install any updates to your workstation.

![Windows-Update](./images/fr0101-01_Windows-Update.png "Windows-Update")

### 3. Create 3 folders, change View Options,  Setup ssh and Create keys

1. In C:\ add repos and remotes 

```
 'repos' (local copies of your gitHub repositories files)
 'remotes' (local copies of remote server files)
```

![Create-folders](./images/fr0101-02_Create-folders.png "Create-folders")

2. In C:\users\Local_Admin\ add .ssh 

```
 '.ssh' (holds your ssh keys related files)
```

![Create-folders2](./images/fr0101-02_Create-folders2.png "Create-folders2")

3. Change View Options in File Explorer

```
Enable Extentions and Hidden Files
```

![Change-View-Options](./images/fr0101-02_Change-View-Options.png "Change-View-Options")

4. Test if OpenSSH client is installed.

```
From DOS command prompt run ssh.
```

5.  If OpenSSH client is Not installed

![OpenSSH-not-installed](./images/fr0101-02_OpenSSH-not-installed.png "OpenSSH-not-installed")

- Install OpenSSH in Apps & Features - Optional Features

![Install-OpenSSH1](./images/fr0101-02_Install-OpenSSH1.png "Install-OpenSSH1")

![Install-OpenSSH2](./images/fr0101-02_Install-OpenSSH2.png "Install-OpenSSH2")

![Install-OpenSSH3](./images/fr0101-02_Install-OpenSSH3.png "Install-OpenSSH3")

6. OpenSSH client is installed

![OpenSSH-is-installed](./images/fr0101-02_OpenSSH-is-installed.png "OpenSSH-is-installed")

7. Create 3 ssh keys. These keys will be used for GitHub, your Cloud Provider and your Remote server. Run from the Windows command prompt

```
Format:

ssh-keygen -t rsa -f
"<local user folder>/.ssh/
<key owner name>@<host name>_<host user name>_v<date>_key"
-C "<key owner name>@<host name>_<host user name>_v<date>"

Example: 

ssh-keygen -t rsa -f "c:/Users/Local_Admin/.ssh/mickey.mouse@github_mm_v210713_key" -C "mickey.mouse@github_mm_v210713"

```

```
In the following change the following to your info:

- "mickey.mouse" to <your Key Owner Name> 
- "mm" to your <Host User Name> i.e. kff
- "v210713" to the <current date>
```

8. Key pairs for Github:

```
ssh-keygen -t rsa -f "c:/Users/Local_Admin/.ssh/mickey.mouse@github_mm_v210713_key" -C "mickey.mouse@github_mm_v210713"
```

![Create New ssh key1](./images/fr0101-03_Create-New-ssh-key1.png "Create New ssh key1")

9. Key pairs for Cloud Provider:

```
ssh-keygen -t rsa -f "c:/Users/Local_Admin/.ssh/mickey.mouse@Vultr_mm_v210713_key" -C "mickey.mouse@Vultr_mm_v210713"
```

![Create New ssh key2](./images/fr0101-03_Create-New-ssh-key2.png "Create New ssh key2")

10. Key pairs for access to Remote Server on Cloud Provider:

```
Change "FormR1-Vultr_nimda" below to your VM Instance name and login

ssh-keygen -t rsa -f "c:/Users/Local_Admin/.ssh/mickey.mouse@Formr1-Vultr_nimda_v210713_key" -C "mickey.mouse@Formr1-Vultr_nimda_v210713"
```

![Create New ssh key3](./images/fr0101-03_Create-New-ssh-key3.png "Create New ssh key3")

11. View created key files:

![Create New ssh key4](./images/fr0101-03_Create-New-ssh-key4.png "Create New ssh key4")

### 4. Install or open Chrome browser

1. Download and install Chrome from:

```
https://google.com/chrome
```

2. Install Chrome Extensions

```
https://chrome.google.com/webstore/category/extensions?hl=en-US
```

![Chrome-extensions](./images/fr0101-03_Chrome-extensions.png "Chrome-extensions")

3. Add Markdown Preview Plus

![Chrome-extensions1](./images/fr0101-03_Chrome-extensions1.png "Chrome-extensions1")

4. Allow access to file URLs

```
chrome://extensions/?id=febilkbfcbhebfnokafefeacimjdckgl
```

![Chrome-extensions2](./images/fr0101-03_Chrome-extensions2.png "Chrome-extensions2")

5. Add React Developers Tools

```
https://chrome.google.com/webstore/category/extensions?hl=en-US
```

![Chrome-extensions3](./images/fr0101-03_Chrome-extensions3.png "Chrome-extensions3")

6. Check the installations

```
chrome://extensions/
```

![Chrome-extensions4](./images/fr0101-03_Chrome-extensions4.png "Chrome-extensions4")

### 5. Create an account or sign into GitHub then Add your ssh key.

- GitHub

```
https://github.com
```

![Login to Github](./images/fr0101-04_Login-to-github.png "Login to GitHub")

- Add your Github ssh key from your .ssh folder to your github account

```
1. Login to your github account:

 https://github.com

2. Navigate to:

 https://github.com/settings/ssh

3. Click New SSH Key button

```

![Add New ssh key](./images/fr0101-04_Add-New-ssh-key.png "Add New ssh key")

![Add New ssh key-1](./images/fr0101-04_Add-New-ssh-key-1.png "Add New ssh key-1")

```
4. In notepad open your github public key from your .ssh folder.

5. Copy the contents to the clipboard.
```

![Add New ssh key-2](./images/fr0101-04_Add-New-ssh-key-2.png "Add New ssh key-2")

![Add New ssh key-3](./images/fr0101-04_Add-New-ssh-key-3.png "Add New ssh key-3") 

```
6. Paste the clipboard contents into the Key box in the github SSH Keys/ Add someone elseow.

7. Copy the last part of the key and paste it into the Title box.

8. Click the Add SSH key button when finished.
```

![Add New ssh key-4](./images/fr0101-04_Add-New-ssh-key-4.png "Add New ssh key-4")

![Add New ssh key-5](./images/fr0101-04_Add-New-ssh-key-5.png "Add New ssh key-5")




- Create a new repository: 'myProject'.

```
Browse to:

https://github.com/new

Add Repository Name "myProject", select Private and check ReadMe file, then click Create Repository.
```

![GitHub-myProject](./images/fr0101-04_GitHub-myProject.png "GitHub-myProject")

- Edit the Readme.md file

```
Click the pencil
```

![GitHub-myProject-readme](./images/fr0101-04_GitHub-myProject-readme.png "GitHub-myProject-readme")

```
Change to:

# myProject was created on mm/dd/yyyy.
```

![GitHub-myProject-readme2](./images/fr0101-04_GitHub-myProject-readme2.png "GitHub-myProject-readme2")

- Commit changes

```
1. Go to the bottom of the edit page to the Commit Changes section.

2. A description is required: Update README.md

3. Click commit Changes
```

![GitHub-myProject-readme3](./images/fr0101-04_GitHub-myProject-readme3.png "GitHub-myProject-readme3")

![GitHub-myProject-readme4](./images/fr0101-04_GitHub-myProject-readme4.png "GitHub-myProject-readme4")

### 6. Configure ssh Access to Github

- Create a Host for github connection in the .ssh/config file.

```
Create .ssh/config file in C:/users/Local_Admin/.ssh. Make sure it is saved without the .txt extention, then open with notepad and add the following:

Be sure to change the following:
- "github-mm"  to "github-<your initials>"
- IdentityFile to the name of your github key file in C:/Users/Local_Admin/.ssh

Host github-mm
    HostName       github.com
    IdentityFile   C:/Users/Local_Admin/.ssh/mickey.mouse@github_mm_v210713_key
    User           git
```

![Add Host to config](./images/fr0101-03_Add-host-to-config.png "Add Host to config")

- From the DOS command window, test the connection to github.

```
ssh github-mm

Note: On the first try when prompted enter "yes" 
```

![Test ssh to github-1st-yes](./images/fr0101-03_Test-ssh-to-github-1st-yes.png "Test ssh to github-1st-yes") 

![Test ssh to github](./images/fr0101-03_Test-ssh-to-github.png "Test ssh to github")

### 7. Download Git, if not already installed

- Download from
```
 https://git-scm.com/download/win
```

![Git-for-Windows](./images/fr0101-06_Git-for-Windows.png "Git-for-Windows")

- Allow changes

![Git-for-Windows1](./images/fr0101-06_Git-for-Windows1.png "Git-for-Windows1")

- Select all the default values and install

![Git-for-Windows2](./images/fr0101-06_Git-for-Windows2.png "Git-for-Windows2")

- Finish Install

![Git-for-Windows3](./images/fr0101-06_Git-for-Windows3.png "Git-for-Windows3")

- Open Git Bash

![Git-for-Windows4](./images/fr0101-06_Git-for-Windows4.png "Git-for-Windows4")

- Add Username for github

```
Change Mickey Mouse to <your name>:

git config --global user.name = "Mickey Mouse"
```

![Git-for-Windows5](./images/fr0101-06_Git-for-Windows5.png "Git-for-Windows5")


- Add User Email for github

```
Change mickey.mouse@gmail.com to <your email in github>:

git config --global user.email = "mickey.mouse@gmail.com"
```

![Git-for-Windows6](./images/fr0101-06_Git-for-Windows6.png "Git-for-Windows6")


### 8. Open or Install VSCode

- Install from

```
https://code.visualstudio.com/download
```

![VSCode](./images/fr0101-07_VSCode.png "VSCode")

- Accept all the defaults

![VSCode](./images/fr0101-07_VSCode1.png "VSCode")

- Pin it to Task Bar

![VSCode2](./images/fr0101-07_VSCode2.png "VSCode2")


- Open VSCode and Install Extensions

![VSCode3](./images/fr0101-07_VSCode3.png "VSCode3")

    - GitLens  -- Supercharged

![VSCode4](./images/fr0101-07_VSCode4.png "VSCode4")

    - Prettier

![VSCode5](./images/fr0101-07_VSCode5.png "VSCode5")

    - React Snippets

![VSCode6](./images/fr0101-07_VSCode6.png "VSCode6")

![VSCode6a](./images/fr0101-07_VSCode6a.png "VSCode6a")


- Change default terminal and add Autosave

- Using Notepad, edit: 

```
 C:\Users\Local_Admin\AppData\Roaming\Code\User\settings.json
```

-Delete all line and Add these lines:

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

- From VSCode open a new Terminal

![VSCode11b](./images/fr0101-07_VSCode11b.png "VSCode11b")

![VSCode11c](./images/fr0101-07_VSCode11c.png "VSCode11c")

- Close VSCode

### 9. Clone myProject

- Using File Explorer open git bash in c/repos folder

```
Navigate to repos, right click and Open Git Bash here
```

![Open-git-bash](./images/fr0101-08_Open-git-bash.png "Open-git-bash")

- Clone myProject from github into the local repos folder

```
Change:
    github-mm to github-<your handle> that you created above
    mickeymouse-gmail to <your github account name>

git clone github-mm:mickeymouse-gmail/myProject.git
```

![Clone-from-GitHub](./images/fr0101-08_Clone-from-GitHub.png "Clone-from-GitHub")

- Open myProject in VScode

```
cd myProject

code .

-- Remember captialization counts
```

![Open-in-VsCode](./images/fr0101-08_Open-in-VsCode.png "Open-in-VsCode")

- Trust the authors

![Trust-authors](./images/fr0101-08_Trust-authors.png "Trust-authors")

- Close the VSCode Welcome window

![Close-welcome](./images/fr0101-08_Close-welcome.png "Close-welcome")


```
Click File.. 

Save Workspace as: myProject.code-workspace
```

![VSCode9](./images/fr0101-08_VSCode9.png "VSCode9")

![VSCode9a](./images/fr0101-08_VSCode9a.png "VSCode9a")


### 10. Markdown Preview test

- Open MyProject in VSCode and click on the ReadMe.md file and add these lines:
```
    1. My first update was changed locally.

    2. I previewed it in VSCode and Chrome.
```

![Markdown-Preview](./images/fr0101-09_Markdown-Preview.png "Markdown-Preview")

![Markdown-Preview2](./images/fr0101-09_Markdown-Preview2.png "Markdown-Preview2")

- Click View.. Command Palette and type: >Markdown: Open Preview to the Side, your preview will display.

![Markdown-Preview3](./images/fr0101-09_Markdown-Preview3.png "Markdown-Preview3")

![Markdown-Preview4](./images/fr0101-09_Markdown-Preview4.png "Markdown-Preview4")

- From File Explorer right click on Readme.md then Open With and navigate to Chrome.exe, your preview will display.

![Markdown-Preview5](./images/fr0101-09_Markdown-Preview5.png "Markdown-Preview5")

![Markdown-Preview6](./images/fr0101-09_Markdown-Preview6.png "Markdown-Preview6")

### 11. From VSCode push and pull with GitHub

- From VSCode.. Click the Control Source icon with the number of changes. In this case there are 2 files that have been changed.

![Github-push](./images/fr0101-10_Github-push.png "Github-push")

- In the Message textbox, type: 

```
Added Workspace and Updated Readme.md
```

![Github-push-1](./images/fr0101-10_Github-push-1.png "Github-push-1")

![Github-push-1a](./images/fr0101-10_Github-push-1a.png "Github-push-1a")

- If this shows then, Select Always at the There are no staged changes... box 

![Github-always](./images/fr0101-10_Github-always.png "Github-always") 

- Click on the Commit checkmark above the Message textbox

![Github-push-2](./images/fr0101-10_Github-push-2.png "Github-push-2")

- If this shows then, Select Yes at the Git fetch box

![Github-no](./images/fr0101-10_Github-no.png "Github-no")

-  From the Source Control menu, click the three dots (...) More menu, and click Push.

![Github-push-3](./images/fr0101-10_Github-push-3.png "Github-push-3")

- Login to GitHub and select the myProject repository then click Readme.md, it should be updated.

![Github-push-4](./images/fr0101-10_Github-push-4.png "Github-push-4")

- Modify Readme.md in Github by adding these lines:
(Remember the pencil!)

```
3. I updated it in GitHub.

4. I pulled it to my local repo using VScode
```

![Github-push-5](./images/fr0101-10_Github-push-5.png "Github-push-5")

- Commit changes

```
1. Go to the bottom of the edit page to the Commit Changes section.

2. A description is required: Update README.md added 3. and 4.

3. Click commit Changes
```

![Github-push-6](./images/fr0101-10_Github-push-6.png "Github-push-6")

![Github-push-6a](./images/fr0101-10_Github-push-6a.png "Github-push-6a")

- In VSCode, From the Source Control menu, click the three dots (...) More menu, and click Pull.

![Github-push-7](./images/fr0101-10_Github-push-7.png "Github-push-7")

- The Github changes will now appear in the Readme.md file. 

![Github-push-8](./images/fr0101-10_Github-push-8.png "Github-push-8")

### 12. Install Node for Windows

- Be sure to CLOSE VSCode before installing Node

- To download browse to: 

```
nodejs.org/en/
```

- Select the version that is Recommended for Most Users

![Nodejs-install-0](./images/fr0101-11_Nodejs-install-0.png "Nodejs-install-0")

- Download and install using all the defaults.

![Nodejs-install-1](./images/fr0101-11_Nodejs-install-1.png "Nodejs-install-1")

- Allow changes

![Git-for-Windows1](./images/fr0101-06_Git-for-Windows1.png "Git-for-Windows1")

- Finish

![Nodejs-install-2](./images/fr0101-11_Nodejs-install-2.png "Nodejs-install-2")

- Test from Windows command prompt:

```
    node --version
    npm --version
```
![Nodejs-install-check](./images/fr0101-11_Nodejs-install-check.png "Nodejs-install-check")

### 13. Install MySql for windows

- Browse to: 

```
dev.mysql.com/downloads

then click: MySql Installer for Windows
```

![MySQL-installer](./images/fr0101-12_MySQL-installer.png "MySQL-installer")


- Choose the version: 

```
mysql-installer-community-x.x.xx.x.msi  (Do not choose the web version.)
```

![MySQL-community](./images/fr0101-12_MySQL-community.png "MySQL-community")

- Select No, thanks, just start my download

![MySQL-no-thanks](./images/fr0101-12_MySQL-no-thanks.png "MySQL-no-thanks")

- Choose Setup Type: Custom

![MySQL-custom](./images/fr0101-12_MySQL-custom.png "MySQL-custom")

- Select Products 

    - MySQL Server
    - MySQL Workbench
    - MySQL Shell
    - Connector/ODBC
    - Connector/J
    - MySQL Documentation
    - Samples and Examples

- Select from the "Available Products" column, then click the Top arrow to move it to the left column.

![MySQL-select-products](./images/fr0101-12_MySQL-select-products.png "MySQL-select-products")

![MySQL-select-products-1](./images/fr0101-12_MySQL-select-products-1.png "MySQL-select-products-1")

![MySQL-select-products-2](./images/fr0101-12_MySQL-select-products-2.png "MySQL-select-products-2")

![MySQL-select-products-3](./images/fr0101-12_MySQL-select-products-3.png "MySQL-select-products-3")

![MySQL-select-products-4](./images/fr0101-12_MySQL-select-products-4.png "MySQL-select-products-4")

- Product Configuration

![MySQL-product-configuration](./images/fr0101-12_MySQL-product-configuration.png "MySQL-product-configuration")

![MySQL-product-configuration-1](./images/fr0101-12_MySQL-product-configuration-1.png "MySQL-product-configuration-1")

![MySQL-product-configuration-2](./images/fr0101-12_MySQL-product-configuration-2.png "MySQL-product-configuration-2")

![MySQL-product-configuration-3](./images/fr0101-12_MySQL-product-configuration-3.png "MySQL-product-configuration-3")

```
#### !! Remember to write your passwords in a safe place !!
```

![MySQL-product-configuration-4](./images/fr0101-12_MySQL-product-configuration-4.png "MySQL-product-configuration-4")

![MySQL-product-configuration-5](./images/fr0101-12_MySQL-product-configuration-5.png "MySQL-product-configuration-5")

![MySQL-product-configuration-6](./images/fr0101-12_MySQL-product-configuration-6.png "MySQL-product-configuration-6")

- Connect to Server

```
Enter password -> FormR!1234 and click the Check button

#### !! Remember to write your passwords in a safe place !!
```

![MySQL-connect-server](./images/fr0101-12_MySQL-connect-server.png "MySQL-connect-server")

- Windows Service

![MySQL-windows-service](./images/fr0101-12_MySQL-windows-service.png "MySQL-windows-service")

- Apply Configuration

![MySQL-apply-configuration](./images/fr0101-12_MySQL-apply-configuration.png "MySQL-apply-configuration")

![MySQL-apply-configuration-1](./images/fr0101-12_MySQL-apply-configuration-1.png "MySQL-apply-configuration-1")

- Be sure to Click the check boxes for Starting Workbench and Shell in the Installation Complete windows

![MySQL-installation-complete](./images/fr0101-12_MySQL-installation-complete.png "MySQL-installation-complete")

- MySQL Shell and MySQL WorkBench are automatically opened because you clicked the check boxes in the previous step.

![MySQL-shell-workbench](./images/fr0101-12_MySQL-shell-workbench.png "MySQL-shell-workbench")

- Select the Workbench window and click Local Instance 

![MySQL-workbench-login](./images/fr0101-12_MySQL-workbench-login.png "MySQL-workbench-login")

- Enter credentials

![MySQL-workbench-login-1](./images/fr0101-12_MySQL-workbench-login-1.png "MySQL-workbench-login-1")

- In the Query 1 pane enter SHOW DATABASES, then Click the Exceute icon

![MySQL-workbench-show-databases](./images/fr0101-12_MySQL-workbench-show-databases.png "MySQL-workbench-show-databases")

![MySQL-workbench-show-databases-1](./images/fr0101-12_MySQL-workbench-show-databases-1.png "MySQL-workbench-show-databases-1")

- Select the MySql Shell window

```
Enter:  \connect root@localhost

Enter: FormR!1234

Enter: Y to save password

```

![MySQL-shell-login](./images/fr0101-12_MySQL-shell-login.png "MySQL-shell-login")

- Shell SHOW DATABASES

```
Enter: \sql SHOW DATABASES;  ( Don't forget the \ and ; )
```

![MySQL-shell-show-databases](./images/fr0101-12_MySQL-shell-show-databases.png "MySQL-shell-show-databases")

### 14. Install BitVise ssh client

- Install Bitvise from: 

```
https://bitvise.com/ssh-client-download
```

![Bitvise-download](./images/fr0101-13_Bitvise-download.png "Bitvise-download")

![Bitvise-download-1](./images/fr0101-13_Bitvise-download-1.png "Bitvise-download-1")

![Bitvise-download-2](./images/fr0101-13_Bitvise-download-2.png "Bitvise-download-2")

![Bitvise-download-3](./images/fr0101-13_Bitvise-download-3.png "Bitvise-download-3")

![Bitvise-start](./images/fr0101-13_Bitvise-start.png "Bitvise-start")

###    15. Install TextPad

- Install Textpad from: 

```
https://textpad.com/download
```

- Select the latest version then accept the defaults

![Textpad-download](./images/fr0101-14_Textpad-download.png "Textpad-download")

![Textpad-download-1](./images/fr0101-14_Textpad-download-1.png "Textpad-download-1")

![Textpad-download-2](./images/fr0101-14_Textpad-download-2.png "Textpad-download-2")

![Textpad-download-3](./images/fr0101-14_Textpad-download-3.png "Textpad-download-3")

![Textpad-download-4](./images/fr0101-14_Textpad-download-4.png "Textpad-download-4")

![Textpad-download-5](./images/fr0101-14_Textpad-download-5.png "Textpad-download-5")

![Textpad-download-6](./images/fr0101-14_Textpad-download-6.png "Textpad-download-6")

![Textpad-download-7](./images/fr0101-14_Textpad-download-7.png "Textpad-download-7")

![Textpad-download-8](./images/fr0101-14_Textpad-download-8.png "Textpad-download-8")

![Textpad-download-9](./images/fr0101-14_Textpad-download-9.png "Textpad-download-9")

![Textpad-download-10](./images/fr0101-14_Textpad-download-10.png "Textpad-download-10")



### Congratulations! Your Developer Workstation is setup.

 After all installations on a new Windows 10 machine, 26GB was used on Drive C:.

<!-- ------------------------------------------------------------------------- -->

<div class="page-back">

[BACK - Create SSH Keys](/Setup/fr0050_Setup-SSH-Key-Files.md)
</div><div class="page-next">

[Create a Simple NodeJS App - NEXT](/Setup/fr0102_Simple-Node-Apps.md)
</div>

<!-- ------------------------------------------------------------------------- -->