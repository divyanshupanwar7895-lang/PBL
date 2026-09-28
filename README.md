USB malware activity involves threat actors using removable media to inject malicious code, steal sensitive data, or compromise hardware firmware 
USB Malware Activity Monitor: Overview
Platform to code on
Language and compiler: C++ (C++17) with g++ (MinGW on Windows).
Editor: VS Code, Code::Blocks, or Visual Studio.
Operating system:
Windows is the most common choice, since most USB malware targets it. You'd use the Win32 API (GetDriveType, FindFirstFile, ReadDirectoryChangesW).
Linux works too, using libudev and /sys for device events.
Beginner tip: start with a console-based version that reads simulated USB events from a text file or menu. Add real device detection later. The OOP and DSA logic stays the same either way.

C++ OOP topics
1.Classes and objects, constructors and destructors
2.Encapsulation (private data, getters and setters)
3.Inheritance and polymorphism (base Detector class with derived detectors, virtual functions)
4.Abstraction (abstract classes, interfaces)
5.File handling (fstream) for logs and rule files
6.Exception handling, the STL, and operator overloading (optional)

DSA topics and where they fit
1.Hash map: whitelist of trusted device IDs, blacklist of known-bad file hashes or names (fast lookup)
2.Queue: processing incoming file and device events in order
3.Priority queue / heap: alerts ranked by severity
4.Linked list or vector: activity log
5.Stack: recent activity history
6.BST: suspicious filename and extension patterns
7.String matching: scanning for malicious signatures or keywords
8.Sorting and searching: ordering logs and finding events by time or device

Attacks it can detect
1.Autorun Files: autorun.inf files that try to launch a program when the USB is plugged in
2.Suspicious executables: .exe, .bat, .vbs, .ps1, .scr files appearing on the drive
3.Double-extension spoofing: names like invoice.pdf.exe
4.Shortcut virus: real folders hidden and replaced by .lnk shortcuts
5.Hidden or system attribute changes: files being silently hidden
6.Mass file copying: possible data theft (exfiltration)
7.Rapid file modification or renaming: ransomware-like behavior
8.Unauthorized devices: a USB whose vendor and product ID (VID/PID) isn't on the whitelist

A project like this uses rules and heuristics, so it's not a full antivirus. It will flag suspicious behavior rather than
prove something is malware.
