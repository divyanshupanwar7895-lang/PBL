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
Classes and objects, constructors and destructors
Encapsulation (private data, getters and setters)
Inheritance and polymorphism (base Detector class with derived detectors, virtual functions)
Abstraction (abstract classes, interfaces)
File handling (fstream) for logs and rule files
Exception handling, the STL, and operator overloading (optional)

Example class design: USBDevice, FileEvent, Detector (base) → AutorunDetector, ExtensionDetector, MassCopyDetector, plus Logger, AlertManager, and Monitor.

DSA topics and where they fit
Hash map / set: whitelist of trusted device IDs, blacklist of known-bad file hashes or names (fast lookup)
Queue: processing incoming file and device events in order
Priority queue / heap: alerts ranked by severity
Linked list or vector: activity log
Stack: recent activity history
BST: suspicious filename and extension patterns
String matching: scanning for malicious signatures or keywords
Sorting and searching: ordering logs and finding events by time or device
Sliding window: detecting abnormal bursts of activity (e.g. 500 files touched in 10 seconds)
USB Malware Activity Monitor: Overview
Platform to code on
Language and compiler: C++ (C++17) with g++ (MinGW on Windows).
Editor: VS Code, Code::Blocks, or Visual Studio.
Operating system:
Windows is the most common choice, since most USB malware targets it. You'd use the Win32 API (GetDriveType, FindFirstFile, ReadDirectoryChangesW).
Linux works too, using libudev and /sys for device events.
Beginner tip: start with a console-based version that reads simulated USB events from a text file or menu. Add real device detection later. The OOP and DSA logic stays the same either way.
C++ OOP topics
Classes and objects, constructors and destructors
Encapsulation (private data, getters and setters)
Inheritance and polymorphism (base Detector class with derived detectors, virtual functions)
Abstraction (abstract classes, interfaces)
File handling (fstream) for logs and rule files
Exception handling, the STL, and operator overloading (optional)

Example class design: USBDevice, FileEvent, Detector (base) → AutorunDetector, ExtensionDetector, MassCopyDetector, plus Logger, AlertManager, and Monitor.

DSA topics and where they fit
Hash map / set: whitelist of trusted device IDs, blacklist of known-bad file hashes or names (fast lookup)
Queue: processing incoming file and device events in order
Priority queue / heap: alerts ranked by severity
Linked list or vector: activity log
Stack: recent activity history
Trie or BST: suspicious filename and extension patterns
String matching (KMP, Rabin-Karp): scanning for malicious signatures or keywords
Sorting and searching: ordering logs and finding events by time or device
Sliding window: detecting abnormal bursts of activity (e.g. 500 files touched in 10 seconds)
