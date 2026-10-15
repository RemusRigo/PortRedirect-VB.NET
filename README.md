# Port Redirect
Port Redirect: reads a COM (serial) port and types the data into another app



## Author

* [@remusrigo](https://github.com/RemusRigo)
* [@remusrigo](https://sourceforge.net/u/remusrigo/profile)



## Features

* Reads data from a COM port (e.g. a barcode scanner on a USB serial port)
* Types the data into another application, found by its window title
* Two port listening methods: Legacy (Win32 API) and .NET (System.IO.Ports)
* Port settings: port, baud rate, data bits, parity, stop bits, flow control
* Save and load settings to JSON file
* Log events to file, with a button to open today's log
* Tested:
  * Handheld scanner connected on USB serial port (COM)



## User's Guide

See the [User's Guide](UsersGuide.md) for downloads, installation and settings.



## Statistics

![VB.NET](https://img.shields.io/badge/Language-VB.NET-blue)
![API](https://img.shields.io/badge/API-Kernel32-lightblue)
![API](https://img.shields.io/badge/API-User32-lightblue)
![.NET10.0](https://img.shields.io/badge/Runtime-.NET%2010.0-lightblue)
![VS](https://img.shields.io/badge/IDE-Visual%20Studio-purple)
![JSON](https://img.shields.io/badge/File-JSON-yellow)
<br>
![status](https://img.shields.io/badge/status-completed-brightgreen) 
![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/RemusRigo/PortRedirect-VB.NET/total)



## Roadmap

* 2026-06-07: Fix: some defaults
* 2026-06-07: Add: button to open current log file
* 2026-06-07: Add: .NET port listening method (using System.IO.Ports.SerialPort)
* 2026-06-06: Fix: \[.NET mode] if you scan codes while process is terminated, the codes will be read after you restart the process,
this is not good, need to clear buffer when process is terminated
* 2026-06-06: Fix: \[Win32 API mode] if you scan codes while process is terminated, the codes will be read after you restart the process,
this is not good, need to clear buffer when process is terminated
* 2026-06-04: Bug: if you scan when stopped, app will send codes when you will click the start button
* 2026-06-03: Fix: some minor programming logic
* 2026-06-03: Add: Configuration form
* 2026-06-03: Add: Send data to application (search by window title)
* 2026-06-02: Add: Title to JSON data
* 2026-06-02: Add: Implement save and load settings to JSON file
* 2026-06-01: Add: Legacy / Win32 API port listening method (using CreateFile and ReadFile)
* 2026-06-01: Project started
