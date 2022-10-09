# Digital Forensics Processes and Techniques

## Quick Summary
When practicing digital forensics, investigators use many techniques. Government bodies such as the National Institute of Standards and Technology (NIST) create standards that can guide these techniques to ensure best practices are followed.

### Forensics process
Following a structured process or framework when practicing digital forensics is essential, as it can keep your investigation moving in the right direction. Investigation frameworks are often based on industry standards and best practices. Different process models have been created by various organizations and researchers, although they all follow a similar logic. 

In this lab, we'll look at the most recent review of digital forensics methods from the **National Institute of Standards and Technology (NIST)**, which features an up-to-date process that has been peer-reviewed by experienced industry researchers. 

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/dr_0snxVxjXCaQfbN5TpF7XAxdULLngS8nSlME6k8f0.png">

The process starts with collecting evidence to support an event, such as a suspected crime or civil lawsuit, which requires investigation. Collection typically involves electronic devices such as computers, mobile phones, and other copies of data from various sources. After acquiring the data, you must protect it from modification and ensure its integrity, as this will provide a reliable source for the analysis stage of the process.

When interpreting the collected evidence, you often need to recover any lost data. Once available, you'll then need to identify, extract, and analyze the data using specialized tools. Finally, you must write a report of your findings and submit it to the appropriate authorities or staff members. 

Legally, you're not required to follow a specific forensics process, but having a process to comply with best practices helps you handle evidence responsibly and ensure its integrity.

### Forensic analysis techniques
Now that we’ve covered the process, let’s have a look at some of the practical techniques a forensic analyst can use to search through the data.

#### File analysis
Sometimes attackers tamper with evidence by deleting files to cover their tracks; they may also do this to harm individuals or companies. Files can be deleted by accident too. In any of these cases, files can be recovered by forensics practitioners. 

When you empty your files from the recycle bin, you're simply allowing other files to overwrite the space where they used to reside. Until that place is fully overwritten, files are never truly deleted from a hard drive. You can identify and reconstruct files based on the file format through a technique known as file carving. Using this method requires knowledge of file systems and involves tracking the beginning of a file (file header) all the way until the end (file footer). 

Another technique is called string searching, where you can look for a specific combination of characters (or string) in the evidence. You can practice string searching using any forensics tool that helps you interpret data. Look for network credentials, usernames, and hidden data that are not easily identifiable when you open a file. 

#### Log analysis
When you’re investigating an incident, system logs are a great place to start as they can be used to create a timeline of events. There are different places to look for generated logs, depending on the operating system and application. 

In Windows systems, Event Logs are files stored locally, revealing useful information about the system, applications, and security. Each event log is marked with an Event ID that indicates the event type. For example, Event ID 4624 indicates a computer was successfully logged into. In Linux systems, the place to look is in the `/var/log` directory, where you can find things like authentication logs, system boot logs, logging records, and more. Investigators will look at event codes and timestamps to build a picture of user and system activity.  

#### Memory analysis
Not all evidence is stored on a hard drive or in the form of files. Using memory analysis techniques, investigators can analyze volatile data by collecting a memory dump. A memory dump reveals running processes, kernel memory and objects, network connections, and other diagnostics data. Criminals can hide files and malware in places where you wouldn't think to look, but they still need to run in memory when activated. Process creation data, services that are running on unexpected ports, and unrecognized inbound and outbound connections are all common things to investigate. 

#### Network traffic analysis
If a record of network activity (or packet capture) is available as part of the evidence, you can analyze network communications and filter for specific network protocols and IP addresses of interest. Packet captures can reveal a lot of information about the data transmitted between local and remote devices. To analyze network packets, you must be familiar with their structure. That includes packet headers where you can find the network protocol, the sender and receiver IP addresses, the packet number, and more. Deep packet inspection (DPI) is a technique that involves searching beyond headers into the actual data (or payload) that the packet contains. 

Generally, investigators do a lot of digging around. Sometimes it's not entirely clear where to start or what direction you should take. Instead, investigations are often on a case-to-case basis, where you must apply your own judgment on how to progress through the analysis stage.