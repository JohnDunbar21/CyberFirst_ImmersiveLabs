# Basic Browser Forensics: Firefox

## Quick Summary
Browsers provide a treasure trove of important information for forensic investigators when conducting their investigations. They can often help investigators identify suspicious activity and pinpoint the origins of an incident.

### Browser forensics
When undertaking a forensics investigation, browsers provide a rich source of information for investigators to discover key information on what the machine has been used for, as well as who used it. Often the source of an incident can be pinpointed in a browser, using the many artefacts stored from our search history and browsing habits.

Artefacts in this context are specific files that the browser creates which store data on browser sessions. Each browser stores its files in a unique place with unique names; however, most browsers store the same information.

Common browser forensics artefacts are as follows:

Browser history
Bookmarks
Autocomplete data
Form history
Cached files/images
Cached pages
File downloads
Searches
Cookies

### Firefox
It is important to distinguish the key differences between browsers on which you are performing forensics. One of the key difficulties is the variety of browsers that exist, and their differences in functionality and data storage.

Mozilla Firefox is another popular web browser whose artefacts can be found on systems where it is installed. The browser offers advanced security and incognito mode.

Different browsers store artefacts in different locations and work in different ways. Firefox stores most of its relevant artefacts in the following directories:

```
C:\Users\%userprofile%\AppData\Roaming\Mozilla\Firefox\Profiles\profileID.default\
C:\Users\%userprofile%\AppData\Local\Mozilla\Firefox\Profiles\profileID.default\
```

Some stored data is encrypted to avoid confidential information being easily extracted. However, there are certain tools/modules which can be used to extract plain text passwords from a browser's history. Mimikatz has released a module which does just this.

Much of this data is stored as SQLite database files, which means that using certain tools you can easily view them. There are several tools that can be used to view and analyse these files. The most basic tool built specifically to view this file type is the DB browser for SQLite. You can simply drag the file which you wish to view into the application window to view the file's contents.