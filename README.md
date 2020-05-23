# Project-Wolfhound
![Logo](https://ctrla1tdel.files.wordpress.com/2020/04/cropped-bigbanner-3.png)

Project Wolfhound aims to document simple techniques and processes that can be followed to find threats within your environment. 
The project is not limited to just identifying threats that are already inside of the network, but also enabling the environment to be able to shine a light on them. 

Often, we focus a lot of time and money in fancy tools that can help prevent future attacks, but what about if they are already inside? 
Attackers can come straight through the front door, and you could be none the wiser. 

Most of the time, we focus on the fails, but attackers hide in the successes. A security system with AV, IPS and HIPs is not going to flag if an attacker logs into an external portal using valid credentials (Stolen) and gains access to a system. 

This is why it’s important to run through these exercises, and constantly review how affective your security really is. Most controls can prevent Mimikatz, but what about if those domain admin credentials are in an Excel spreadsheet your IT thought was hidden. 

## Discovery
This section we will work on enabling auditing and help identify what is already out there. 

### [Auditing Powershell](Discovery/Powershell_Audit.md)
### [Email Enumeration](Discovery/Email_Enumeration.md)
