# AzurePowerShellAzModule
### Install the Azure PowerShell module
To install for all users run the command below from elevated PowerShell session.  
```
Install-Module -Name Az -AllowClobber -Scope AllUsers
```
### Find your installed version of Azure PowerShell
This command will also tell you if you have mulitiple versions of PowerShell installed.
```
Get-InstalledModule -Name Az -AllVersions
```
### Update the Azure PowerShell module
Because of how the Az module is packaged, the Update-Module command won't update your installation correctly. When you install the Az module, it actually collects and installs all of its dependent submodules, and which provide the cmdlets for each service. That means that to update the Azure PowerShell module, you will need to reinstall, rather than just update. This is done in the same way as installing, but you may need to add the -Force argument:
```
Install-Module -Name Az -AllowClobber -Force
```
