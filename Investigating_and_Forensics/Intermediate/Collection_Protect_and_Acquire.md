# Collection: Protect and Acquire

## Quick Summary
The first step during the collection of potential evidence is to protect and acquire the data correctly. In this lab, we'll explore the tools available for protecting evidence and look at why the order of volatility is important when collecting data.

### Protecting the evidence

#### Write Blockers
After getting your hands on a hard drive or a device that will serve as evidence, it's crucial to ensure its integrity and accountability. Starting with the chain of custody, you must document how you've acquired and handled the evidence and when. You'll then need to attach the evidence to a specialist computer, where you'll examine it and make copies for later analysis.

It's vital to keep the evidence intact, which can be achieved by attaching it to a write blocker or using a forensics workstation with an in-built write blocker. Write blockers are popular in the forensic community because they allow users to view evidence while preventing accidental modification. They achieve this by permitting read-only access to the content and monitoring system or application commands sent to a device, suppressing any that would change file contents. Both software and hardware write blockers are available and perform the same task. Software write blockers are arguably more convenient as they simply have to be installed on a single device, whereas a hardware write blocker must be carried separately.

Once you've collected copies of the evidence, you should place the original evidence in an evidence bag and store it safely. Don't forget to document this action in the chain of custody as well!

Write blockers are great, but they have limitations, and in some cases, they're not feasible. For example, for live acquisition of memory, mobile devices, or any running system, it isn't possible to use write blocking technology. In this case, the evidence will be acquired using other tools that could overwrite a small portion of the memory. 

### Acquiring evidence

#### What is volatility?
The devices you use in your day-to-day life such as mobile phones, laptops, tablets, and flash drives all store data. Depending on the device it's stored on and the method in which it has been stored, data can be measured based on its volatility. The word "volatility" refers to the likelihood of rapid and unpredictable change. Based on this definition, volatility is considered to be a binary concept (volatile or non-volatile). In the context of data collection, volatility is outlined on a spectrum from most to least volatile. 

#### Order of volatility
The order of volatility is the sequence in which digital evidence in a case is collected, making it possible to order data sources from least to most volatile. Considering the order of volatility, it's important to collect the most volatile elements first. Random-access memory (RAM), for example, must be addressed early in the collection process because the actions required to capture a disk image will likely overwrite or clear the RAM. This is also true if the device needs to be shut down, which would lead to such data being lost. Less volatile data is relatively stable. This includes data stored on disk drives or other permanent storage media. The Internet Engineering Task Force (IETF) outlines the order of volatility in the following sequence:

<img src="https://il-labforge-assets.origin.immersivelabs.team/uploads/GOXwMRBmpa142-S40_ASsMHEmpNAyfEzDPzxN7Fjad0.png">

#### Registers and cache
The contents stored within a CPU cache/register usually consist of fast storage, and the data within constantly changes. This makes them extremely volatile; you should aim to collect them first.

#### The routing table, ARP cache, process table, kernel statistics, memory
This refers to the contents of networking devices (routing tables), running memory processes, memory, and other fast-changing data which is also lost on shutdown.

#### Temporary file systems 
These are created while a file is being created or modified to temporarily hold the current state of a file. Sometimes your browser saves temporary files while browsing, so when you visit a page again, it can load faster. Despite their name, temporary file systems are not as volatile, and they can stay in your system for a while.

#### Disk
Hard disks are considered a lower priority as the information in them stays the same even if a computer is turned off.

#### Remote logging and monitoring data relevant to the system in question
This type of data is stored on remote systems, and while the data itself is volatile, it's not as relevant as the disk or other local parts of the device in question.

#### Physical Configuration, network topology, and archival media
The physical configuration of the devices in question could provide some more clarity to an investigation, but this isn't considered a priority in terms of collection. Archives are also a low priority as they're typically stored in a safe place and aren't likely to be easily lost.