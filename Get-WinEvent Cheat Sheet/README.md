

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
