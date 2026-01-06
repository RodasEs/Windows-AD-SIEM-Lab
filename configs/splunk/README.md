This folder, located within our config folder, is for how Splunk ingests, labels, and interprets logs.

Splunk works as the aggregator of the collected, centralized, and analyzed logs from multiple sources if has been configured to pull from, which include Sysmon ( a Windows-based system monitoring application that generates security specific logs within Event Viewer), firewalls and servers. Splunk serves at the SIEM (Security Information and Event Management) platform.



The way I have learned to understand how this application works with the conjunction of Sysmon through an analogy is: Sysmon and the other serving data sources are like the different areas within our brain that are responsible for holding specific types od data-visual memory here, auditory processing there. While zooming out and taking a collective approach, the brain (Splunk) works to capture all the information and make sense of that data, placing it under an aggregated, organized, and automated process that outs it all together into actional intelligence that we can then use.

