# NotSwiftOnSecurity
Modified version of SwiftOnSecurity, in order to enable in-depth collection to aide deliberate hunting and incident response.
## Install
sysmon.exe -accepteula -i sysmonconfig-export-modified.xml
## Configure Splunk Universal Forwarder
Add the following to C:\Program Files\SplunkUniversalForwarder\etc\apps\SplunkUniversalForwarder\local\inputs.conf
```
[WinEventLog://Microsoft-Windows-Sysmon/Operational]
checkpointInterval = 5
current_only = 0
disabled = 0
start_from = oldest
```
