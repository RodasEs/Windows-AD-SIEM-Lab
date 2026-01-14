Detections\\README.md



This section of the repo is what allows us to write up the detection philosophy behind our methods of catching threats ( most efficiently) 



“How do I turn raw logs into alerts that are useful to humans, not noise machines?”

* First, we must produce a reasoned **hypothesis** about where we can best observe locations that may harbor helpful clues for threat activity
* We must then understand the type of **signals** that most efficiently progress us in our efforts in detecting threat signals
* Once we have figured out what we can test and what kind of signals to look out for, then we are to configure or tune our configurations to reduce "noise" alerts
* It is important to acknowledge false positives within a configured detection framework. If we hypothesize malware in PowerShell and run detections on -enc (encoded commands), should we formally acknowledge that legitimate commands using -enc could also be flagged, and ensure alerts are reviewed?
* Response (becomes a runbook reference). The decision of how to act when the said alert fires. 





###### Hypothesis → Signal → Tuning → False Positives → Response

