# :comet: Windows Setup :comet:

### Chocolately Packages
- Git
- Azure CLI
- Slack
- VScode
- Spotify
- Runelite



### Step 1: Visual Studio Code
##### Installation
1. Download the [Visual Studio Code installer for Windows](https://visualstudio.microsoft.com/downloads/).
2. Once it is downloaded, run the installer (VSCodeUserSetup-{version}.exe). This will only take a minute.
3. By default, VS Code is installed under **C:\Users\{Username}\AppData\Local\Programs\Microsoft VS Code**.
4. Alternatively, you can also download a Zip archive, extract it and run Code from there.

Tip: Setup will add Visual Studio Code to your %PATH%, so from the console you can type 'code .' to open VS Code on that folder. You will need to restart your console after the installation for the change to the %PATH% environmental variable to take effect.

### Step 2: Git for Windows
##### Installation
1. Download the latest [Git for Windows installer](https://gitforwindows.org/).

2. When you've successfully started the installer, you should see the **Git Setup** wizard screen. Follow the **Next** and **Finish** prompts to complete the installation. The default options are pretty sensible for most users.

3. Open a Command Prompt (or Git Bash if during installation you elected not to use Git from the Windows Command Prompt).

4. Run the following commands to configure your Git username and email using the following commands, replacing my name with your own. These details will be associated with any commits that you create:

```powershell
git config --global user.name "Alexander Horning"
git config --global user.email "firstname.lastname@gmail.com"
```


### Step 3: Chocolatey Package Manager for Windows
##### Installation
When installing the software via PowerShell, we must ensure the local Get-ExecutionPolicy is not set to restricted. Chocolately suggests using Bypass to bypass the policy to get things installed or AllSigned for increased security.

1. First, we need to run the Get-ExecutionPolicy. If it returns Restricted, then we need to run one of the two commands below.
```powershell
Set-ExecutionPolicy AllSigned
```
2. Now run the following command in the Windows shell.
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
4. If there are no errors, Chocolatey will be installed. We can verify the installation using the **choco** or **choco -?** command.

### Step 4: GitHub CLI for Windows
##### Installation
This installation requires the package manager Chocolatey. Please refer to previous steps!
1. Run The following chocolatey command.
```powershell
choco install gh
```
2. Authenticate with GitHub CLI
```powershell
gh auth login
```
