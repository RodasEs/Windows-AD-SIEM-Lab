This folder will be responsible in holding all Sysmon logging

Sysmon or *Windows* systems monitoring application works to provide detailed visibility into what is happening on endpoints or the individual computers, basically logging critical security events. This helps SOC analysts identify and articulate threats like malicious programs that may be running, attackers establishing persistence mechanisms, or computer systems communicating with external command servers. Importantly speaking as well, Sysmon allows for a configurable application via XML to help reduce false positives or in other words system noise, so that SOC analysts can work to focus on what really matters.
What Sysmon is capable of articulating through every event log is the following:

Process Activity:

Event ID 1: Process creation - logs whenever a program starts running on the computer, which helps detect malware execution
Event ID 5: Process terminated- Logs when a program stops running, which is useful for tracking how long suspicious processes ran
Event ID 10: ProcessAccess (process accessing another process)- Logs when one program tries to access or manipulate another program's memory which is common malware behavior
 

Network Activity:

Event ID 3: Network connection- helps spot data theft or communication with hacker servers (C2 traffic)
Event ID 22: DNSEvent (DNS query)- Logs whenever a program looks up a website address which helps detect connections to malicious domains
File Activity:

Event ID 11: FileCreate (file created or overwritten)- Helps catch ransomeware or malware dropping payloads
Event ID 23: FileDelete (file deleted, archived)- Useful for recovering evidence that attackers tried to destroy
Event ID 26: FileDeleteDetected (file deletion logged)- Lighter-weight tracking of what's being removed
Registry Activity:

Event ID 12: RegistryEvent (registry object added or deleted)- Logs changes to Windows registry entries - helps detect malware setting up persistence to survive reboots
Event ID 13: RegistryEvent (registry value set)- Logs when registry settings are modified - catches attackers changing system configurations
Event ID 14: RegistryEvent (registry object renamed)-Logs when registry entries are renamed - helps track suspicious configuration changes
Driver/Image Activity:

Event ID 6: Driver loaded- Logs when system drivers are loaded - helps detect rootkits or malicious drivers with deep system access
Event ID 7: Image loaded (DLL/driver loaded by process)- Logs when programs load libraries (DLLs) - helps catch malware injecting malicious code into legitimate programs.
