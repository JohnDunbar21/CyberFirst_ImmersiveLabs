# Digital Forensics Tools

## Quick Summary
Like with every job, knowing how to use your tools and where to find them can benefit the quality and speed of your work.

### Forensics tools
Have you ever tried to fix something but didn’t have the right tools? You've probably heard the famous saying: “A man is only as good as his tools.” This is just as true for digital forensics. A forensic tool is a software application that helps you identify, extract, and analyze digital evidence. 

Let's explore the most commonly used tools and their applications. Every tool or collection of tools covered in this lab is either free to use or open source.

### Imaging
When collecting evidence, you often start by imaging the hard drive. This involves creating an exact bit-by-bit copy of the hard drive, including all user and system files. The most commonly used imaging tool is **Forensics Toolkit (FTK) Imager** by AccessData. Another well-known tool is **EnCase Forensic Imager**. 

Please note that while FTK Imager and EnCase Forensic Imager are both free to use, there are other components in the FTK and EnCase software suite that require a license.

Another popular tool is the Linux command-line **dd**, used to create backups of entire hard disks or just specific partitions. It can also create raw images of a hard drive which makes it a good tool for digital forensics.  

### Disk analysis
Once you've acquired a copy of the hard drive, you need to analyze the data. Disk analysis tools allow you to read, analyze, and recover data such as files, web artifacts (such as browsing history, bookmarks, and cookies), emails, metadata, and more. 

**The Sleuth Kit (TSK)** and **Autopsy** are both popular options for analyzing and investigating data. TSK is a command-line tool that allows you to analyze disk images. Autopsy is a GUI for TSK tools that's easier to use, but just as powerful. These tools make it easier to find notable items, tag them for reference, leave comments as to why they're essential, and generate reports based on them.

If you want to take a deep dive into the data files, there are various tools to support you. **Bulk Extractor** is a speedy tool, which, like others, can extract traditional disk data such as emails and URLs. The tool also provides unique features such as wordlists of all “words” extracted from the disk, which can be useful for password cracking. Find out more about Bulk Extractor by visiting its GitHub page.

You can take file analysis a step further and examine the data in hexadecimal format, using tools like **xxd** or **HxD**, which create a hex dump of a given file. This approach is used in file carving techniques to uncover the structure of file systems, which can help with data recovery.

### Memory analysis
Files and other disk data are not the only places to look for evidence. You can find many useful pieces of evidence in volatile memory, aka RAM. **Volatility** is one of the most important tools in a forensic analyst's toolset for extracting digital artifacts such as running processes and network connections. 

### Network forensics
Analyzing network traffic data is different from memory and hard drive analysis. Other specialized tools allow you to dig into the network protocols and inspect each individual packet. One of the most popular tools for doing this is **Wireshark**.

Even though it’s a less popular choice, **Zeek** is an excellent tool for network traffic analysis. It's command-line-based, so may take a little time to get used to, but the results will be worth it! 

### Collections
You don't have to create your toolbox from scratch as there are pre-made collections of tools available online. For example, the **Sans Investigative Forensics Toolkit (SIFT)** workstation comes with various tools for forensic analysis and incident response, some of which are covered above. To find out more about the SIFT workstation, visit its webpage.  

Another collection of tools that may come in handy is **Eric Zimmerman’s tools**. They're primarily used for investigating Windows-based artifacts. Find out more here.