This project provides a Burp Suite extension for importing and passively scanning Pcap/Pcapng files with Burp. It can be used in cases 
where a HTTP client does not support proxying but it would be useful to scan, inspect or replay the HTTP traffic using Burp. 

Building from Source (optional)
-------------------------------
The Ant "dist" target will produce a consolidated jar in the dist/lib directory.

Installation
------------
* This project makes use of jNetPcap, which requires you have installed either [WinPcap](http://www.winpcap.org/) (on Windows) or [libpcap](http://www.tcpdump.org/) (on Linux)
* jNetPcap 1.4.r1425 includes a native binary component which must be loaded by Java. 
   For convenience you can download the correct binary for your platform from https://github.com/neonbunny/pcap-reconst/tree/master/lib 
   and place it in your java.library.path (i.e. your %PATH% on Windows) :

   |     | Windows | Linux |
   |-----|---------|-------|
   | x32 | [jnetpcap.dll](https://github.com/neonbunny/pcap-reconst/raw/master/lib/x32/jnetpcap.dll) | [libjpcap.so](https://github.com/neonbunny/pcap-reconst/raw/master/lib/x32/libjnetpcap.so) |
   | x64 | [jnetpcap.dll](https://github.com/neonbunny/pcap-reconst/raw/master/lib/x64/jnetpcap.dll) | [libjpcap.so](https://github.com/neonbunny/pcap-reconst/raw/master/lib/x64/libjnetpcap.so) |
* Use Burp's "Extender" tab to add the latest jar file from the [dist/lib](https://github.com/nccgroup/pcap-burp/tree/master/dist/lib) directory.

Usage
-----
After installation, an "Open Pcap file..." option will be added to the "right-click" 
context menu on the **Scanner Issues**, **Target Tree** and **Request/Response View** areas of Burp.