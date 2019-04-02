# SimpliVity-POSH-module
SimpliVity POSH modules rendition for my automation works

This POSH module consists of two files:
  1. Simplivity.psd1 - Contains the manifest and customization of the SimpliVity.psm1
  2. Simplivity.psm1 - Contains the scripts for the SimpliVity module

Currently there is no installation scripts for this module. Please follow the recommendation of POSH module installation as described in https://docs.microsoft.com/en-us/powershell/developer/module/installing-a-powershell-module.
The recommended location is determined by the path specified in the $Env:PSModulePath Microsoft Windows environment variable.

There are 3 ways to authenticate using this POSH module
  1. -OVCusername [SimpliVity Administrator Username] -OVCpassword [SimpliVity Administrator Password]
  2. -OVCcredential [PSCredential object] such as: https://blogs.technet.microsoft.com/gary/2009/07/23/creating-a-ps-credential-from-a-clear-text-password-in-powershell/
  3. Without (1) and (2) which then triggers the Get-Credential menu as described in: https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/get-credential?view=powershell-6.

This POSH module has been signed with the embedded certificates. User can load this module and experiment by importing it directly in the folder where the modules are located. Please use the right execution-policy as govern by your IT dept.

      PS C:\Users\Ron.Dharma> cd C:\shares\scripts\Modules

      PS C:\shares\scripts\Modules> dir


          Directory: C:\shares\scripts\Modules


      Mode                LastWriteTime         Length Name                                                                                                                                                       
      ----                -------------         ------ ----                                                                                                                                                       
      d-----        1/23/2019   9:04 PM                .vscode                                                                                                                                                    
      -a----        10/3/2016   9:32 PM           2504 InstallModule.ps1                                                                                                                                          
      -a----         4/5/2017   4:36 PM           5334 Simplivity.psd1                                                                                                                                            
      -a----         4/2/2019  12:09 AM          43195 Simplivity.psm1                                                                                                                                            



      PS C:\shares\scripts\Modules> import-module .\simplivity.psm1
      PS C:
