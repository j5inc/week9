# Project 9 - Honeypots


### Honeypots Deployed: 

  I used the Modern Honey Network (MHN) to complete the assignment for Week 9. In total, I created five Ubuntu 14.04 honeypots. All of the honeypots, including the MHN admin web application, were hosted in the Google Cloud. 

Honeypots: 
* Ubuntu 14.04- Dionaea with HTTP: Goal is to trap malware that exploits vulnerabilties in an exposed network. Once trapped, reserach can be done to determine the functions of the malware.

* Ubuntu 14.04 - Wordpot: A WordPress honeypot designed to trap attacks that are targeting WordPress servers.

* Ubuntu 14.04 - ElasticHoney: An elasticsearch honeypot designed to catch attackers exploiting RCE vulnerabilities in elasticsearch.

* Ubuntu 14.04 - Amun: Also has a goal of capturing malware in an automated fashion.

* Ununtu 14.04 - Shockpot: Designed to find those attempting to exploit the Bash remote code vulnerability CVE-2014-6271.


### Issues Encountered

The only issue I had was the link not working to the github repo for the MHN application. This was addressed later on in class and the link was corrected. Other than that, I was able to successfully create the VMs in the Google Cloud and hook them into the Modern Honey Net web app.

### Summary of the data collected: number of attacks, number of malware samples, etc.

Dionaea had roughly 4000 attacks in about a day of uptime. These attacks were mostly port scans of popular ports such as Telnet, MySQL, and smbd. It was by far the most successful honeypot in terms of raw attacks. In terms of content, I cannot say for sure since I was not able to capture any actual malware.

The runner up with sheer number of attacks was Amun. This honepot had about 2500 attacks in a day. One of the most popular protocols logged in attacks was Microsoft-DS file sharing using SMB on port number 445. It should be clear why this type of target is sought after; file servers typically store files that contain useful information.

ElasticHoney had one attack, and shockpot and wordpot were not attacked from a real world target. ElastiicHoney was attacked on port 9200, which makes sense since this is a port used by elasticsearch. This must not be as much as a target as the other services that were emulated in other honeypots.

### Unresolved questions raised by the data collected

There were two things that really surprsied me during this exercise. The first was the speed at which the first attack came in. In less than 10 seconds after hooking Dionaea into MHN, it registered an attack.

The other thing I noticed was that certain countries are more prevalent attackers than others. China wins the prize as the most "attacky" nation state in this exercise.

