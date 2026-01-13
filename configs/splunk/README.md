This folder, located within our config folder, is for how Splunk ingests, labels, and interprets logs.

Splunk works as the aggregator of the collected, centralized, and analyzed logs from multiple sources if has been configured to pull from, which include Sysmon ( a Windows-based system monitoring application that generates security specific logs within Event Viewer), firewalls and servers. Splunk serves at the SIEM (Security Information and Event Management) platform.

The way I’ve learned to understand how this application works in conjunction with Sysmon is through an analogy is: Sysmon and the other serving data sources are like the different areas within our brain that are responsible for holding specific types od infromation. Zooming out and taking a collective approach, the brain as a whole (Splunk) works to capture all the information, sychronize that data, interpret that data, placing it under an aggregated and automated process that puts it all together into actionable intelligence that we can then use for informed decision making. 

Purpose for configs/splunk/inputs.conf:
  *the Splunk input file articulates what kind of logs to we need to collect and where do they land?

Purpose for configs/splunk/props.conf
  *the props.conf tells Splunk how it should interpret the incoming logs
    *Sourcetype = the log's format/type, like a category tag like WinEventLog:Security → Windows Security event       log OR apache:access → Apache web server access logs
    *Parsing behavior = Splunk’s rules for turning raw text into usable events + fields.
      When Splunk recieves a log, it must then conduct time extraction, which is the timestamp under what             timezone. It will also need to figure out where does one event start and end which is event breaking.
      It must also figure out which parts should become fields, which is field extraction. 

      Why it matters
      If parsing is wrong, you get problems like:
      *events merged together (looks like one giant log line)
      *wrong timestamps (alerts appear at the wrong time)
      *missing fields (you can’t pivot by user/process/IP)
