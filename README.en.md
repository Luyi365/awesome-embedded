# Awesome Embedded [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

<!--lint disable awesome-list-item double-link-->

> A carefully curated collection of open-source embedded code libraries, classified in detail by function and covering 💥 **most** development scenarios.
> Unlike most Awesome lists, it collects relevant repositories and records **key usage notes** for selected libraries. 📝

A good open-source project is the result of community effort. If anything below interests you, please leave a comment through [Issues](https://github.com/Luyi365/Awesome-Embedded/issues):

- Recommend a strong embedded open-source library, including code snippets;
- Write up your experience using a listed library, such as an introductory tutorial or hard-won pitfalls;
- Report documentation errors or share suggestions;

<ins>For classification details and other collections, see [✨ Additional Resources](#-additional-resources).</ins>

#### TODO

- [x] Add license information;
- [x] Review link validity
- [ ] Improve layout and formatting
- [ ] Add English documentation
- [ ] Rewrite key usage notes for selected libraries

---

## 📚 Contents

#### Single-purpose

- [Pin and Control Library](#pin-and-control-library)
- [Timer and Time Library](#timer-and-time-library)
- [Memory and File System Library](#memory-and-file-system-library)
- [Board-Level Bus Protocol Libraries](#board-level-bus-protocol-libraries)
- [Data Structure and Data Processing Libraries](#data-structure-and-data-processing-libraries)
- [Communication Protocol and Format Parsing Library](#communication-protocol-and-format-parsing-library)
- [Logging and Terminal Interaction Library](#logging-and-terminal-interaction-library)
- [Validation, Security, Boot, and Update Library](#validation-security-boot-and-update-library)
- [UI and Menu Library](#ui-and-menu-library)
- [Kernel and Foundation Framework Library](#kernel-and-foundation-framework-library)
- [Exception Snapshot and Testing Libraries](#exception-snapshot-and-testing-libraries)
- [Algorithms and AI Libraries](#algorithms-and-ai-libraries)

#### Integrated-purpose

- [System and Thread Library](#system-and-thread-library)
- [Module Collection Packages](#module-collection-packages)

#### Other

- [Chip and Toolchain Adaptation Libraries](#chip-and-toolchain-adaptation-libraries)
- [Engine (Simulation) Libraries](#engine-simulation-libraries)

---

## [Pin and Control Library](./io-control-lib/README.en.md)

### [Buttons](./io-control-lib/README.en.md#buttons)

- ~~[key_detect](./io-control-lib/README.en.md#key_detect) - Simple button-detection component that uses event registration to provide the most basic button functionality.~~ (pending release)
- [key_module](./io-control-lib/README.en.md#key_module) - Simple, easy-to-use button-detection module that uses event callbacks and provides everything but matrix-key buttons.
- [FlexibleButton](./io-control-lib/README.en.md#flexiblebutton) - Detects buttons through intermittent polling scans, scanning and processing all button states at once, and supports most individual button events; combination buttons and interrupt triggering must be added manually.
- [MultiButton](./io-control-lib/README.en.md#multibutton) - Timer-triggered scanning drives this event-driven button module, designed with an object-oriented approach so that each button object is managed by its own data structure.
- [cotKey](./io-control-lib/README.en.md#cotkey) - Listener-based button-recognition library covering single click, double click, multiple click, short press, and long press, though it handles only a single button.
- [key_board](./io-control-lib/README.en.md#key_board) - Uses button registration and heap memory by default, scanning and processing all button states at once, and includes matrix-keypad and combination-button functionality.
- [LwBTN](./io-control-lib/README.en.md#lwbtn) - Professional button-event management library with rich configuration, if somewhat hard to grasp.

### [LED](./io-control-lib/README.en.md#led)

- [cotLed](./io-control-lib/README.en.md#cotled) - Lightweight LED control module capable of driving multiple LED mode states.
- [led_module](./io-control-lib/README.en.md#led_module) - General-purpose LED display module built on object-oriented and simple-factory patterns.

### [PID](./io-control-lib/README.en.md#pid)

- [pid_temperature_control](./io-control-lib/README.en.md#pid_temperature_control) - PID temperature control; a solid example whose approach extends well to other domains.

### [CNC](./io-control-lib/README.en.md#cnc)

- [Grbl](./io-control-lib/README.en.md#grbl) - Industry-renowned open-source CNC codebase for laser cutters, automated handwriting machines, drilling machines, graffiti painters, and quirky plotters; a maker favorite and an industry standard.
- [µCNC](./io-control-lib/README.en.md#µcnc) - General-purpose CNC firmware for microcontrollers.

---

## [Timer and Time Library](./timer-time-lib/README.en.md)

### [Timers](./timer-time-lib/README.en.md#timers)

- [MultiTimer](./timer-time-lib/README.en.md#multitimer) - Software-simulated timer module that replaces the conventional flag-checking approach, operating almost identically to a hardware timer.
- [SmartTimer](./timer-time-lib/README.en.md#smarttimer) - Very practical timer scheduler for bare-metal systems. Besides basic polling callbacks, it can also set the number of polling iterations.
- [microseconds](./timer-time-lib/README.en.md#microseconds) - Microsecond-level timer library based on the Cortex-M SysTick, with blocking and non-blocking delays. Most vendors already provide timer functions, so this mainly targets scenarios where the chip or timer module needs to be replaced.
- [perf_counter](./timer-time-lib/README.en.md#perf_counter) - Based on the Cortex-M SysTick, it provides not only basic timer functions but also code-section cycle measurement and timing services, and supports RTOS. The code looks complex and is suited to company-level projects.

### [Watchdogs](./timer-time-lib/README.en.md#watchdogs)

- [LwWDG](./timer-time-lib/README.en.md#lwwdg) - Lightweight watchdog library aimed mainly at operating systems. It monitors multiple threads and resets the system when one fails.

### [Time-related](./timer-time-lib/README.en.md#time-related)

- [LwDTC](./timer-time-lib/README.en.md#lwdtc) - Utility library for dates, times, and cron. Because Cron supports only numbers, rather than strings, parsing is faster.

---

## [Memory and File System Library](./mem-fs-lib/README.en.md)

### [Memory Management](./mem-fs-lib/README.en.md#memory-management)

- [memory](./mem-fs-lib/README.en.md#memory) - Minimalist memory management module that only provides memory allocation and release, with no other features.
- [mem_malloc](./mem-fs-lib/README.en.md#mem_malloc) - Simple and practical memory management module that does not produce memory fragmentation.
- [tlsf](./mem-fs-lib/README.en.md#tlsf) - Heap allocator using the TLSF algorithm. It supports dynamically adding and removing memory-pool regions, has $O(1)$ allocation complexity, and does not emphasize thread safety.
- [LwMEM](./mem-fs-lib/README.en.md#lwmem) - Professional memory management library with C++-like wrapper functions. It permits fragmented memory use and emphasizes RTOS thread safety.
- [jemalloc](./mem-fs-lib/README.en.md#jemalloc) - High-performance memory allocator suitable for large-scale memory allocation and release in multithreaded environments.
- [LWMalloc](./mem-fs-lib/README.en.md#lwmalloc) - Lightweight dynamic memory allocator for Linux, designed to replace the default ptmalloc allocator with better performance and memory usage.

### [Read/Write Wrapper Layer](./mem-fs-lib/README.en.md#readwrite-wrapper-layer)

- [flashMultipleErase](./mem-fs-lib/README.en.md#flashmultipleerase) - Emulates EEPROM with FLASH and uses sequential writing to achieve more than one million storage cycles.
- [eepromfs](./mem-fs-lib/README.en.md#eepromfs) - Simple file-like data read/write library based on EEPROM. It is not a true file system, but simulates data reads and writes as files.
- [Dhara](./mem-fs-lib/README.en.md#dhara) - NAND flash translation layer (FTL) for small microcontrollers. It is mainly used to manage FLASH read, write, and erase operations. It sits between the FLASH device and the file system layer.
- [kFlashFile](./mem-fs-lib/README.en.md#kflashfile) - Lightweight file-data storage solution based on NOR Flash, primarily for projects that require data to be preserved after power loss.
- [esp_partition](./mem-fs-lib/README.en.md#esp_partition) - Partition-table library from ESP that wraps SPI Flash read/write operations and allows flash access by block.
- [NVS](./mem-fs-lib/README.en.md#nvs) - Non-volatile storage library from ESP, primarily for storing key-value data in flash. Together with other ESP tools, it supports encryption, partition-image generation, and other functions.

### [File Systems](./mem-fs-lib/README.en.md#file-systems)

- [FatFs](./mem-fs-lib/README.en.md#fatfs) - Renowned file system library that is very easy to port, supporting the exFAT file system, 64-bit LBA, and GPT. It can be configured with macros according to functionality and emphasizes thread safety.
- [JesFs](./mem-fs-lib/README.en.md#jesfs) - Lightweight serial NOR flash file system designed for resource-constrained embedded systems. It is suitable for IoT use cases such as data collection, event logging, and firmware updates.
- [RanFs](./mem-fs-lib/README.en.md#ranfs) - Lightweight file system module providing POSIX-compatible file operations and emphasizing efficiency and data reliability.
- [littlefs](./mem-fs-lib/README.en.md#littlefs) - Safe file system designed for microprocessors, with power-loss protection, wear leveling, low resource consumption, and other features.
- [SPIFFS](./mem-fs-lib/README.en.md#spiffs) - File system designed for low memory (<=128MB), using statically sized ram buffers and providing wear leveling and other functions.

---

## [Board-Level Bus Protocol Libraries](./board-bus-lib/README.en.md)

### [UART](./board-bus-lib/README.en.md#uart)

- [LwOW](./board-bus-lib/README.en.md#lwow) - A professional 1-Wire protocol library that supports communication through UART or a single GPIO and provides thread-safe APIs.
- [MUDLink](./board-bus-lib/README.en.md#mudlink) - Elevates UART serial communication to a link/transport layer, guarantees framed-packet delivery, and provides delivery assurance, flow control, and link-performance statistics.

### [CDbus](./board-bus-lib/README.en.md#cdbus)

- [CDBUS](./board-bus-lib/README.en.md#cdbus-1) - A simple, efficient fieldbus compatible with UART and RS-485 protocols and hardware. It introduces hardware packet segmentation and arbitration, allowing every node to send and receive packets freely.

### [Modbus](./board-bus-lib/README.en.md#modbus)

- [freemodbus](./board-bus-lib/README.en.md#freemodbus) - A Modbus protocol stack ported by armink, supporting both master and slave functionality.
- [nanoMODBUS](./board-bus-lib/README.en.md#nanomodbus) - A compact Modbus library that can be feature-trimmed as needed and is intended for resource-constrained environments.

### [I2C](./board-bus-lib/README.en.md#i2c)

- ~~[i2c_scanner](./board-bus-lib/README.en.md#i2c_scanner) - An I2C device-scanning library extracted from Nordic's SDK that can scan the number and addresses of onboard I2C devices.~~ (pending release)

### [SPI](./board-bus-lib/README.en.md#spi)

- [SFUD](./board-bus-lib/README.en.md#sfud) - An open-source universal serial SPI Flash driver library that supports a range of Flash chips through device tables.

### [Interboard Communication](./board-bus-lib/README.en.md#interboard-communication)

- [ESSL](./board-bus-lib/README.en.md#essl) - ESP's serial slave link component, allowing a host to communicate with slaves through bus drivers and the corresponding protocol. In essence, it is MCU-to-MCU communication with an additional layer.
- [SACP](./board-bus-lib/README.en.md#sacp) - Snapmaker's device data-communication protocol, implemented in C++ for communication among multiple devices in a complete machine.

### [USB](./board-bus-lib/README.en.md#usb)

- [TinyUSB](./board-bus-lib/README.en.md#tinyusb) - An open-source cross-platform USB host/device stack for embedded systems. It is memory-safe, uses no dynamic allocation, is thread-safe, and defers all interrupt events for handling in non-ISR task functions.
- [CherryUSB](./board-bus-lib/README.en.md#cherryusb) - A USB host/device protocol stack for embedded systems (with USB IP). It is portable across platforms and suits chips that lack a built-in USB protocol stack.

---

## [Data Structure and Data Processing Libraries](./data-struct-process-lib/README.en.md)

### [Queues](./data-struct-process-lib/README.en.md#queues)

- [CBUF](./data-struct-process-lib/README.en.md#cbuf) - An elegantly implemented macro-based ring buffer that is simple and easy to use.
- [sys/queue](./data-struct-process-lib/README.en.md#sysqueue) - Queue and linked-list header files used by Linux and FreeBSD. They are implemented entirely with macros and can link arbitrary types, such as structs.
- [byte_queue](./data-struct-process-lib/README.en.md#byte_queue) - A C-language ring queue supporting arbitrary types, wrapped with macros and simple to use.
- [queue](./data-struct-process-lib/README.en.md#queue) - A general-purpose C queue supporting arbitrary data types; simple and efficient to use.
- [Ring-Buffer](./data-struct-process-lib/README.en.md#ring-buffer) - A simple and efficient ring-buffer library that is easy to use.
- [wl_queue](./data-struct-process-lib/README.en.md#wl_queue) - A ring queue supporting arbitrary data types. It uses C overloading techniques and emphasizes coroutine safety.
- [RingBuffer](./data-struct-process-lib/README.en.md#ringbuffer) - A practical, fully featured ring-buffer library that uses heap-memory allocation.
- [queue](./data-struct-process-lib/README.en.md#queue-1) - A simple, highly extensible queue library that also supports zero-copy queue reads and writes (suitable for individual elements that use large amounts of memory, effectively reducing function execution time).
- [QueueForMcu](./data-struct-process-lib/README.en.md#queueformcu) - A queue module for non-RTOS systems that dynamically creates queue objects and buffers.
- [ConcurrentQueue](./data-struct-process-lib/README.en.md#concurrentqueue) - An industrial-grade lock-free queue based on C++; it requires no locks and places strong emphasis on thread safety.
- [LwRB](./data-struct-process-lib/README.en.md#lwrb) - A professional FIFO ring-buffer library with no dynamic memory allocation, suitable for MDA transfers and focused on thread and interrupt safety.
- [fifofast](./data-struct-process-lib/README.en.md#fifofast) - A FIFO library optimized for MCUs, intended to reduce CPU and SRAM consumption as much as possible.

### [Streams](./data-struct-process-lib/README.en.md#streams)

- ~~[uart_stream](./data-struct-process-lib/README.en.md#uart_stream) - A data-stream buffer-processing library for UART data with some general applicability.~~ (pending release)
- [xprintf](./data-struct-process-lib/README.en.md#xprintf) - Embedded string functions that substitute for conventional printf functionality and can dynamically write strings to different peripherals. Their main purpose is to interact with multiple peripherals rather than a terminal.
- [CMSIS-Stream](./data-struct-process-lib/README.en.md#cmsis-stream) - An ARM-official data-stream processing component with graphical representations, suitable for professional projects and multi-device data-stream processing.

### [Data Structure Collections](./data-struct-process-lib/README.en.md#data-structure-collections)

- [uthash](./data-struct-process-lib/README.en.md#uthash) - Provides data-structure libraries for hashes, lists, rings, and more; use them by including only the header file.

### [Databases](./data-struct-process-lib/README.en.md#databases)

- [cotParam](./data-struct-process-lib/README.en.md#cotparam) - Manages parameters in a table-driven manner, including default, minimum, and maximum values.
- [EasyFlash](./data-struct-process-lib/README.en.md#easyflash) - A simple Key-Value database that primarily provides variable KV pairing, IAP data modification (for upgrades), log storage, and other functions.
- [FlashDB](./data-struct-process-lib/README.en.md#flashdb) - Provides both KV and TS databases; compared with EasyFlash, it focuses more on the database itself and provides fewer extra features.
- [Nanopb](./data-struct-process-lib/README.en.md#nanopb) - A lightweight Protobuf implementation supporting C. Protobuf is a data format developed by Google. It can be used for data storage and communication protocols and is independent of language and platform, allowing communication between different devices.
- [ITTIA DB](./data-struct-process-lib/README.en.md#ittia-db) - A powerful real-time embedded database mainly for embedded systems and IoT devices, used for on-device monitoring, storage, and analysis of time-series data; it requires a commercial license.
- [linq4c](./data-struct-process-lib/README.en.md#linq4c) - Implements C# LINQ methods in C.
- [SQLite](./data-struct-process-lib/README.en.md#sqlite) - The most widely used industry-standard embedded database, using SQL syntax and disk files.

### [Compression Libraries](./data-struct-process-lib/README.en.md#compression-libraries)

- [lz4](./data-struct-process-lib/README.en.md#lz4) - An extremely fast lossless compression-algorithm library, suitable for data compression during communication.
- [heatshrink](./data-struct-process-lib/README.en.md#heatshrink) - An embedded decompression library with extremely low resource consumption. Related documentation is sparse.
- [TJpgDec](./data-struct-process-lib/README.en.md#tjpgdec) - A JPEG image-decompression module optimized for embedded systems.

---

## [Communication Protocol and Format Parsing Library](./protocol-format-parser-lib/README.en.md)

### [Web Server](./protocol-format-parser-lib/README.en.md#web-server)

- [LightTPD](./protocol-format-parser-lib/README.en.md#lighttpd) - A lightweight, high-performance embedded Web server.
- [Mongoose](./protocol-format-parser-lib/README.en.md#mongoose) - An event-driven C/C++ networking library with HTTP and MQTT.
- [Boa](./protocol-format-parser-lib/README.en.md#boa) - An unmaintained embedded Web server with known vulnerabilities.

### [Web Plugin](./protocol-format-parser-lib/README.en.md#web-plugin)

- [FastCGI](./protocol-format-parser-lib/README.en.md#fastcgi) - A higher-performance CGI implementation.
- [libevent](./protocol-format-parser-lib/README.en.md#libevent) - An event-driven library for network servers.
- [rtty](./protocol-format-parser-lib/README.en.md#rtty) - Web access to an embedded Linux device terminal.
- [Nanomsg](./protocol-format-parser-lib/README.en.md#nanomsg) - A socket library for scalable communication protocols.
- [url](./protocol-format-parser-lib/README.en.md#url) - A simple URL parsing module.
- [tiny-curl](./protocol-format-parser-lib/README.en.md#tiny-curl) - An embedded cURL library supporting HTTP only.

### [RPC](./protocol-format-parser-lib/README.en.md#rpc)

- [ERPC](./protocol-format-parser-lib/README.en.md#erpc) - A simple, efficient embedded remote-call framework.
- [EmbedXrpc](./protocol-format-parser-lib/README.en.md#embedxrpc) - An RPC component with code generation.
- [erpc](./protocol-format-parser-lib/README.en.md#erpc-1) - NXP's embedded Remote Procedure Call system.

### [TCP/IP](./protocol-format-parser-lib/README.en.md#tcpip)

- [lwIP](./protocol-format-parser-lib/README.en.md#lwip) - A widely used lightweight embedded TCP/IP stack.
- [CycloneTCP](./protocol-format-parser-lib/README.en.md#cyclonetcp) - An embedded dual IPv4/IPv6 stack.
- [onps](./protocol-format-parser-lib/README.en.md#onps) - A network stack for resource-constrained microcontrollers.
- [wolfIP](./protocol-format-parser-lib/README.en.md#wolfip) - A tiny TCP/IP stack without dynamic allocation.
- [dyad](./protocol-format-parser-lib/README.en.md#dyad) - A Linux asynchronous networking library for TCP.

### [SSH](./protocol-format-parser-lib/README.en.md#ssh)

- [tinyssh](./protocol-format-parser-lib/README.en.md#tinyssh) - A minimalist embedded SSHv2 server.
- [wolfSSH](./protocol-format-parser-lib/README.en.md#wolfssh) - A lightweight ANSI C SSHv2 library.

### [HTTP](./protocol-format-parser-lib/README.en.md#http)

- [libevhtp](./protocol-format-parser-lib/README.en.md#libevhtp) - A low-overhead embedded HTTP library.

### [MQTT](./protocol-format-parser-lib/README.en.md#mqtt)

- [Paho MQTT](./protocol-format-parser-lib/README.en.md#paho-mqtt) - An embedded MQTT library with packet serialization and C/C++ clients.
- [mqttclient](./protocol-format-parser-lib/README.en.md#mqttclient) - A high-performance cross-platform MQTT client.
- [Mosquitto](./protocol-format-parser-lib/README.en.md#mosquitto) - A lightweight Eclipse MQTT message broker.
- [wolfMQTT](./protocol-format-parser-lib/README.en.md#wolfmqtt) - A lightweight multi-platform MQTT client library.

### [Thread](./protocol-format-parser-lib/README.en.md#thread)

- [OpenThread](./protocol-format-parser-lib/README.en.md#openthread) - Google's open-source Thread implementation.

### [Bluetooth](./protocol-format-parser-lib/README.en.md#bluetooth)

- [bluetooth_stack](./protocol-format-parser-lib/README.en.md#bluetooth_stack) - A low-power dual-mode Bluetooth stack for learning.
- [BTstack](./protocol-format-parser-lib/README.en.md#btstack) - A lightweight embedded Bluetooth protocol stack.
- [NimBLE](./protocol-format-parser-lib/README.en.md#nimble) - Apache Mynewt's open-source Bluetooth stack.

### [GNSS](./protocol-format-parser-lib/README.en.md#gnss)

- [LwGPS](./protocol-format-parser-lib/README.en.md#lwgps) - A simple NMEA message parser.
- [RTKLIB](./protocol-format-parser-lib/README.en.md#rtklib) - A benchmark RTK library and reference manual.
- [Ntrip](./protocol-format-parser-lib/README.en.md#ntrip) - A C++ Ntrip library with client, caster, and CORS support.

### [AT](./protocol-format-parser-lib/README.en.md#at)

- [AT Command](./protocol-format-parser-lib/README.en.md#at-command) - An AT command communication parser for Modem, WiFi, and Bluetooth.
- [Xradio_atcmd](./protocol-format-parser-lib/README.en.md#xradio_atcmd) - An AT command parser extracted from the Xradio SDK.

### [Base64](./protocol-format-parser-lib/README.en.md#base64)

- [base64](./protocol-format-parser-lib/README.en.md#base64-1) - A minimal Base64 codec.
- [base64](./protocol-format-parser-lib/README.en.md#base64-2) - A SIMD- and OpenMP-accelerated Base64 codec.

### [CSV](./protocol-format-parser-lib/README.en.md#csv)

- [MiniCSV](./protocol-format-parser-lib/README.en.md#minicsv) - A minimal CSV parser for complex rows.
- [CRStrLib](./protocol-format-parser-lib/README.en.md#crstrlib) - CSV and other string parsing with frame validation.
- [fast-cpp-csv-parser](./protocol-format-parser-lib/README.en.md#fast-cpp-csv-parser) - A small, fast, header-only C++ CSV parser.

### [INI](./protocol-format-parser-lib/README.en.md#ini)

- [libinimini](./protocol-format-parser-lib/README.en.md#libinimini) - A minimal MCU INI parser.
- [inih](./protocol-format-parser-lib/README.en.md#inih) - A C INI parser for embedded systems.
- [iniparser](./protocol-format-parser-lib/README.en.md#iniparser) - A portable, thread-safe C INI parser.

### [TLV](./protocol-format-parser-lib/README.en.md#tlv)

- ~~[ITLV](./protocol-format-parser-lib/README.en.md#itlv) - An optimized minimal TLV data format with CRC validation.~~ (pending release)
- [TLV](./protocol-format-parser-lib/README.en.md#tlv-1) - A TLV format encoding implementation.

### [JSON](./protocol-format-parser-lib/README.en.md#json)

- [cJSON](./protocol-format-parser-lib/README.en.md#cjson) - An ultra-lightweight ANSI C JSON parser.
- [struct2json](./protocol-format-parser-lib/README.en.md#struct2json) - Fast C structure and JSON conversion based on cJSON.
- [cson](./protocol-format-parser-lib/README.en.md#cson) - A C json-struct model parser based on cJSON.
- [json](./protocol-format-parser-lib/README.en.md#json-1) - A simple C JSON generation and parsing library.
- [JSMN](./protocol-format-parser-lib/README.en.md#jsmn) - A compact, fast JSON parser without dynamic memory.
- [lwjson](./protocol-format-parser-lib/README.en.md#lwjson) - A general JSON parser optimized for embedded systems.
- [MojoJson](./protocol-format-parser-lib/README.en.md#mojojson) - An object-oriented general JSON parser with a C version.
- [LJSON](./protocol-format-parser-lib/README.en.md#ljson) - A feature-rich high-performance JSON parser.
- [json-parser](./protocol-format-parser-lib/README.en.md#json-parser) - A practical C JSON parsing and generation library.
- [Frozen](./protocol-format-parser-lib/README.en.md#frozen) - A scanf/printf-like JSON parser and generator.
- [sj.h](./protocol-format-parser-lib/README.en.md#sjh) - A zero-copy minimalist C JSON parser.

### [XML](./protocol-format-parser-lib/README.en.md#xml)

- [simple_xml](./protocol-format-parser-lib/README.en.md#simple_xml) - A full-featured bidirectional XML parser.
- [TinyXML-2](./protocol-format-parser-lib/README.en.md#tinyxml-2) - A C++ DOM XML parser.

### [TOML](./protocol-format-parser-lib/README.en.md#toml)

- [TOML](./protocol-format-parser-lib/README.en.md#toml-1) - A readable data markup format more extensible than INI.

### [Other Formats](./protocol-format-parser-lib/README.en.md#other-formats)

- [LwPKT](./protocol-format-parser-lib/README.en.md#lwpkt) - A general packet protocol library with variable-length data.
- [xpack](./protocol-format-parser-lib/README.en.md#xpack) - Header-only conversion between C++ structures and common formats.
- [Uart_Transfer_BIN_to_exFlash](./protocol-format-parser-lib/README.en.md#uart_transfer_bin_to_exflash) - Reliable serial transfer of data to Flash.

---

## [Logging and Terminal Interaction Library](./log-term-lib/README.en.md)

### [LOG Logging](./log-term-lib/README.en.md#log-logging)

- [dbuglib](./log-term-lib/README.en.md#dbuglib) - A compact logging library that only provides output display and can adjust log levels to filter logs at specified levels, equivalent to the printf functionality that generic SDKs include;
- [log.c](./log-term-lib/README.en.md#logc) - A minimalist logging library that only provides output display and recording. Based on the C99 standard, it is not well suited to the embedded field.
- [log](./log-term-lib/README.en.md#log) - A compact logging module whose output includes the time, log type, content, file name, line number, function name, and other information.
- [alog](./log-term-lib/README.en.md#alog) - A streamlined output logging component with color and mutex locking.
- [LwPRINTF](./log-term-lib/README.en.md#lwprintf) - A safe, concise standard-output utility library that allows multiple output streams to be redirected; all APIs are reentrant.
- [EasyLogger](./log-term-lib/README.en.md#easylogger) - A relatively comprehensive logging library supporting dynamic filtering and color selection. It emphasizes thread safety and supports asynchronous and buffered output modes.
- [zlog](./log-term-lib/README.en.md#zlog) - A pure C logging function library that is highly reliable, high-performance, thread-safe, flexible, and conceptually clear; it does not support content filtering or parsing.

### [Terminal Interaction](./log-term-lib/README.en.md#terminal-interaction)

- [cmd-parser](./log-term-lib/README.en.md#cmd-parser) - A minimalist command-parsing library that triggers functions through strings, which is a pretty interesting approach.
- [LwSHELL](./log-term-lib/README.en.md#lwshell) - A lightweight shell library that is simple and easy to use and includes command descriptions.
- [debugcmd](./log-term-lib/README.en.md#debugcmd) - A feature-complete command-line parsing library providing Tab completion, help viewing, subcommand registration, and other functions.
- [Argtable3](./log-term-lib/README.en.md#argtable3) - A standardized command-line parsing library for custom operation commands that follows the POSIX interface.
- [nr_micro_shell](./log-term-lib/README.en.md#nr_micro_shell) - A standard command-line interaction library that provides Tab command completion and command history lookup, with native support for ENV tools.
- [letter shell](./log-term-lib/README.en.md#letter-shell) - A powerful embedded command-line interaction library providing nearly all shell functions and allowing functions to be executed directly through function addresses.
- [Xradio_console](./log-term-lib/README.en.md#xradio_console) - A console library extracted from the Xradio SDK. Its commands use a hierarchical structure, making it suitable when there are many commands; it is based on RTOS.
- [easyShell](./log-term-lib/README.en.md#easyshell) - A simple and easy-to-use microcontroller shell that supports Tab completion.

---

## [Validation, Security, Boot, and Update Library](./secure-boot-update-lib/README.en.md)

### [Validation and Security](./secure-boot-update-lib/README.en.md#validation-and-security)

- [crc-lib-c](./secure-boot-update-lib/README.en.md#crc-lib-c) - A minimalist CRC library implementing 21 commonly used CRC parameter models, with no extensions.
- [tiny-AES-c](./secure-boot-update-lib/README.en.md#tiny-aes-c) - A compact, portable AES library providing ECB, CTR, and CBC encryption modes.
- ~~[key](./secure-boot-update-lib/README.en.md#key) - A minimalist encryption algorithm used with keys. It is single-purpose but practical, and suitable for network encryption and similar applications.~~ (pending release)
- [wolfCrypt](./secure-boot-update-lib/README.en.md#wolfcrypt) - A lightweight cryptographic library from wolfSSL that supports many popular algorithms and ciphers, suitable for enterprise projects.
- [wolfSSL](./secure-boot-update-lib/README.en.md#wolfssl) - A lightweight, portable SSL/TLS library powered by the wolfCrypt cryptography library, aimed at IoT, embedded, and RTOS environments.
- [Mbed TLS](./secure-boot-update-lib/README.en.md#mbed-tls) - A TrustedFirmware project and a widely used SSL/TLS library in the industry.
- [wolfHSM](./secure-boot-update-lib/README.en.md#wolfhsm) - A client-server framework for hardware cryptography, nonvolatile memory, and secure processing. Originally an HSM core for automotive applications, it now suits any trusted environment.
- [wolfTPM](./secure-boot-update-lib/README.en.md#wolftpm) - A portable TPM stack that provides wrapper interfaces to simplify key operations and supports bare metal, RTOS, Linux, Windows, and other platforms.
- [wolfSentry](./secure-boot-update-lib/README.en.md#wolfsentry) - A dynamic intrusion detection and prevention system (IDPS): an embedded-ready firewall engine centered on monitoring, logging, pattern matching, and notification.

### [Boot and Update](./secure-boot-update-lib/README.en.md#boot-and-update)

- [Tiny Bootloader](./secure-boot-update-lib/README.en.md#tiny-bootloader) - A simple bootloader for 8-bit and 32-bit microcontrollers that uses very few resources and supports multiple bus communication methods.
- [OpenBLT](./secure-boot-update-lib/README.en.md#openblt) - A well-known microcontroller bootloader library supporting 8-, 16-, and 32-bit microcontrollers.
- [wolfBoot](./secure-boot-update-lib/README.en.md#wolfboot) - A secure bootloader solution for 32-bit microcontrollers, supporting firmware authentication and firmware update mechanisms.
- [mOTA](./secure-boot-update-lib/README.en.md#mota) - An update component designed for 32-bit MCUs, transferred through the YModem-1K protocol.
- [MicorBoot](./secure-boot-update-lib/README.en.md#micorboot) - A bootloader module optimized for embedded microcontroller-device updates, providing power-failure protection, resumable transfers, and more.
- [MCUboot](./secure-boot-update-lib/README.en.md#mcuboot) - A TrustedFirmware project: a general secure bootloader for 32-bit microcontrollers that is independent of specific systems and hardware.

---

## [UI and Menu Library](./ui-menu-lib/README.en.md)

### [HMI](./ui-menu-lib/README.en.md#hmi)

- [tslib](./ui-menu-lib/README.en.md#tslib) - The most widely used resistive touchscreen calibration algorithm library in embedded systems, although it seems to be available only on Linux.
- [tslib_for_mcu](./ui-menu-lib/README.en.md#tslib_for_mcu) - A resistive touchscreen calibration library trimmed down from Linux.

### [Monochrome](./ui-menu-lib/README.en.md#monochrome)

- [ECBM_GUI](./ui-menu-lib/README.en.md#ecbm_gui) - A very basic monochrome GUI library that implements GUI functionality solely by storing screen content in an internal buffer. It suits small hobby projects.
- [SimpleGUI](./ui-menu-lib/README.en.md#simplegui) - A GUI library designed for monochrome displays that provides simple drawing capabilities. It suits low-pixel monochrome dot-matrix screens.
- [oledlib](./ui-menu-lib/README.en.md#oledlib) - An open-source OLED graphics library with some graphics suitable for screen savers.
- [U8g2](./ui-menu-lib/README.en.md#u8g2) - A monochrome display library that provides support for various controllers and basic graphics drawing.
- [MonoGUI](./ui-menu-lib/README.en.md#monogui) - A specialized GUI system for small electronic devices with monochrome screens, offering comprehensive features and an input method. It suits devices such as electronic dictionaries and label printers.
- [WouoUI](./ui-menu-lib/README.en.md#wououi) - Inspired by Zhihui Jun's not-yet-open-source MonoUI, it implements a smooth UltraLink-like interface, uses an encoder as the controller, and has a particularly smooth and attractive upgraded version.
- [astra UI](./ui-menu-lib/README.en.md#astra-ui) - A C++-based multi-level OLED menu UI with smooth transition animations.
- [GLCD](./ui-menu-lib/README.en.md#glcd) - A graphical LCD library for microcontroller-based embedded systems, including hardware drivers, text, and basic graphics drawing.

### [Color](./ui-menu-lib/README.en.md#color)

- [GuiLite](./ui-menu-lib/README.en.md#guilite) - An ultra-lightweight GUI library that supports multiple platforms and third-party libraries.
- [Olive.c](./ui-menu-lib/README.en.md#olivec) - A simple 2D graphics library for C that draws only with canvas features.
- [microui](./ui-menu-lib/README.en.md#microui) - A tiny, portable UI library that uses very little memory and is suitable for any rendering system that can draw rectangles and text.
- [LingLongGUI](./ui-menu-lib/README.en.md#linglonggui) - An efficient GUI generation library with a graphical interface editor for conveniently generating code.
- [LingDongGUI](./ui-menu-lib/README.en.md#lingdonggui) - A GUI library that further encapsulates Arm-2D, aiming to improve ease of use while also supporting native APIs.
- [AAGUI](./ui-menu-lib/README.en.md#aagui) - A cross-platform, general-purpose GUI that aims to enable Android-like advanced UI development in embedded systems. It supports semi-declarative (JSON) programming and is suitable for projects similar to mobile applications.
- [GT-HMI](./ui-menu-lib/README.en.md#gt-hmi) - A UI library from Qualcomm intended for Chinese users, with multiple languages and font libraries, a simulator, and PC-side tools. It can be used with both RTOS and bare metal, making it suitable for practical product-level projects.
- [LVGL](./ui-menu-lib/README.en.md#lvgl) - A lightweight general-purpose graphics library that is open source, free, and has almost everything needed for a GUI. It suits project-level devices.
- [AWTK](./ui-menu-lib/README.en.md#awtk) - A GUI graphics library from ZLG that is open source and free.
- [TouchGFX](./ui-menu-lib/README.en.md#touchgfx) - A GUI graphics library from STM32 with powerful features and graphical editing software, generally suitable only for STM32 development.
- [GUIX](./ui-menu-lib/README.en.md#guix) - A GUI graphics library provided by Azure RTOS; it is mature, convenient to develop with, open source, and free.
- [emWin](./ui-menu-lib/README.en.md#emwin) - Also known as uCGUI, it is a GUI graphics library from Segger that can be licensed for use with chips from many well-known manufacturers.
- [Embedded Wizard GUI](./ui-menu-lib/README.en.md#embedded-wizard-gui) - A very powerful GUI graphics library, but it is paid. It comes with a graphical editor.
- [Qt for MCU](./ui-menu-lib/README.en.md#qt-for-mcu) - A GUI graphics library from QT, suitable for developers with QT experience, and requires payment.
- [μGFX](./ui-menu-lib/README.en.md#μgfx) - A lightweight UI library for touchscreens that focuses on performance and is free for non-commercial use.
- [MiniGUI](./ui-menu-lib/README.en.md#minigui) - A multi-platform, highly customizable UI library that can be used with chips of different performance levels; it is suitable for mobile devices and industrial fields, and is free for non-commercial use.
- [μGUI](./ui-menu-lib/README.en.md#μgui) - An open-source minimalist graphics library that is platform-independent and consists of only one source file.
- [Aeropoint GUI](./ui-menu-lib/README.en.md#aeropoint-gui) - Creates GUIs using a PPT-based approach, requires payment, and has no trial version.
- [Clay](./ui-menu-lib/README.en.md#clay) - A high-performance 2D UI layout library that provides responsive layout capabilities and is suitable for embedded Web development.
- [Nuklear](./ui-menu-lib/README.en.md#nuklear) - A dependency-free graphical user interface toolkit that builds graphics through input states and drawing commands, suitable for responsive applications.
- [LinaVG](./ui-menu-lib/README.en.md#linavg) - A rendering library for 2D vector graphics.
- [BlurHash](./ui-menu-lib/README.en.md#blurhash) - An open-source image placeholder algorithm and implementation that can display a wireframe and thumbnail before images are loaded; it may be useful in embedded applications.
- [OpenGL](./ui-menu-lib/README.en.md#opengl) - A cross-language, cross-platform 2D/3D rendering library primarily developed in C, which also supports development in C++, Python, Java, and other languages. Its capabilities are extremely powerful and suitable for game development, scientific visualization, virtual reality, and other fields.
- [Rawdraw](./ui-menu-lib/README.en.md#rawdraw) - A cross-platform, dependency-free UI drawing system that provides a good interface abstraction for OpenGL.
- [TinyGL](./ui-menu-lib/README.en.md#tinygl) - A small implementation of OpenGL for embedded systems. It simplifies complex interfaces into forms that are easier to understand and use.
- [foolrenderer](./ui-menu-lib/README.en.md#foolrenderer) - A software renderer implemented in C that does not depend on graphics libraries. In only a few thousand lines of code, it implements OpenGL-like basic graphics features and real-time rendering techniques for game development, such as shadows, tangent-space normal mapping, and physically based material systems.
- [EmberGL](./ui-menu-lib/README.en.md#embergl) - An OpenGL-like real-time 2D / 3D raster rendering library for MCU.
- [Cairo](./ui-menu-lib/README.en.md#cairo) - A 2D graphics library that supports multiple outputs and provides PostScript- and PDF-like drawing methods. It is primarily intended for PCs but can also be ported to embedded chips.

### [Acceleration](./ui-menu-lib/README.en.md#acceleration)

- [Arm-2D](./ui-menu-lib/README.en.md#arm-2d) - A 2D graphics acceleration library optimized for Cortex-M processors, positioned between GUI libraries and the driver layer.
- [GUIslice](./ui-menu-lib/README.en.md#guislice) - A simple, easy-to-use open-source GUI framework with a hacker style, no dynamic memory allocation, and a layout PC-side tool.

### [Graphics](./ui-menu-lib/README.en.md#graphics)

- [qrencode](./ui-menu-lib/README.en.md#qrencode) - A QR code generation library suitable for microcontrollers.
- [QR Code generator library](./ui-menu-lib/README.en.md#qr-code-generator-library) - A general-purpose QR code generation library containing versions for multiple languages, intended to achieve better performance with less code.
- [QRCode](./ui-menu-lib/README.en.md#qrcode) - A QR code generation library based on QR Code generator library, optimized for systems with constrained processors and memory, and supporting all specifications from Version 1 through Version 40.

### [Glyphs](./ui-menu-lib/README.en.md#glyphs)

- [MCUFont](./ui-menu-lib/README.en.md#mcufont) - A library dedicated to fonts, implementing font compression, decompression, and text rendering (adjustment).
- [Unicorn](./ui-menu-lib/README.en.md#unicorn) - A C99-based Unicode encoding and decoding library that provides basic algorithms and functionality for this encoding.

### [Menu Frameworks](./ui-menu-lib/README.en.md#menu-frameworks)

- [zBitsView](./ui-menu-lib/README.en.md#zbitsview) - A virtual multi-level menu that exists only in the logic layer and is unrelated to whether a screen is present.
- [emenu](./ui-menu-lib/README.en.md#emenu) - An unusual menu framework whose menu structure is reflected directly in the code.
- ~~[Menu](./ui-menu-lib/README.en.md#menu) - A simple and practical menu framework, suitable for small company projects.~~ (pending release)
- [cotMenu](./ui-menu-lib/README.en.md#cotmenu) - Implements multi-level deep menus with linked lists, equivalent to the display logic layer and completely decoupled from keys and displays.
- [MiaoUI](./ui-menu-lib/README.en.md#miaoui) - An OLED menu UI framework based on U8g2, supporting list and icon menus, nonlinear animations, task pop-ups, and other features.
- [MultMenu](./ui-menu-lib/README.en.md#multmenu) - A combination of multi-level menus and a monochrome OLED nonlinear animation library; it is simple and convenient to port and suitable for maker projects with similar requirements.
- [SMF](./ui-menu-lib/README.en.md#smf) - A C++-based menu framework providing multi-level menus and menu objects, suitable for product-level projects.
- [PageManager](./ui-menu-lib/README.en.md#pagemanager) - A C++-based page lifecycle management library providing complete page scheduling capabilities, suitable for product-level projects.

---

## [Kernel and Foundation Framework Library](./kernel-framework-lib/README.en.md)

### [Events](./kernel-framework-lib/README.en.md#events)

- [cpost](./kernel-framework-lib/README.en.md#cpost) - An ultra-lightweight context-switching and task-decoupling library that uses event dispatching and is suitable for bare-metal systems.
- [LwEVT](./kernel-framework-lib/README.en.md#lwevt) - A professional event-module library with optional custom data types and attached specified functions; it can be understood as a combination of events and messages, handling event dispatching and callbacks.

### [Messages](./kernel-framework-lib/README.en.md#messages)

- [YAMI4](./kernel-framework-lib/README.en.md#yami4) - A messaging library designed for distributed systems, with particular attention to control and monitoring systems.
- [ZeroMQ](./kernel-framework-lib/README.en.md#zeromq) - A high-performance asynchronous messaging library intended for distributed or concurrent applications.
- [CDIPC](./kernel-framework-lib/README.en.md#cdipc) - An inter-process communication (IPC) mechanism and library suitable for coordinating perception, control drivers, and algorithms in real-time systems.

### [Pipes](./kernel-framework-lib/README.en.md#pipes)

- [readerwriterqueue](./kernel-framework-lib/README.en.md#readerwriterqueue) - A C++ single-producer, single-consumer lock-free queue. It serves the same purpose as a pipe framework, is fast and easy to use, and emphasizes thread safety without locks.

### [Mailboxes](./kernel-framework-lib/README.en.md#mailboxes)

- [DataCenter](./kernel-framework-lib/README.en.md#datacenter) - A C++ message publish-subscribe framework that provides complete mailbox services and is suitable for project-level engineering.

### [Thread Management](./kernel-framework-lib/README.en.md#thread-management)

- [C Thread Pool](./kernel-framework-lib/README.en.md#c-thread-pool) - A lightweight embedded thread-pool library for managing thread creation and lifecycles, solving the overhead caused by frequent thread creation and destruction.

### [Driver Frameworks](./kernel-framework-lib/README.en.md#driver-frameworks)

- ~~[initcall](./kernel-framework-lib/README.en.md#initcall) - Extracts the RT-Thread initialization framework so initialization is completed in the kernel.~~ (pending release)
- ~~[platform_dev](./kernel-framework-lib/README.en.md#platform_dev) - A simplified driver framework modeled on Linux. Its design does not use dynamic memory allocation, making it suitable for chips with limited resources.~~ (pending release)
- [c-periphery](./kernel-framework-lib/README.en.md#c-periphery) - A Linux-based hardware peripheral abstraction-layer template.

### [Sensor Frameworks](./kernel-framework-lib/README.en.md#sensor-frameworks)

- ~~[senser_algorithm](./kernel-framework-lib/README.en.md#senser_algorithm) - A sensor-data processing framework for RTOS.~~ (pending release)

### [Module Frameworks](./kernel-framework-lib/README.en.md#module-frameworks)

- [RIL](./kernel-framework-lib/README.en.md#ril) - Wireless communication module (GSM/GPRS/CatM1/NB-Iot) management software developed specifically for embedded platforms.

### [State Machines](./kernel-framework-lib/README.en.md#state-machines)

- [EFSMC](./kernel-framework-lib/README.en.md#efsmc) - An event-driven finite state machine that avoids naming conflicts through careful design. It is simple, convenient, and standardized to use.
- [signals_slots](./kernel-framework-lib/README.en.md#signals_slots) - A lightweight signal-and-slot framework that simplifies event-driven programming.
- [UML State Machine in C](./kernel-framework-lib/README.en.md#uml-state-machine-in-c) - A multi-platform, lightweight state-machine framework supporting finite state machines and hierarchical state machines, with logging functionality.

### [Dynamic Loading](./kernel-framework-lib/README.en.md#dynamic-loading)

- [dynamic_loader](./kernel-framework-lib/README.en.md#dynamic_loader) - A dynamic-loading function library trimmed from the libdl source code of RT-Thread. It is not coupled to the original OS and can be used on bare metal.

---

## [Exception Snapshot and Testing Libraries](./exception-test-lib/README.en.md)

### [Coredump](./exception-test-lib/README.en.md#coredump)

- [CmBacktrace](./exception-test-lib/README.en.md#cmbacktrace) - Renowned error-tracing library for ARM Cortex-M series MCUs; for any project that's even a little complex, just drop it in and you're done.

### [Exception Handling](./exception-test-lib/README.en.md#exception-handling)

- ~~[try](./exception-test-lib/README.en.md#try) - try-catch exception handling implemented in C.~~ (pending release)
- [CException](./exception-test-lib/README.en.md#cexception) - Simple exception handling for C, faster than the standard library and portable to any platform supporting setjmp/longjmp.
- [MLA](./exception-test-lib/README.en.md#mla) - A small, easy-to-use memory leak analysis library that records allocation counts.

### [Testing](./exception-test-lib/README.en.md#testing)

- ~~[MTTEST](./exception-test-lib/README.en.md#mttest) - A simple RTOS-based testing framework using a registration mechanism.~~ (pending release)
- [MinUnit](./exception-test-lib/README.en.md#minunit) - A minimal unit testing framework for C without memory allocation.
- [CuTest](./exception-test-lib/README.en.md#cutest) - A minimalist C unit testing framework using dynamic memory allocation.
- [cmockery](./exception-test-lib/README.en.md#cmockery) - A lightweight C unit testing framework based on the standard C library.
- [EEMBC](./exception-test-lib/README.en.md#eembc) - Provides many testing libraries for the embedded field, mainly for chip performance testing; an industry standard suitable for enterprise-level project deployment.
- [Unity](./exception-test-lib/README.en.md#unity) - A unit testing framework written in C and focused on embedded toolchains.
- [greatest](./exception-test-lib/README.en.md#greatest) - A compact C testing system that uses instrumentation/coverage testing and can run with other programs.
- [Catch2](./exception-test-lib/README.en.md#catch2) - A popular C++ unit testing framework with only one header file, designed to be lightweight, easy to use, and dependency-free.

---

## [Algorithms and AI Libraries](./algo-ai-lib/README.en.md)

### [Arithmetic](./algo-ai-lib/README.en.md#arithmetic)

- ~~[float_converter](./algo-ai-lib/README.en.md#float_converter) - A library for rounding and integer conversion of floating-point data.~~ (pending release)
- [LibBF](./algo-ai-lib/README.en.md#libbf) - A high-precision floating-point arithmetic library that provides values with greater precision than standard floating-point types such as *float* and *double*, with flexible control over precision and rounding modes.

### [Fundamental Algorithms](./algo-ai-lib/README.en.md#fundamental-algorithms)

- [FXT](./algo-ai-lib/README.en.md#fxt) - A collection of C algorithms focused on bit manipulation, combinatorics, fast transforms, and more.
- [xxHash](./algo-ai-lib/README.en.md#xxhash) - An extremely fast non-cryptographic hash algorithm that works under RAM and speed constraints and suits more demanding use cases.
- [Terathon Math Library](./algo-ai-lib/README.en.md#terathon-math-library) - A C++ mathematics library containing classes for vectors, matrices, quaternions, and projective geometric algebra elements. It can be used in graphics, AI, games, and related fields.

### [AI Frameworks](./algo-ai-lib/README.en.md#ai-frameworks)

- [TinyMaix](./algo-ai-lib/README.en.md#tinymaix) - An AI neural-network inference framework designed for resource-constrained microcontrollers.
- [miniMNIST-c](./algo-ai-lib/README.en.md#minimnist-c) - A two-layer miniature neural network implemented in C, suitable for learning and basic embedded applications.
- [Genann](./algo-ai-lib/README.en.md#genann) - A minimal, thoroughly tested neural-network library for training and using feedforward artificial neural networks (ANNs) in C.
- [uTensor](./algo-ai-lib/README.en.md#utensor) - An extremely lightweight machine-learning inference framework built on TensorFlow that imports trained models as C++ files.
- [NNoM](./algo-ai-lib/README.en.md#nnom) - A framework for running neural networks on MCUs. It is similar to TinyMaix but offers more features.
- [Paddle Lite](./algo-ai-lib/README.en.md#paddle-lite) - A high-performance, lightweight, flexible, and extensible deep-learning inference framework targeting mobile, embedded, edge, and other hardware platforms.
- [TVM](./algo-ai-lib/README.en.md#tvm) - An end-to-end deep-learning compiler framework for CPU, GPU, ARM, and other hardware architectures.
- [tflite-micro](./algo-ai-lib/README.en.md#tflite-micro) - TensorFlow Lite for microcontrollers, enabling deployment of machine-learning frameworks on MCUs.
- [ncnn](./algo-ai-lib/README.en.md#ncnn) - A high-performance neural-network forward-computation framework highly optimized for mobile platforms. It supports most common CNN networks and can be deployed on some embedded chips.
- [MNN](./algo-ai-lib/README.en.md#mnn) - A lightweight deep neural-network engine that supports deep-learning inference and training on embedded devices with POSIX interfaces.
- [TensorFlow Lite](./algo-ai-lib/README.en.md#tensorflow-lite) - A well-known machine-learning library for deploying models to mobile devices, microcontrollers, and other edge devices for on-device machine learning.
- [Mediapipe](./algo-ai-lib/README.en.md#mediapipe) - Google's open-source cross-platform machine-learning framework. It provides tools that can be deployed to mobile, web, PC, and IoT devices, including models for object detection, image classification, face recognition, gesture recognition, text classification, language detection, and audio classification.
- [Edge Impulse](./algo-ai-lib/README.en.md#edge-impulse) - A popular embedded machine-learning development platform for data processing and analysis, model training, and model deployment.
- [YMCV](./algo-ai-lib/README.en.md#ymcv) - A miniature computer-vision library written purely in C, with no dependencies, cross-platform support, and easy feature trimming.
- [NeuralNetwork](./algo-ai-lib/README.en.md#neuralnetwork) - A neural-network library for MCUs that runs RNN, GRU, and LSTM architectures with very few resources and supports bare metal and some operating systems.

### [AI Models and Algorithms](./algo-ai-lib/README.en.md#ai-models-and-algorithms)

- ~~[Knn](./algo-ai-lib/README.en.md#knn) - A very basic KNN algorithm written in C with no particular optimizations; it is not recommended.~~ (pending release)
- [NanoDet-Plus](./algo-ai-lib/README.en.md#nanodet-plus) - A super-fast, high-precision, lightweight anchor-free object-detection model implemented on a mobile AI framework.
- [pico](./algo-ai-lib/README.en.md#pico) - A lightweight face-recognition algorithm based on pixel-intensity comparisons for object detection, suitable for single-purpose, low-traffic scenarios.

---

## [System and Thread Library](./sys-thread-lib/README.en.md)

### [Time-Slice Scheduling Systems](./sys-thread-lib/README.en.md#time-slice-scheduling-systems)

- [ztask](./sys-thread-lib/README.en.md#ztask) - An extremely simple time-slice scheduler with only five APIs; the kind of framework you could write on the fly.
- [ETP](./sys-thread-lib/README.en.md#etp) - A time-slice polling framework intended to decouple tasks with different time slices in the main polling loop; it is the most basic polling framework.
- [cotTask](./sys-thread-lib/README.en.md#cottask) - A time-slice polling framework for initialization, startup, and task-scheduling management, with the ability to set task priorities.
- [CodeBrick](./sys-thread-lib/README.en.md#codebrick) - A time-slice polling framework that includes many practical modules, has no driver layer, and is simple and easy to use. It fits modern project development philosophy and is a bare-metal framework I really like; you could call it a top choice for ordinary projects.
- [vkern](./sys-thread-lib/README.en.md#vkern) - A task scheduling kernel written by imitating the RTOS architecture; its principle is still to use timers to create a foreground-background system.
- [cola_os](./sys-thread-lib/README.en.md#cola_os) - A foreground-background system suitable for bare metal that has power-consumption requirements, limited CPU performance, and somewhat complex functionality.
- [JxOS](./sys-thread-lib/README.en.md#jxos) - A foreground-background system with no complex registration or function-pointer structures, providing system kernel functions: tasks, events, messages, bulletin boards, mailboxes, pipes, registration, memory allocation...
- [EventOS](./sys-thread-lib/README.en.md#eventos) - An event-driven embedded system that provides kernel functions and more.
- [BabyOS](./sys-thread-lib/README.en.md#babyos) - A registration-service framework for bare-metal MCU projects. It manages functional modules and peripheral drivers, has very clear code layering and standards, RTT-like "MenuConfig" terminal configuration, and PC simulation.

### [Quasi-Real-Time Systems](./sys-thread-lib/README.en.md#quasi-real-time-systems)

- [cotOs](./sys-thread-lib/README.en.md#cotos) - A simple query-based cooperative multitasking system that does not require timers for task switching; it creates tasks just like an RTOS does, but provides no other functions. I really like it, and it feels absolutely cool.
- [BasicOS](./sys-thread-lib/README.en.md#basicos) - An extremely simple cooperative system in which all tasks share one task stack, including simple kernel functional components and more.
- [TaskScheduler](./sys-thread-lib/README.en.md#taskscheduler) - A cooperative multitasking framework with preemptive programming, but without concerns about concurrent-processing safety. It supports various configurations of task execution parameters.
- [QuarkTS](./sys-thread-lib/README.en.md#quarkts) - An event-driven multitasking scheduling system that avoids concurrency pitfalls (resource sharing, race conditions, deadlocks, and so on) and provides complete kernel functions, complies with multiple industry standards, and is suitable for basic enterprise projects.
- [VSF](./sys-thread-lib/README.en.md#vsf) - An event-driven preemptive multitasking framework that includes a kernel and commonly used components, suitable for enterprise-level projects.

### [RTOS](./sys-thread-lib/README.en.md#rtos)

- [KLite](./sys-thread-lib/README.en.md#klite) - A very concise and easy-to-use RTOS with the most basic practical kernel functions. It is suitable for simple RTOS projects that need rapid deployment.
- [FreeRTOS](./sys-thread-lib/README.en.md#freertos) - An OS used by many small vendors, with abundant online materials. It is fairly conventional and suitable for a basic project preparing to adopt an RTOS.
- [uC/OS](./sys-thread-lib/README.en.md#ucos) - An OS that was relatively popular early on. Its features are similar to FreeRTOS, but it has somewhat stronger functionality.
- [RT-Thread](./sys-thread-lib/README.en.md#rt-thread) - A shining star among domestic products, an excellent and practical RTOS with multiple components and extra functions. Its detailed documentation makes it very suitable for an OS project starting from scratch.
- [RTX](./sys-thread-lib/README.en.md#rtx) - ARM's RTOS, with strong compatibility with Keil.
- [NuttX](./sys-thread-lib/README.en.md#nuttx) - An operating system emphasizing standard compatibility and compact packaging that follows the POSIX standard and ANSI standards.
- [embOS](./sys-thread-lib/README.en.md#embos) - SEGGER's RTOS, free for non-commercial use.
- [Azure RTOS](./sys-thread-lib/README.en.md#azure-rtos) - Microsoft's RTOS, with a rich set of components.
- [Zephyr](./sys-thread-lib/README.en.md#zephyr) - An RTOS maintained by Linux, well suited to learning Linux development philosophy.
- [At-RTOS](./sys-thread-lib/README.en.md#at-rtos) - A user-friendly real-time operating system for embedded controllers, providing only basic kernel functions.
- [Embox](./sys-thread-lib/README.en.md#embox) - A multitasking operating system characterized by supporting Linux open-source components without using Linux itself. This open-source system aims to make Linux software usable everywhere.
- [YiYiYa OS](./sys-thread-lib/README.en.md#yiyiya-os) - A full-featured OS with an architecture designed in layers from top to bottom. It can almost be regarded as a simplified Android system, suitable for phone-like products.
- [LK](./sys-thread-lib/README.en.md#lk) - Short for Little Kernel, a tiny embedded system whose BootLoader is particularly well known and used in native Android systems.
- [SKRTOS_sparrow](./sys-thread-lib/README.en.md#skrtos_sparrow) - An ultra-small system of only a few hundred lines that implements basic scheduling and IPC mechanisms; some call it a children's version of FreeRTOS.
- [CosyOS](./sys-thread-lib/README.en.md#cosyos) - An operating system with zero interrupt latency that can maintain real-time performance without globally disabling interrupts, including many innovative and practical kernel functions.
- [scmRTOS](./sys-thread-lib/README.en.md#scmrtos) - A lightweight RTOS written in C++, providing only the most basic kernel functions such as scheduling and messages.
- [MuditaOS](./sys-thread-lib/README.en.md#muditaos) - A mobile operating system built on FreeRTOS, optimized specifically for E-Ink displays.

### [IoT-RTOS](./sys-thread-lib/README.en.md#iot-rtos)

- [Contiki-NG](./sys-thread-lib/README.en.md#contiki-ng) - A multitasking IoT operating system maintained by the authors of uIP and LwIP. It focuses on reliable, secure low-power communication and standard Internet protocols.
- [Mbed OS](./sys-thread-lib/README.en.md#mbed-os) - An easy-to-use IoT operating system from ARM.
- [Huawei LiteOS](./sys-thread-lib/README.en.md#huawei-liteos) - A lightweight IoT operating system from Huawei for the IoT domain.
- [Xiaomi Vela](./sys-thread-lib/README.en.md#xiaomi-vela) - An IoT operating system from Xiaomi, built on the NuttX kernel at its foundation.
- [AliOS Things](./sys-thread-lib/README.en.md#alios-things) - A highly scalable IoT operating system from Alibaba for the IoT domain.
- [TencentOS Tiny](./sys-thread-lib/README.en.md#tencentos-tiny) - A real-time operating system developed by Tencent for the IoT domain.
- [OneOS](./sys-thread-lib/README.en.md#oneos) - A lightweight operating system introduced by China Mobile for the IoT domain, featuring configurability, cross-platform support, low power consumption, and high security. It supports mainstream chip architectures such as ARM Cortex-M/A, MIPS, and RISC-V; is compatible with standard interfaces such as POSIX and CMSIS; and supports JavaScript and MicroPython development.
- [LuatOS](./sys-thread-lib/README.en.md#luatos) - A Lua script runtime framework for embedded systems, with the functional scope of an operating system.
- [Lua-RTOS-ESP32](./sys-thread-lib/README.en.md#lua-rtos-esp32) - A real-time operating system supporting a Lua interpreter, providing all Lua-required resources, basic modules, and middleware, and portable to other 32-bit platforms.
- [Apache Mynewt OS](./sys-thread-lib/README.en.md#apache-mynewt-os) - An Apache OS designed for low-power wireless devices, with built-in Bluetooth and IEEE protocol stacks, ready to use out of the box.
- [Mongoose OS](./sys-thread-lib/README.en.md#mongoose-os) - An IoT firmware development framework supporting C/JavaScript development, with good support for remote management and upgrades. The open-source edition has limited functionality.
- [MicroPythonOS](./sys-thread-lib/README.en.md#micropythonos) - A lightweight, multifunctional operating system built with MicroPython, designed for microcontrollers such as ESP32 and desktop systems. It provides a modern Android-like touch interface, an app store, OTA, and more.

### [ROS](./sys-thread-lib/README.en.md#ros)

- [ROS](./sys-thread-lib/README.en.md#ros-1) - A well-known open-source robot operating system in the industry that implements a complete set of software libraries and tools.
- [AimRT](./sys-thread-lib/README.en.md#aimrt) - A runtime development framework built with Modern C++ for modern robotics. It provides comprehensive plugin development interfaces, is highly extensible, and compatible with other ROS ecosystems.

---

## [Module Collection Packages](./module-pack/README.en.md)

- [ToolKit](./module-pack/README.en.md#toolkit) - A small embedded toolkit providing a circular queue, software timer, and event set, with very clear documentation.
- [lwUTIL](./module-pack/README.en.md#lwutil) - A practical toolkit containing value operations, endian storage, bit operations, ASCII conversion, and more.
- [sc](./module-pack/README.en.md#sc) - A standalone, high-performance toolkit with a small memory footprint, mainly providing data-structure functionality.
- [cotUtils](./module-pack/README.en.md#cotutils) - A general C extension library, including multiple containers (queues, stacks, doubly-linked lists, dynamic arrays), serializable/deserializable structures, the PP library (multifunction macros), and more.
- [mr-library](./module-pack/README.en.md#mr-library) - A lightweight embedded framework providing standardized driver interfaces and simple kernel-function components; a top choice for ordinary vendor-level projects.
- [Zorb Framework](./module-pack/README.en.md#zorb-framework) - A lightweight embedded framework with basic kernel functions, all independently integrated for convenient trimming.
- [Gear-Lib](./module-pack/README.en.md#gear-lib) - A set of general C foundational libraries implemented entirely in POSIX C for cross-platform compatibility with Linux, Windows, Android, and iOS, including data structures, async operations, I/O, state machines, and dynamic loading.
- [c-algorithms](./module-pack/README.en.md#c-algorithms) - Provides a collection of common algorithms and data structures to make up for missing standard-library facilities, and compiles much smaller than the C standard library.
- [klib](./module-pack/README.en.md#klib) - An independent, lightweight C library offering a variety of foundational algorithms, data structures, parsers, and more.
- [AMetal](./module-pack/README.en.md#ametal) - A software package from ZLG that covers various types of peripherals and provides a unified abstraction-layer interface. The code is somewhat redundant, but its coverage of types is fairly comprehensive.
- [eLab](./module-pack/README.en.md#elab) - An integrated development platform containing most packages needed for embedded systems, with particular emphasis on cross-platform development and PC simulation; it is especially suited to projects with standardized development processes.
- [TheAlgorithms](./module-pack/README.en.md#thealgorithms) - The open-source organization TheAlgorithms maintains a rich collection of foundational algorithms, data structures, machine-learning libraries, and versions in popular languages.
- [simpostOS](./module-pack/README.en.md#simpostos) - A design methodology and collection of software components and services. It modularizes all functions and greatly improves reuse. Written in modern C++, it is not beginner-friendly.
- [PetiteDrv](./module-pack/README.en.md#petitedrv) - A general SDK library based on layered abstraction to decouple functions without complex code; suitable for small-company, small-project development.
- [varch](./module-pack/README.en.md#varch) - An embedded C module library with commonly used algorithms, data structures (containers), parsers, a standalone C std library, and utilities. Each library can be used independently and is simple and efficient.
- [ctool](./module-pack/README.en.md#ctool) - Common tools usually absent from ordinary libraries, including variadic arguments, dates, and memory testing.
- [Generic_MCU_Software_Infrastructure](./module-pack/README.en.md#generic_mcu_software_infrastructure) - Provides the necessary software infrastructure, services, and macros for high-level abstract concepts and paradigms.
- [appkit](./module-pack/README.en.md#appkit) - A C++ library for Linux application development, including common modules such as thread management, timers, file I/O, and serial communication.
- [GLib](./module-pack/README.en.md#glib) - The core GTK library, offering many functions including data structures, type conversion, string utilities, file operations, and main-loop abstraction.

---

## [Chip and Toolchain Adaptation Libraries](./chip-toolchain-lib/README.en.md)

### [51](./chip-toolchain-lib/README.en.md#51)

- [8051-ELL](./chip-toolchain-lib/README.en.md#8051-ell) - An ELL (efficient low-layer) library that combines the programming concepts of HAL and LL libraries, primarily targeting the STC8 series.
- [ECBM](./chip-toolchain-lib/README.en.md#ecbm) - 51-chip peripheral function library; take whichever module you need.

### [AVR](./chip-toolchain-lib/README.en.md#avr)

### [ST](./chip-toolchain-lib/README.en.md#st)

- [STM32F4 Discovery](./chip-toolchain-lib/README.en.md#stm32f4-discovery) - A collection of driver libraries for STM32F4-series microcontrollers, including implementation tutorials and examples for multiple peripherals and interfaces.

### [ESP](./chip-toolchain-lib/README.en.md#esp)

- [LwESP](./chip-toolchain-lib/README.en.md#lwesp) - Professional AT parser library intended for communicating with ESP devices from other devices through AT commands.
- [ESPUI](./chip-toolchain-lib/README.en.md#espui) - A simple web user interface library for ESP32 and ESP8266 devices. It lets users create and manage device web interfaces easily without HTML, CSS, or JavaScript frontend-development knowledge.
- [FluidNC](./chip-toolchain-lib/README.en.md#fluidnc) - A CNC firmware library optimized for ESP32 controllers.
- [Rabbit GRBL](./chip-toolchain-lib/README.en.md#rabbit-grbl) - A CNC firmware library running on ESP32 processors, highly optimized to maintain stable, jitter-free control pulses up to 120 kHz.

### [SIMCom](./chip-toolchain-lib/README.en.md#simcom)

- [LwCELL](./chip-toolchain-lib/README.en.md#lwcell) - Professional AT parser library intended for communicating with SIMCom devices from other devices through AT commands.

### [MDK](./chip-toolchain-lib/README.en.md#mdk)

- [flash_blob](./chip-toolchain-lib/README.en.md#flash_blob) - Quickly generates generic flash drivers using MDK FLM files.

### [Driver](./chip-toolchain-lib/README.en.md#driver)

- [LibDriver](./chip-toolchain-lib/README.en.md#libdriver) - An open-source driver-development organization containing driver libraries for all common peripheral modules (140+).

---

## [Engine (Simulation) Libraries](./engine-sim-lib/README.en.md)

### [SoftFP](./engine-sim-lib/README.en.md#softfp)

- [SoftFP](./engine-sim-lib/README.en.md#softfp-1) - A software floating-point implementation for systems without a hardware floating-point unit (FPU).

### [C++](./engine-sim-lib/README.en.md#c)

- [sds](./engine-sim-lib/README.en.md#sds) - A simple dynamic-string library that uses heap memory and imitates the C++ `string` type in C.
- [STR](./engine-sim-lib/README.en.md#str) - A more advanced string-processing library with string splitting, trimming, searching, and error-checking functions.
- [etl](./engine-sim-lib/README.en.md#etl) - A C++ template library for embedded systems.
- [LW_OOPC](./engine-sim-lib/README.en.md#lw_oopc) - An object-oriented programming extension for embedded systems. It has been updated and optimized across multiple versions based on the original source and is simple to use.
- [PLOOC](./engine-sim-lib/README.en.md#plooc) - Provides object-oriented programming extensions in C, including private members, inheritance, overloading, and more.
- [vlib](./engine-sim-lib/README.en.md#vlib) - A C-language template library providing functionality similar to C++ STL, including common containers and support for arbitrary data types.

### [Lua](./engine-sim-lib/README.en.md#lua)

- [MicroLua](./engine-sim-lib/README.en.md#microlua) - A LUA development package for Raspberry Pi Pico. With porting changes, it should also work on other microcontroller devices.
- [eLua](./engine-sim-lib/README.en.md#elua) - A Lua engine for embedded systems that lets Lua scripts run on embedded platforms.

### [Python](./engine-sim-lib/README.en.md#python)

- [PikaPython](./engine-sim-lib/README.en.md#pikapython) - An ultra-lightweight Python engine with zero dependencies and zero configuration that uses Python instead of C for development. It has extensive Chinese documentation and video materials.

### [Rust](./engine-sim-lib/README.en.md#rust)

- [Rust Embedded](./engine-sim-lib/README.en.md#rust-embedded) - Focuses on improving the end-to-end experience of using Rust in resource-constrained environments and on nontraditional platforms.

### [JavaScript](./engine-sim-lib/README.en.md#javascript)

- [mJS](./engine-sim-lib/README.en.md#mjs) - A JavaScript engine specifically for microcontrollers, with a small footprint (RAM: 1k, ROM: 50k) and based on the ES6 standard.

### [Arduino](./engine-sim-lib/README.en.md#arduino)

- [ArduinoCore-API](./engine-sim-lib/README.en.md#arduinocore-api) - The hardware-independent layer of the Arduino core. Include the corresponding API files when using Arduino-related libraries.

### [Android](./engine-sim-lib/README.en.md#android)

- [rawdrawandroid](./engine-sim-lib/README.en.md#rawdrawandroid) - A lightweight, cross-platform framework for developing Android applications in C.

### [Virtual Machines (Sandboxes)](./engine-sim-lib/README.en.md#virtual-machines-sandboxes)

- [EVM](./engine-sim-lib/README.en.md#evm) - An ultra-lightweight IoT virtual machine composed of a syntax-parsing frontend framework and a bytecode-execution backend. It runs on resource-constrained microcontrollers and supports running self-developed apps on this virtual-machine engine.
- [uvm32](./engine-sim-lib/README.en.md#uvm32) - A minimalist, dependency-free virtual-machine (RISC-V) sandbox designed for microcontrollers and other resource-constrained devices. It is a single C file with no dynamic memory allocation and an asynchronous architecture. It can replace script engines such as LUA and MicroPython.

### [Multimedia](./engine-sim-lib/README.en.md#multimedia)

- [FFmpeg](./engine-sim-lib/README.en.md#ffmpeg) - A highly renowned cross-platform audio/video processing framework that provides a suite of audio/video codec development tools.

### [Game Frameworks](./engine-sim-lib/README.en.md#game-frameworks)

- [Arduboy](./engine-sim-lib/README.en.md#arduboy) - Provides the programming interfaces required to make games, allowing players to create C/C++ games easily, run them on the platform, and share them through the community.
- [raylib](./engine-sim-lib/README.en.md#raylib) - A game library written entirely in C that provides simple video and game-programming capabilities.

---

## ✨ Additional Resources

### Library Classification Details

Open-source libraries are diverse. Similar functions may have different names in different contexts, while a single library may contain multiple subfunctions that could each form a separate category. This makes classification difficult.
For this reason, the collection is divided into three types: single-purpose, integrated-purpose, and other.

- [Single-purpose](#single-purpose) - Open-source libraries for a single function or domain, organized as `domain-function`;
- [Integrated-purpose](#integrated-purpose) - Packages or frameworks integrating multiple functions, organized by `domain`;
- [Other](#other) - Libraries adapted only to specific chip types or engines;

**Note: this collection does not list libraries that only support POSIX interfaces. Find them in [Other Related Open-Source Library Collections](#other-related-open-source-library-collections).* 

### Other Related Open-Source Library Collections

- [EmbedSummary: Embedded resource collection](https://gitee.com/zhengnianli/EmbedSummary)
- [nhivp/Awesome-Embedded: A curated list of awesome embedded programming.](https://github.com/nhivp/Awesome-Embedded)
- [fffaraz/awesome-cpp: A curated list of awesome C++ (or C) frameworks, libraries, resources, and shiny things. Inspired by awesome-... stuff.](https://github.com/fffaraz/awesome-cpp)
- [ESP Component Registry](https://components.espressif.com)

In addition, ESP32's official [ESP Component Registry](https://components.espressif.com) contains many libraries. The Arduino community also provides many libraries, searchable in the Arduino IDE or through [Arduino Library List - Arduino Libraries](https://www.arduinolibraries.info). Other vendor chips may require porting an [Arduino core](./engine-sim-lib/README.en.md#arduinocore-api).

---

## 🤝 Contributing

Contributions are welcome. See the [contribution guide](./CONTRIBUTING.md) for details.

<p align="right"><a href="#-contents">⬆TOP</a></p>

<!--lint enable awesome-list-item double-link-->
