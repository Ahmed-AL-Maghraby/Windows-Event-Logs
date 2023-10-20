

## Get all logs from a computer

```ps1
PS C:\Users\devil> Get-WinEvent -ListLog *

LogMode   MaximumSizeInBytes RecordCount LogName
-------   ------------------ ----------- -------
Circular            15728640          85 Windows PowerShell
Circular             1052672           0 Visual Studio
Circular            20971520        2536 System
Circular            20971520       27410 Security
Circular             1052672           0 OAlerts
Circular            20971520           0 Key Management Service
Circular             1052672           0 Internet Explorer
Circular            20971520           0 HardwareEvents
Circular            20971520        3522 Application

```


## Get event log providers and log names

```ps1
PS C:\Users\devil> Get-WinEvent -ListProvider *

Name     : VSTO 4.0
LogLinks : {Application}
Opcodes  : {}
Tasks    : {}

Name     : Microsoft-PerfTrack-MSHTML
LogLinks : {Microsoft-PerfTrack-MSHTML/Diagnostic}
Opcodes  : {win:Start, win:Stop}
Tasks    : {Navigation, Scroll, Redirect, XSSFilter-RuleCheck...}

```


## Log filtering

```ps1
PS C:\Users\devil> Get-WinEvent -LogName Application | Where-Object { $_.ProviderName -Match 'WLMS' }

   ProviderName: WLMS

TimeCreated                     Id LevelDisplayName Message
-----------                     -- ---------------- -------
6/21/2023 2:18:27 AM          100 Information
6/18/2023 3:18:57 PM          100 Information
6/15/2023 4:30:2 AM          100 Information
6/15/2023 4:18:34 AM          100 Information
```
OR we can use ``FilterHashtable`` command

```ps1
Get-WinEvent -FilterHashtable @{
  LogName='Application' 
  ProviderName='WLMS' 
}
```



## Command

```ps1
Get-WinEvent -FilterHashtable @{LogName='Microsoft-Windows-PowerShell/Operational'; ID=4104} | Select-Object -Property Message | Select-String -Pattern 'SecureString'
```



















































