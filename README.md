# Windows Event Logs ID and Analysis
in grograss

+ path <br>
``C:\Windows\System32\winevt\Logs``
+ accessing these event logs
  - Event Viewer ( GUI )
  - Wevtutil.exe ( command-line )
  - Get-WinEvent ( PowerShell )
<br> <br> 
## Elements of Windows Event Logs
<br>

| Element | Description |
| ------------- | ------------- |
| System Logs |  - Records events associated with the Operating System segments <br> - They may include information about hardware changes, device drivers, system changes, and other activities related to the device |
| Security Logs | - Records events connected to logon and logoff activities on a device <br> - The system's audit policy specifies the events <br> - The logs are an excellent source for analysts to investigate attempted or successful unauthorized activity |
| Application Logs | - Records events related to applications installed on a system <br> - The main pieces of information include application errors, events, and warnings |
| Directory Service Events | Active Directory changes and activities are recorded in these logs, mainly on domain controllers |
| File Replication Service Events | Records events associated with Windows Servers during the sharing of Group Policies and logon scripts to domain controllers, from where they may be accessed by the users through the client servers |
| DNS Event Logs | DNS servers use these logs to record domain events and to map out |
| Custom Logs | - Events are logged by applications that require custom data storage <br> - This allows applications to control the log size or attach other parameters, such as ACLs, for security purposes |

<br> <br> <br>
## Evnet types

<br>

| Event type | Description|
| ------------- | ------------- |
| Error | An event that indicates a significant problem such as loss of data or loss of functionality. For example, if a service fails to load during startup, an Error event is logged. |
| Warning | An event that is not necessarily significant, but may indicate a possible future problem. For example, when disk space is low, a Warning event is logged. If an application can recover from an event without loss of functionality or data, it can generally classify the event as a Warning event. |
| Information | An event that describes the successful operation of an application, driver, or service. For example, when a network driver loads successfully, it may be appropriate to log an Information event. Note that it is generally inappropriate for a desktop application to log an event each time it starts. |
| Success Audit	 | An event that records an audited security access attempt that is successful. For example, a user's successful attempt to log on to the system is logged as a Success Audit event. |
| Failure Audit	 | An event that records an audited security access attempt that fails. For example, if a user tries to access a network drive and fails, the attempt is logged as a Failure Audit event. |

<br> <br> <br>

## Event ID

+ This is a predefined numerical value that maps to a specific operation or event based on the log source. This makes Event IDs not unique







