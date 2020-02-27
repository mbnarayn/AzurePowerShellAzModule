# AzurePowerShellAzModule

Starting in December 2018, the Azure PowerShell Az module is in general release and is now the intended PowerShell module for interacting with Azure. Azure PowerShell Az module replaces the AzureRM module which in turn replaced the original Azure PowerShell (ASM Module) that was intended for interacting with the Azure Classic Deployment model also known as the Azure Service Management model.  The AzureRM module was introduced alongside the current Azure Portal and went GA in December 2015. The current Azure Portal uses the Resource Manager model and the classic Azure Portal was turned off in January 2018. The Resource Manager model eases the deployment of complex setups by using templates to deploy, update and manage resources within a resource group as a single operation.

Az offers shorter commands, improved stability, and cross-platform support. Az also has feature parity with AzureRM, giving you an easy migration path. Az is a new module, so the version has been reset to 1.0.0

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
### Sign in with Azure PowerShell
```
Connect-AzAccount
```
### Get subscriptions that the current account can access
```
Get-AzSubscription
```
### Show currently selected Azure subscription
```
Get-AzContext
```
### Change subscription context
```
Set-AzContext -SubscriptionName "Company Subscription"
```
### List all resources in a subscription
```
Get-AzResource
```
### Create a Resource Group
```
New-AzResourceGroup -Name MyResourceGroup -Location uksouth
```


