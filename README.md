# USB Malware Activity Monitor Using C and C++ OOP

## 1. Project Overview

The **USB Malware Activity Monitor** is a security-oriented system designed to monitor activities performed by USB devices when they are connected to a computer.

USB devices are commonly used for transferring files and data, but they can also introduce potentially malicious or suspicious files into a system. The proposed project aims to provide a monitoring mechanism that observes USB-related activities, records relevant information, and identifies predefined suspicious conditions.

The project combines **C programming** for system-level and file-related operations with **C++ Object-Oriented Programming (OOP)** for modular and structured system development.

---

## 2. Problem Statement

USB devices provide a convenient way to transfer data, but an unknown or compromised USB device may contain malicious files or perform suspicious activities.

Traditional systems may not provide a simple, project-level mechanism for monitoring USB activities and presenting relevant information to the user.

This project proposes a **USB Malware Activity Monitor** that can monitor USB-related activities, check files or predefined conditions, maintain activity logs, and provide alerts or indications when suspicious activity is detected.

---

## 3. Objectives

* Monitor activities associated with connected USB devices.
* Identify potentially suspicious USB-related activities.
* Maintain logs of relevant activities.
* Provide alerts or indications for predefined suspicious conditions.
* Apply C programming for system-level and file-handling operations.
* Apply C++ OOP concepts for modular system design.
* Develop a functional prototype for demonstration.
* Provide a foundation for future USB security enhancements.

---

## 4. Proposed System

The basic working flow of the system is:

```text
USB Device Connected
        |
        v
USB Activity Detection
        |
        v
Device / File Information
        |
        v
Activity Monitoring
        |
        v
Suspicious Activity Analysis
        |
        v
+-----------------------+
| Suspicious Condition? |
+----------+------------+
       Yes |       No
           |        |
           v        v
       Alert /     Normal
       Warning     Activity
           |
           v
      Activity Log
```

When a USB device is connected, the system monitors relevant activities and collects available information. The collected information is analyzed against predefined suspicious conditions. If suspicious activity is identified, the system can generate an appropriate alert or indication and record the event.

---

## 5. Project Phases

### Phase 1 — Introduction & Planning

This phase focuses on understanding the problem and defining the proposed solution.

Activities include:

* Problem identification
* Project objectives
* Proposed solution
* System requirements
* System architecture
* Working methodology
* Technology selection
* Expected outcomes

### Phase 2 — System Design & Prototype Development

This phase converts the proposed concept into a basic working prototype.

Activities include:

* Designing system modules
* USB activity monitoring
* Device information collection
* File/activity checking
* Suspicious activity detection logic
* Alert mechanism
* Activity logging
* C and C++ OOP implementation
* Individual module testing
* Prototype integration

### Phase 3 — Full Implementation & Execution

This phase focuses on completing and testing the entire system.

Activities include:

* Integration of all modules
* Complete system testing
* Debugging
* Testing different USB activities
* Suspicious-condition testing
* Log verification
* Performance evaluation
* Final demonstration
* Documentation
* Future enhancement planning

---

## 6. Major Modules

### 6.1 USB Device Detection

Detects when a USB device is connected to the computer and identifies available device information.

### 6.2 Device Information Module

Collects relevant information about the connected USB device, depending on the operating system and available system interfaces.

### 6.3 Activity Monitoring Module

Monitors selected activities associated with the USB device, such as file access or transfer-related events.

### 6.4 Suspicious Activity Detection

Checks monitored activities against predefined rules or conditions to identify potentially suspicious behavior.

### 6.5 Alert Module

Provides an appropriate warning or indication when a predefined suspicious condition is detected.

### 6.6 Activity Logging

Records relevant USB events and detected suspicious activities for later analysis.

### 6.7 OOP Management Module

Uses C++ classes and objects to organize the different components of the system and provide a modular structure.

---

## 7. Technology Used

The project will primarily use:

