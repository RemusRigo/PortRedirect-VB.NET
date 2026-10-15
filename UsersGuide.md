# Port Redirect: User's Guide



## Downloads & Runtimes

Download the latest release from the [Releases page](https://github.com/RemusRigo/PortRedirect-VB.NET/releases).

|Build|Architecture|Required Runtime|
|-|-|-|
|`x64`|64-bit|none (self-contained single file)|
|`x86`|32-bit|none (self-contained single file)|

> On 64-bit Windows 10/11, use **x64**. Each build is a single `PortRedirect.exe` that already contains .NET 10,
> so there is nothing else to install.



## Install

Port Redirect is portable: there is no installer.

1. Copy `PortRedirect.exe` to a folder where you have write access, for example `D:\My Apps\PortRedirect\`.
   Port Redirect saves its settings and logs in that folder.
2. Connect your device (e.g. the barcode scanner) and note its COM port in **Device Manager → Ports (COM & LPT)**.
3. Double-click `PortRedirect.exe`.

> If Windows blocks the file ("Windows protected your PC"), right-click `PortRedirect.exe` →
> **Properties** → check **Unblock** → **OK**, then try again.



## Usage

1. Click **Settings** and set the port and the target window (see below).
2. Open the application that should receive the data, e.g. Notepad.
3. Click **Start**. The status bar shows the port and baud rate.
4. Scan / send data: Port Redirect shows it, switches to the target window and types it there.
5. Click **Stop** to close the port.

|Button|Description|
|-|-|
|**Start**|Open the COM port and start listening|
|**Stop**|Close the COM port|
|**Open log**|Open today's log file|
|**Settings**|Open the settings|

Right-click the title bar → **About...** for version information.




## Settings

|Group|Setting|Default|Description|
|-|-|-|-|
|**Method**|**Legacy** / **.Net**|Legacy|How the port is read: Win32 API, or .NET `SerialPort`. Try the other one if your device doesn't work|
|**Input**|**Port**|COM1|The COM ports found on this PC|
| |**Baud Rate**|9600|110 - 115200; must match your device|
| |**Data Bits**|8|5 - 8|
| |**Parity**|0|0 = None, 1 = Odd, 2 = Even, 3 = Mark, 4 = Space|
| |**Stop Bits**|1| |
| |**Flow Control**|None|None, RTS/CTS, XON/XOFF|
|**Target**|**Window Title**|Notepad|The title of the window that receives the data (as shown in its title bar)|

Click **✓** to save. Settings are saved in `PortRedirect.json` next to `PortRedirect.exe`.

> Most barcode scanners use 9600 baud, 8 data bits, no parity, 1 stop bit, no flow control. Check your device's manual.



## Logs

Events (port opened/closed, data sent, errors) are written to
`Logs\<year>\<month>\<day>\PortRedirect.log` next to `PortRedirect.exe`. Click **Open log** to see today's log.



## Uninstall

Delete the folder you copied `PortRedirect.exe` to (this also deletes the settings and logs).
