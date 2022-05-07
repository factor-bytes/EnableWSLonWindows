# Enable WSL on Windows 10 or 11

1. Ensure WSL (Windows Subsystem for Linux) check box is checked under "Control Panel > Programs > Turn Windows feature On or Off". If not check the check nox and save. This will enable WSL.

2. Open PowerShell in administrator mode and run the following comand
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
Restart your system

3. Enable virtual Machine. RUn the following command in powershell
```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

3. Download and install WSL kernel update https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

4. Set WSL2 as default. Run following command
```
wsl --set-default-version 2
```
List all Linux ersions installd
```
wsl --list --verbose
```

Setting a specific verion
```
wsl --set-version <distribution name> <versionNumber>
```

5. Run Linux

