﻿<p align="center">
    <a href="https://www.nuget.org/packages/WinUICommunity.ShellContextMenu">
        <img alt="nuget-version" src="https://img.shields.io/nuget/v/WinUICommunity.ShellContextMenu.svg"></img>
    </a> 
    <a href="https://github.com/WinUICommunity">
        <img alt="projects" src="https://img.shields.io/badge/WinUICommunity-Projects-green"></img>
    </a> 
        <a href="https://www.nuget.org/profiles/WinUICommunity">
        <img alt="WinuiCommunity Nugets" src="https://img.shields.io/badge/WinUICommunity-Nugets-green"></img>
    </a> 
        <a href="https://www.nuget.org/packages/WinUICommunity.ShellContextMenu">
        <img alt="nuget-version" src="https://img.shields.io/nuget/v/WinUICommunity.ShellContextMenu.svg"></img>
    </a>
    <a href="https://www.nuget.org/packages/WinUICommunity.ShellContextMenu">
        <img alt="Installed" src="https://img.shields.io/nuget/dt/WinUICommunity.ShellContextMenu?color=brightgreen&label=Installs"></img>
    </a> 
    <a href="https://ghost1372.github.io/winUICommunity/">
        <img alt="Docs" src="https://img.shields.io/badge/Document-Here-critical"></img>
    </a> 
</p>

<br>
<p align="center">
	<b>🙌 Donate Bitcoin with <a href="https://link.trustwallet.com/send?coin=0&address=bc1qzs4kt4aeqym6gsde669g5rksv4swjhzjqqp23a">Trust</a>🙌</b><br>
	<b>🙌 Donate ETH with <a href="https://link.trustwallet.com/send?coin=60&address=0x40Db4476c1D498b167f76A2c7ED9D45b65eb5d0C">Trust</a>🙌</b><br><br>
	<b>🙌 Bitcoin: bc1qzs4kt4aeqym6gsde669g5rksv4swjhzjqqp23a<br></b>
	<b>🙌 ETH: 0x40Db4476c1D498b167f76A2c7ED9D45b65eb5d0C</b>
</p>
<br>

# ShellContextMenu
add a new ContextMenu for Windows 11/10.

> **_NOTE:_** ShellContextMenu is based on `WindowsAppSDK` version `1.2.221209.1` stable and `Microsoft.Windows.SDK.BuildTools` version `10.0.22621.755`

```
Install-Package WinUICommunity.ShellContextMenu
```

After installing, add the following codes to `Package.appxmanifest`

```xml
<Extensions>
    <desktop4:Extension Category="windows.fileExplorerContextMenus">
        <desktop4:FileExplorerContextMenus>
            <desktop5:ItemType Type="Directory"  >
                <desktop5:Verb Id="CustomMenu" Clsid="46F650E5-9959-48D6-AC13-A9637C5B3787" />
            </desktop5:ItemType>
            <desktop5:ItemType Type="*"  >
                <desktop5:Verb Id="CustomMenu" Clsid="46F650E5-9959-48D6-AC13-A9637C5B3787" />
            </desktop5:ItemType>
            <desktop5:ItemType Type="Directory\Background">
                <desktop5:Verb Id="CustomMenu" Clsid="46F650E5-9959-48D6-AC13-A9637C5B3787" />
            </desktop5:ItemType>
        </desktop4:FileExplorerContextMenus>
    </desktop4:Extension>
    <com:Extension Category="windows.comServer">
        <com:ComServer>
            <com:SurrogateServer  DisplayName="Custome Context Menu">
                <com:Class Id="46F650E5-9959-48D6-AC13-A9637C5B3787" Path="ContextMenuCustomHost.dll" ThreadingModel="STA"/>
            </com:SurrogateServer>
        </com:ComServer>
    </com:Extension>
    <uap3:Extension Category="windows.appExecutionAlias">
        <uap3:AppExecutionAlias>
            <desktop:ExecutionAlias Alias="App5.exe"/>
        </uap3:AppExecutionAlias>
    </uap3:Extension>
</Extensions>
```

`change App5.exe to your project name.`

read the docs to see how to use it

## Documentation

See Here for Online [Documentation](https://ghost1372.github.io/winUICommunity/)
