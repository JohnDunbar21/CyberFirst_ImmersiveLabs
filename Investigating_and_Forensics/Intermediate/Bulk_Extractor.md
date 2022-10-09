# Bulk Extractor

## Quick Summary
Bulk Extractor is a forensics tool used to scan a disk image or directory for information. It can be used to extract a wide range of data, such as credit card details, password lists and IP addresses. This lab introduces the Bulk Extractor Command Line Interface (CLI) and explains how it can be used to acquire information.

Bulk Extractor works by splitting up a target image (or directory) into pages which can be analysed in parallel. This avoids parsing the entire file system, which requires significant amounts of memory, particularly when dealing with a large disk image.

Thanks to the way it automatically detects and decompresses certain files, Bulk Extractor is capable of analysing data which may be overlooked by other forensic tools. In some instances, it is also possible to recover information from deleted files.

The locations of the target file and output directory are required to run Bulk Extractor. The program will then create the output directory and populate it with a range of text files. These text files include details of the information found and how many times each one occurred (histograms).

An example of a basic command is shown below.

Syntax: `bulk_extractor image.iso -o /output/directory`

By default, Bulk Extractor searches for a wide range of information, including EXIF, JSON and GPS data. Disabling a scan requires the **-x** option, followed by the type of data you wish to ignore. Alternatively, the **-E** option enables users to disable all scanners, except for the one named by the user in the command line.

As well as finding information such as email addresses and credit card numbers, Bulk Extractor can build wordlists based on the names of files and folders identified during a scan. This is particularly useful, as many people use passwords which contain a word or phrase familiar to them. For example, a favoured holiday destination could be identified by analysing a user’s pictures.

Although this lab focuses on the command line interface, Bulk Extractor offers a graphical user interface (GUI) called **BEViewer**, which offers users the same features as the command line but displayed in an alternative format.

In this lab, you will need to analyse a disk image using Bulk Extractor. Once you have done this, analyse the output to answer the following questions.