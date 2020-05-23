# Powershell Auditing

![Powershell](https://ctrla1tdel.files.wordpress.com/2020/04/image-24.png)

“Windows PowerShell is a Windows command-line shell designed especially for system administrators. Windows PowerShell includes an interactive prompt and a scripting environment that can be used independently or in combination.” – Microsoft


## Attacking With Powershell
Powershell is built into Windows, so it makes the perfect tool for living off the land. 
Below are some of the more well known Powershell scripts/frameworks:

- Mimikatz (dogz, yakz, etc...): 
- PowerSploit
- Nishang
- Offensive-Powershell
- Powercat
- PSAttackBuildTool

 Mitre | Att&ck  https://attack.mitre.org/techniques/T1086/
 
 
## Enabling Auditing

By default, the auditing for Windows Powershell is poor. It will tell you when, it's ran and closed but not what. For this information, we need to enable a few settings. This can be done via group policy or by settings the registry key.  

For Group Policy, they can be found under: Administrative Templates > Windows Components > Windows PowerShell

 Module Logging (Win-Event ID 4103)  
 Script Block Logging (Win-Event ID 4104,4105,4106) (Not execution as too much noise)  
 Transcription (Default location: $Home\My Documents directory as \PowerShell_transcript.<time-stamp>.txt)
 

 
## Monitoring

Once auditing is enabled, you can start to query the logs generated. Forwarding to a SIEM makes life easier, and allows you to filter through the logs. If you run an AV with ADC capability or custom rules for applications, you should look to enable these as well. Common traits to track for process creation of Powershell: 

* (new-object net.webclient).Downloadstring *  
* (new-object net.webclient).DownloadFile *  
* -Enc * or * -encoded*  
* -w hidden * or * -windowstyle hidden *  
* -ep bypass * or * -executionpolicy bypass *  
* certutil -urlcache -split -f *  
* bitsadmin /create *  
* bitsadmin /transfer *   

More: https://securethelogs.com/2020/05/12/living-off-the-land-suspicious-system32/
 

 
## Validating

BlueChecker is a script which can help identify the level of auditing on your host.  
https://github.com/securethelogs/Bluechecker

Once you've ran the script, or run the below command, Bluechecker will query the machine and highlight any potential misses. It also checks the history to see if anything suspicious has occured. 

*powershell –nop –c “iex(New-Object Net.WebClient).DownloadString(‘https://raw.githubusercontent.com/securethelogs/Bluechecker/master/BlueChecker.ps1’)”*
 

 
## Useful References

Securethelogs: https://securethelogs.com/hacking-with-powershell-blue-team/  
Fireeye: https://www.fireeye.com/blog/threat-research/2016/02/greater_visibilityt.html   
Cheatsheet: https://static1.squarespace.com/static/552092d5e4b0661088167e5c/t/59c1814829f18782e24f1fe2/1505853768977/Windows+PowerShell+Logging+Cheat+Sheet+ver+Sept+2017+v2.1.pdf








