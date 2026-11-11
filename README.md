# Hi there, I'm GeorgeZeng997

**Embedded Systems & Systems Software Engineer**

Focused on hardware-software co-design—spanning MCU/ESP32 firmware, Windows kernel and hardware-level fault isolation (DRAM bit-flip forensics, ATA/ACS-3 SSD telemetry), quantitative decision engines, and developer automation workflows.

---

## Tech Stack

- **Systems & Hardware Diagnostics**: Windows Internals (`ntdll` Superfetch, BCD `{badmemory}`, Win32 `IOCTL_ATA_PASS_THROUGH`, `PAGEDU64` Minidump Forensics), ATA/ACS-3 SMART Telemetry
- **Embedded & IoT**: C / C++, ESP-IDF / PlatformIO, ESP32 / ESP32-S3, BLE GATT, OV2640 Camera Streaming, Environmental Sensors (DHT11), Android Companion Apps
- **Software & AI Automation**: Python, JavaScript / Node.js, OpenCV, YOLOv8, PyTorch / DouZero, Tkinter / PyQt5, VS Code Extension API, Model Context Protocol (MCP)

---

## Featured Open-Source Projects

### Windows System & Hardware Diagnostics

| Repository | Description | Stack |
| :--- | :--- | :--- |
| [**win-badpage-hunter**](https://github.com/GeorgeZeng997/win-badpage-hunter) | **DRAM Bit-Flip Hunter & Kernel BCD Isolator** — Parses `PAGEDU64` BSOD minidumps for single-bit register flips, hunts leaky DRAM pages in user-mode via FIFO charge-retention windows, resolves hardware PFNs via Superfetch, and surgically excises bad RAM via Windows BCD `{badmemory}` (CLI + Desktop GUI). | Python, Win32/NTAPI, Tkinter |
| [**win-ssd-lifeguard**](https://github.com/GeorgeZeng997/win-ssd-lifeguard) | **ATA/ACS-3 SSD Forensics & 7-Layer Lifespan Suite** — Queries raw `IOCTL_ATA_PASS_THROUGH` GP Log `0x04` and vendor NAND telemetry to expose spoofed "Happy Meter" SMART health, hunts background disk write culprits in real time, and deploys Dynamic RAMDisk + NTFS cache junctions + hardware Over-Provisioning. | Python, ATA/ACS-3, PowerShell, Tkinter |

### Quantitative, AI & Developer Automation

| Repository | Description | Stack |
| :--- | :--- | :--- |
| [**bilibili-bet-ai**](https://github.com/GeorgeZeng997/bilibili-bet-ai) | **Parimutuel +EV Scanner & Fractional Kelly Engine** — Quantitative market scanner for Bilibili Prediction Plaza & Esports Match Center featuring parimutuel odds-drift discounting, late-sniping window guards, Fractional Kelly sizing, and SQLite PnL settlement tracking. | Python, SQLite, Quantitative Modeling |
| [**vscode-mcp-open-docs**](https://github.com/GeorgeZeng997/vscode-mcp-open-docs) | **VS Code Open-Documents MCP Server & Stdio Bridge** — Exposes VS Code's live in-memory editor buffers (`listOpenDocuments`, `readDocument`, `searchOpenDocuments`) to MCP-compatible AI coding agents over local WebSocket and JSON-RPC stdio. | JavaScript, Node.js, VS Code API, MCP |
| [**image-clicker**](https://github.com/GeorgeZeng997/image-clicker) | **Template-Matching Screen Automation Utility** — Multi-template OpenCV screen matcher (`TM_CCOEFF_NORMED`) with interactive region capture, self-window masking, randomized jitter/delays, global hotkeys, and cursor restoration. | Python, OpenCV, MSS, Tkinter |
| [**happily-struggle-against-landlords**](https://github.com/GeorgeZeng997/happily-struggle-against-landlords) | **YOLOv8 + DouZero Card Game Assistant** — Real-time screen card detector powered by YOLOv8 (`best.pt`) paired with DouZero deep reinforcement learning agents and interactive PyQt5 region calibration. | Python, YOLOv8, PyTorch, PyQt5 |

### Embedded Firmware & IoT

| Repository | Description | Stack |
| :--- | :--- | :--- |
| [**ESP32-S3-CAM-DHT**](https://github.com/GeorgeZeng997/ESP32-S3-CAM-DHT) | **ESP32-S3 Camera & Environmental Telemetry Node** — PlatformIO firmware integrating camera capture and DHT temperature/humidity sensing with a companion Android client. | C++, PlatformIO, ESP32-S3, Android |
| [**ESP32-BLE**](https://github.com/GeorgeZeng997/ESP32-BLE) | **ESP32 BLE Sensor & Mobile Link** — Bluetooth Low Energy peripheral firmware with DHT11 sensor acquisition and Android BLE companion app. | C, PlatformIO, ESP32, BLE |
| [**ESP32-CAM**](https://github.com/GeorgeZeng997/ESP32-CAM) | **ESP32-CAM Video Streaming Firmware** — Custom partition table and PlatformIO firmware for ESP32-CAM embedded image capture and Wi-Fi streaming. | C, PlatformIO, ESP32-CAM |

---

## Engineering Principles

- **Verify at the Hardware Boundary**: Never trust surface indicators when kernel structures (`_MMPFN`), raw bus commands (`IOCTL_ATA_PASS_THROUGH`), or physical measurements tell the real story.
- **Non-Destructive & Reproducible**: Prefer surgical isolation, deterministic state machines, and zero-bloat standalone tooling.