* **C Programming:** System-level operations, file handling, and core monitoring functionality.
* **C++:** Object-Oriented Programming and modular system design.
* **Data Structures:** Managing device and activity information.
* **File Handling:** Storing and retrieving activity logs.
* **Operating System Interfaces:** Accessing relevant USB/device information.
* **Command-Line Interface:** For displaying monitoring information and alerts.

The exact system APIs and libraries may depend on the operating system used for implementation.

---

## 8. System Architecture

```text
+----------------------+
|     USB Device       |
+----------+-----------+
           |
           v
+----------------------+
| USB Device Detection |
+----------+-----------+
           |
           v
+----------------------+
| Device Information   |
| Collection           |
+----------+-----------+
           |
           v
+----------------------+
| Activity Monitoring  |
+----------+-----------+
           |
           v
+----------------------+
| Suspicious Activity  |
| Analysis             |
+----------+-----------+
           |
           v
+----------------------+
| Alert / Warning      |
+----------+-----------+
           |
           v
+----------------------+
| Activity Logging     |
+----------------------+
```

---

## 9. Expected Outcome

The expected outcome is a functional prototype capable of demonstrating USB activity monitoring and basic suspicious-activity identification.

e system should demonstrate:

* Detection of a connected USB device.
* Collection of relevant device information.
* Monitoring of selected USB-related activities.
* Analysis of predefined suspicious conditions.
* Generation of an appropriate alert or warning.
* Recording of relevant activities in a log.
---

## 10. Testing

The prototype can be tested using different scenarios:

| Scenario                        | Expected Behaviour                       |
| ------------------------------- | ---------------------------------------- |
| No USB device connected         | Monitoring remains inactive/idle         |
| USB device connected            | Device detection is triggered            |
| Normal file activity            | Activity is recorded as normal           |
| Suspicious predefined condition | Warning/alert is generated               |
| Multiple USB activities         | Relevant activities are monitored/logged |
| USB device removed              | Device state is updated                  |
| Log generation                  | Relevant events are stored correctly     |

---


## 12. Advantages

* Provides additional monitoring of USB activities.
* Helps identify predefined suspicious conditions.
* Maintains activity records for analysis.
* Demonstrates practical application of C programming.
* Demonstrates C++ OOP concepts in a real-world project.
* Modular and expandable design.
* Can serve as a foundation for more advanced USB security systems.

---

## 14. Project Structure

A possible project structure is:

```text
USB-Malware-Activity-Monitor/
│
├── README.md
│
├── src/
│   ├── usb_detection/
│   ├── activity_monitor/
│   ├── suspicious_detection/
│   ├── alert/
│   └── logging/
│
├── include/
│   ├── usb_detection/
│   ├── activity_monitor/
│   ├── suspicious_detection/
│   ├── alert/
│   └── logging/
│
├── data/
│   └── logs/
│
├── tests/
│
├── docs/
│   ├── architecture/
│   └── project_report/
│
└── main.cpp
```

---

## 15. Role of C and C++ OOP

### C Programming

C can be used for:

* Low-level system operations.
* File handling.
* Memory management.
* Basic device/activity processing.
* Core monitoring functions.

### C++ OOP

C++ can be used for:

* Creating classes and objects.
* Encapsulating system modules.
* Organizing monitoring components.
* Managing communication between modules.
* Making the system easier to maintain and extend.

Example conceptual classes could include:

```text
USBDevice
     |
ActivityMonitor
     |
SuspiciousDetector
     |
AlertManager
     |
ActivityLogger
```

---

## 16. Conclusion

The **USB Malware Activity Monitor** proposes a practical approach to monitoring USB-related activities and identifying predefined suspicious conditions. By combining **C programming for system-level and file-related operations** with **C++ OOP for modular system design**, the project demonstrates how programming concepts can be applied to a real-world cybersecurity problem.

The project will progress from **problem identification and system planning in Phase 1**, to **prototype development in Phase 2**, and finally to **complete implementation, testing, and demonstration in Phase 3**.

The system can serve as a foundation for future development involving advanced malware detection, file analysis, machine learning, threat intelligence, and real-time security monitoring.
