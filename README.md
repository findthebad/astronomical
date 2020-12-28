# Find the Bad: Astronomical
This lab contains malicious activity for you to identity that was captured in log files. It should only require the installation of Docker and Docker Compose. 

## Disclaimer
This lab is based on real data containing actual malicious indicators. If you attempt to do things such as find and run files, or visit network entities that occur in these logs, you do so at your own risk.

## Setup
1) Download and install [Docker](https://www.docker.com/get-started).
2) Download and install [Docker Compose](https://docs.docker.com/compose/install/) (On Windows Docker Compose should be bundled with the Docker installer, so this step shouldn't be required).
3) Download or clone this repository.
4) Open up a command prompt, make your way to this repository folder on your local machine and run `docker-compose up`.
5) When `docker-compose up` is finished bringing the containers up, open a browser and navigate to `http://localhost:5601` to access the Kibana instance.

## The Lab
This lab is built around using Kibana for identifying and investigating signs of a compromise. The `VT Hunting` Dashboard should provide you the information you need to get started.  It is considered intermediate, and so some assumptions are made about Kibana familiarity.  If you're looking for something more introductory, try these [labs instead](https://findthebad.com/tags/introductory/).

### Questions
1) What domain and image combination in the `VT Malicious Domains` stands out?
2) What other DNS look ups occured throughout the process tree for the image identified in question one?
3) Can you identify any URLs that the malware requested?
4) What persistence method does the malware appear to use?
5) What process appears to have caused this activity and when was it run, by what user, on what computer?

### Bonus question
6) What malware does this appear to be?

### Useful Links
- [Sysmon Events List](https://docs.microsoft.com/en-ca/sysinternals/downloads/sysmon#events)
- [Sysmon Event ID 1](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon#event-id-1-process-creation)
- [Sysmon Event ID 11](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon#event-id-11-filecreate)
- [Sysmon Event ID 22](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon#event-id-22-dnsevent-dns-query)
- [MITRE - ATT&CK - Boot or Logon Autostart Execution: Registry Run Keys / Startup Folder](https://attack.mitre.org/techniques/T1547/001/)
- [MITRE - ATT&CK - Software](https://attack.mitre.org/software/)

### Solution
Available [here](https://findthebad.com/astronomical/).