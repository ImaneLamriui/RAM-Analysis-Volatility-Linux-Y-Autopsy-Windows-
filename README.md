#### challenge statement https://ctf.unizar.es/agujas_pajares/home
#### More challenges: https://ctf.unizar.es/
__Used Tools:__

<a href="https://github.com/keydet89/RegRipper3.0">RegRipper</a>

We need to  need to upload or provide the hive file as input for analysis use RegRipper to analyze it and generate a report file containing the extracted information:

###### Hive files extracted from a live system or a forensic image wiches will be analyzed by RegRipper to extract information about system configuration, user activity, installed software, and more.

###### Report file is the output generated by running RegRipper on a hive file.

<p align="center">
<img src="regripper.png" width="350">

<a href="https://www.autopsy.com/download/">autopsy</a>

keywords in __Autopsy__ refer to specific strings or patterns that are used to identify relevant information within the Windows Registry. These keywords are typically used in the context of plugins, which are small scripts or routines designed to extract specific types of information from Registry hive files.

Each plugin is designed to target specific types of information within the Registry, and keywords are used to help identify relevant data for extraction and analysis.

<p align="center">
  
<img src="KeyWords-types.png" width="350">

Keyword lists in __Autopsy__ are curated collections of terms or patterns that plugins use to identify relevant information within Windows Registry hive files.

They play a crucial role in guiding plugins to identify and extract relevant information from Windows Registry hive files, offering both predefined options and customization capabilities to suit the needs of forensic analysis tasks.

<p align="center">
<img src="keywordLists.png" width="350">
  
<img src="html.png" width="350">

In __Autopsy__, UTC settings pertain to the configuration parameters stored in the Windows Registry that govern the system's handling of Coordinated Universal Time (UTC). These settings encompass various aspects related to time management on the system, including time zone information, time synchronization mechanisms, and adjustments for daylight saving time.

<p align="center">
  
<img src="timeConfig-UTC.png" width="350">
  
<p align="center">
  
__More Tools:__

<p align="center">Click here👇

<a href="https://github.com/volatilityfoundation/volatility3"><p align="center"><img src="volatility_banner.png" width="350"></a><br>

###### How-to-use-volatility?
<p align="center">Click here👇

<a href="https://www.varonis.com/blog/how-to-use-volatility"><p align="center"><img src="Volatility-Icon-3.png" width="200" height="200"></a>

__Disk images💽__, also known as __"raw images"__ are exact copies of the entire contents of a hard disk, including the operating system files, installed programs, and user data. __For example, the file "WIN-LQS146OE2S1-20201027-142607.raw"__ appears to be a disk image or snapshot of a Windows operating system taken on a specific date: October 27, 2020, at 14:26:07. The file naming convention suggests that it was generated automatically and may contain relevant information about the operating system, configuration, files, and data stored on the disk at the time of capture.

###### When running the command __imageinfo__:

__python2 vol.py -f /home/kali/Downloads/06-export/WIN-LQS146OE2S1-20201027-142607.raw__  __imageinfo__

###### It suggests the following profiles:

Suggested Profile(s): __Win7SP1x64, Win7SP0x64, Win2008R2SP0x64, Win2008R2SP1x64_24000, Win2008R2SP1x64_23418, Win2008R2SP1x64, Win7SP1x64_24000, Win7SP1x64_23418
This output indicates that the system image may correspond to one of the suggested profiles listed, including Win7SP1x64, Win7SP0x64, Win2008R2SP0x64, Win2008R2SP1x64_24000, Win2008R2SP1x64_23418, Win2008R2SP1x64, Win7SP1x64_24000, or Win7SP1x64_23418.__ These profiles represent different versions and service pack levels of Windows operating systems and architectures.

And then we use: __--profile=__ comand and we select for example __Win7SP1x64__ profile  as the operating system from which we extracted its image. 

###### We can scan the networks that were connected using the previous command to detect anomalies:

__python2 vol.py -f /home/kali/Downloads/06-export/WIN-LQS146OE2S1-20201027-142607.raw  --profile=Win7SP1x64 netscan | tee netscan__

<p align="center">
  
<img src="scan-image.png" width="350">

__More Tools:__

<a href="https://app.any.run/submissions/">any.run App</a> uses its own virtualization infrastructure to execute and analyze malware samples securely and comprehensively. The platform employs its own set of servers and specialized software to create isolated virtual environments where malware samples can be executed and monitored without compromising the security of users' systems. These virtual environments are designed to emulate operating systems and provide a controlled environment.

<a href="https://www.joesandbox.com/">Joe Sandbox</a> runs on its own cloud infrastructure, using its own servers and systems to perform malware analyses in a virtualized manner. Users don't need to install anything on their own devices; they simply access the platform through a web browser and upload the files they want to analyze. Joe Sandbox's infrastructure takes care of executing these files securely in isolated virtual environments to prevent any potential harm to the user's system.

<a href="https://www.abuseipdb.com/">AbuseIPdb</a> is an advanced malware analysis.

<a href="https://gchq.github.io/CyberChef/">CyberChef</a>is an indispensable tool, streamlining data manipulation and analysis tasks, and serving as an invaluable asset for professionals navigating diverse datasets and formats.


