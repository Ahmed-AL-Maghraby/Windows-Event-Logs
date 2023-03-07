# Windows Event Logs ID and Analysis
in grograss

+ path <br>
``C:\Windows\System32\winevt\Logs``
+ accessing these event logs
  - Event Viewer ( GUI )
  - Wevtutil.exe ( command-line )
  - Get-WinEvent ( PowerShell )

## Elements of Windows Event Logs


| Element | Description |
| ------------- | ------------- |
| System Logs |  - Records events associated with the Operating System segments <br> - They may include information about hardware changes, device drivers, system changes, and other activities related to the device |
| Security Logs | - Records events connected to logon and logoff activities on a device <br> - The system's audit policy specifies the events <br> - The logs are an excellent source for analysts to investigate attempted or successful unauthorized activity |
| Application Logs | - Records events related to applications installed on a system <br> - The main pieces of information include application errors, events, and warnings |
| Directory Service Events | Active Directory changes and activities are recorded in these logs, mainly on domain controllers |
| File Replication Service Events | Records events associated with Windows Servers during the sharing of Group Policies and logon scripts to domain controllers, from where they may be accessed by the users through the client servers |
| DNS Event Logs | DNS servers use these logs to record domain events and to map out |
| Custom Logs | - Events are logged by applications that require custom data storage <br> - This allows applications to control the log size or attach other parameters, such as ACLs, for security purposes |
