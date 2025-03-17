# MSI2EXE-Crowdstrike
Covert .exe to .msi

# Building the installer
* Install WiX Toolset's necessary dependencies
  * Go to Control Panel -> Programs -> Turn Windows features on or off -> .NET Framework 3.5
* Install [WiX Toolset](https://wixtoolset.org/releases/) - this was tested on V3.14.1
* Download your CrowdStrike installer (`FalconSensor_Windows.exe`), save it in the same directory as this git
repository
* Build the MSI
```shell
PS C:\Users\bvarela\CrowdStrikeInstaller> & 'C:\Program Files (x86)\WiX Toolset v3.14\bin\candle.exe' .\CrowdStrikeInstaller.wxs
Windows Installer XML Toolset Compiler version 3.14.1.8722
Copyright (c) .NET Foundation and contributors. All rights reserved.

CrowdStrikeInstaller.wxs
PS C:\Users\bvarela\CrowdStrikeInstaller> & 'C:\Program Files (x86)\WiX Toolset v3.14\bin\light.exe' .\CrowdStrikeInstaller.wixobj
Windows Installer XML Toolset Linker version 3.14.1.8722
Copyright (c) .NET Foundation and contributors. All rights reserved.
```
The `CrowdStrikeInstaller.msi` is ready!
