### Visual Studio Code
##### Installation
1. Download the Visual Studio Code installer for Windows.
2. Once it is downloaded, run the installer (VSCodeUserSetup-{version}.exe). This will only take a minute.
3. By default, VS Code is installed under **C:\Users\{Username}\AppData\Local\Programs\Microsoft VS Code**.
4. Alternatively, you can also download a Zip archive, extract it and run Code from there.

Tip: Setup will add Visual Studio Code to your %PATH%, so from the console you can type 'code .' to open VS Code on that folder. You will need to restart your console after the installation for the change to the %PATH% environmental variable to take effect.

### Git for Windows
##### Installation
1. Download the latest [Git for Windows installer](https://gitforwindows.org/).

2. When you've successfully started the installer, you should see the **Git Setup** wizard screen. Follow the **Next** and **Finish** prompts to complete the installation. The default options are pretty sensible for most users.

3. Open a Command Prompt (or Git Bash if during installation you elected not to use Git from the Windows Command Prompt).

4. Run the following commands to configure your Git username and email using the following commands, replacing Emma's name with your own. These details will be associated with any commits that you create:

```powershell
git config --global user.name "Alexander Horning"
git config --global user.email "firstname.lastname@gmail.com"
```
