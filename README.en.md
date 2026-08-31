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

- ~~[key_detect](./io-control-lib/README.en.md#key_detect) - A simple event-registration button detection component with basic button functionality.~~ (pending release)
- [key_module](./io-control-lib/README.en.md#key_module) - A simple, easy-to-use button detection module using event callbacks.
- [FlexibleButton](./io-control-lib/README.en.md#flexiblebutton) - An ultra-lightweight button library using polling scans.
- [MultiButton](./io-control-lib/README.en.md#multibutton) - A standard button library that manages each button structure independently.
- [cotKey](./io-control-lib/README.en.md#cotkey) - A listener-based button recognition library for click, double-click, multi-click, short-press, and long-press actions.
- [key_board](./io-control-lib/README.en.md#key_board) - A feature-rich button library with matrix-keyboard and combination support.
- [LwBTN](./io-control-lib/README.en.md#lwbtn) - A professional, highly configurable button-event management library.

### [LED](./io-control-lib/README.en.md#led)

- [cotLed](./io-control-lib/README.en.md#cotled) - A lightweight LED control module supporting multiple LED modes.
- [led_module](./io-control-lib/README.en.md#led_module) - A general LED display module based on object-oriented and simple-factory patterns.

### [PID](./io-control-lib/README.en.md#pid)

- [pid_temperature_control](./io-control-lib/README.en.md#pid_temperature_control) - A good PID temperature-control example that can be extended to other domains.

### [CNC](./io-control-lib/README.en.md#cnc)

- [Grbl](./io-control-lib/README.en.md#grbl) - A well-known open-source CNC codebase for cutters, plotters, drilling machines, and more.
- [µCNC](./io-control-lib/README.en.md#µcnc) - General-purpose CNC firmware for microcontrollers.

---

## [Timer and Time Library](./timer-time-lib/README.en.md)

### [Timers](./timer-time-lib/README.en.md#timers)

- [MultiTimer](./timer-time-lib/README.en.md#multitimer) - A software timer module that replaces conventional flag checks.
- [SmartTimer](./timer-time-lib/README.en.md#smarttimer) - A practical timer scheduler for bare-metal systems.
- [microseconds](./timer-time-lib/README.en.md#microseconds) - A Cortex-M SysTick microsecond timer with blocking and non-blocking delays.
- [perf_counter](./timer-time-lib/README.en.md#perf_counter) - A Cortex-M SysTick timer with cycle measurement and timing services.

### [Watchdogs](./timer-time-lib/README.en.md#watchdogs)

- [LwWDG](./timer-time-lib/README.en.md#lwwdg) - A lightweight watchdog library for monitoring multiple threads.

### [Time-related](./timer-time-lib/README.en.md#time-related)

- [LwDTC](./timer-time-lib/README.en.md#lwdtc) - A utility library for dates, times, and cron.

---

## [Memory and File System Library](./mem-fs-lib/README.en.md)

### [Memory Management](./mem-fs-lib/README.en.md#memory-management)

- [memory](./mem-fs-lib/README.en.md#memory) - A minimalist memory allocation and release module.
- [mem_malloc](./mem-fs-lib/README.en.md#mem_malloc) - A simple memory manager that avoids fragmentation.
- [tlsf](./mem-fs-lib/README.en.md#tlsf) - A TLSF heap allocator with $O(1)$ allocation complexity.
- [LwMEM](./mem-fs-lib/README.en.md#lwmem) - A professional memory manager focused on RTOS thread safety.
- [jemalloc](./mem-fs-lib/README.en.md#jemalloc) - A high-performance allocator for multithreaded workloads.
- [LWMalloc](./mem-fs-lib/README.en.md#lwmalloc) - A lightweight Linux dynamic allocator intended to replace ptmalloc.

### [Read/Write Wrapper Layer](./mem-fs-lib/README.en.md#readwrite-wrapper-layer)

- [flashMultipleErase](./mem-fs-lib/README.en.md#flashmultipleerase) - FLASH-based EEPROM emulation using sequential writes.
- [eepromfs](./mem-fs-lib/README.en.md#eepromfs) - A simple EEPROM-based file-like data read/write library.
- [Dhara](./mem-fs-lib/README.en.md#dhara) - A NAND Flash translation layer for small microcontrollers.
- [kFlashFile](./mem-fs-lib/README.en.md#kflashfile) - A lightweight NOR Flash file-data storage solution.
- [esp_partition](./mem-fs-lib/README.en.md#esp_partition) - ESP's partition-table library for block-based flash access.
- [NVS](./mem-fs-lib/README.en.md#nvs) - ESP's non-volatile key-value storage library.

### [File Systems](./mem-fs-lib/README.en.md#file-systems)

- [FatFs](./mem-fs-lib/README.en.md#fatfs) - A portable, configurable, and thread-safe file system.
- [JesFs](./mem-fs-lib/README.en.md#jesfs) - A lightweight serial NOR Flash file system for constrained embedded systems.
- [RanFs](./mem-fs-lib/README.en.md#ranfs) - A POSIX-compatible lightweight file system.
- [littlefs](./mem-fs-lib/README.en.md#littlefs) - A fail-safe microprocessor file system with wear leveling.
- [SPIFFS](./mem-fs-lib/README.en.md#spiffs) - A file system for low-memory devices using static RAM buffers.

---

## [Board-Level Bus Protocol Libraries](./board-bus-lib/README.en.md)

### [UART](./board-bus-lib/README.en.md#uart)

- [LwOW](./board-bus-lib/README.en.md#lwow) - A professional 1-Wire protocol library over UART or GPIO.
- [MUDLink](./board-bus-lib/README.en.md#mudlink) - A UART link/transport layer with framed-packet delivery.

### [CDbus](./board-bus-lib/README.en.md#cdbus)

- [CDBUS](./board-bus-lib/README.en.md#cdbus-1) - An efficient fieldbus compatible with UART and RS-485.

### [Modbus](./board-bus-lib/README.en.md#modbus)

- [freemodbus](./board-bus-lib/README.en.md#freemodbus) - A Modbus stack supporting both master and slave functions.
- [nanoMODBUS](./board-bus-lib/README.en.md#nanomodbus) - A compact, configurable Modbus library.

### [I2C](./board-bus-lib/README.en.md#i2c)

- ~~[i2c_scanner](./board-bus-lib/README.en.md#i2c_scanner) - An I2C device-scanning library extracted from Nordic's SDK.~~ (pending release)

### [SPI](./board-bus-lib/README.en.md#spi)

- [SFUD](./board-bus-lib/README.en.md#sfud) - A universal serial SPI Flash driver library.

### [Interboard Communication](./board-bus-lib/README.en.md#interboard-communication)

- [ESSL](./board-bus-lib/README.en.md#essl) - ESP's serial slave link component for MCU-to-MCU communication.
- [SACP](./board-bus-lib/README.en.md#sacp) - Snapmaker's multi-device data communication protocol.

### [USB](./board-bus-lib/README.en.md#usb)

- [TinyUSB](./board-bus-lib/README.en.md#tinyusb) - A memory-safe embedded USB host/device stack.
- [CherryUSB](./board-bus-lib/README.en.md#cherryusb) - A portable USB host/device stack for embedded systems.

---

## [Data Structure and Data Processing Libraries](./data-struct-process-lib/README.en.md)

### [Queues](./data-struct-process-lib/README.en.md#queues)

- [CBUF](./data-struct-process-lib/README.en.md#cbuf) - An elegant macro-based ring buffer.
- [sys/queue](./data-struct-process-lib/README.en.md#sysqueue) - Macro-based queue and linked-list headers for Linux and FreeBSD.
- [byte_queue](./data-struct-process-lib/README.en.md#byte_queue) - A macro-wrapped C ring queue for arbitrary types.
- [queue](./data-struct-process-lib/README.en.md#queue) - A general-purpose C queue for arbitrary data types.
- [Ring-Buffer](./data-struct-process-lib/README.en.md#ring-buffer) - A simple, efficient ring-buffer library.
- [wl_queue](./data-struct-process-lib/README.en.md#wl_queue) - A ring queue for arbitrary data types using C overloading techniques.
- [RingBuffer](./data-struct-process-lib/README.en.md#ringbuffer) - A fully featured heap-allocated ring-buffer library.
- [queue](./data-struct-process-lib/README.en.md#queue-1) - An extensible queue with zero-copy reads and writes.
- [QueueForMcu](./data-struct-process-lib/README.en.md#queueformcu) - A queue module for non-RTOS microcontroller systems.
- [ConcurrentQueue](./data-struct-process-lib/README.en.md#concurrentqueue) - An industrial-grade C++ lock-free queue.
- [LwRB](./data-struct-process-lib/README.en.md#lwrb) - A professional FIFO ring buffer without dynamic allocation.
- [fifofast](./data-struct-process-lib/README.en.md#fifofast) - A FIFO library optimized for MCU CPU and SRAM use.

### [Streams](./data-struct-process-lib/README.en.md#streams)

- ~~[uart_stream](./data-struct-process-lib/README.en.md#uart_stream) - A UART data-stream buffer-processing library.~~ (pending release)
- [xprintf](./data-struct-process-lib/README.en.md#xprintf) - Embedded string functions with dynamic peripheral output.
- [CMSIS-Stream](./data-struct-process-lib/README.en.md#cmsis-stream) - ARM's data-stream processing component with graphical representations.

### [Data Structure Collections](./data-struct-process-lib/README.en.md#data-structure-collections)

- [uthash](./data-struct-process-lib/README.en.md#uthash) - Header-only hash, list, ring, and other data structures.

### [Databases](./data-struct-process-lib/README.en.md#databases)

- [cotParam](./data-struct-process-lib/README.en.md#cotparam) - Table-driven parameter management.
- [EasyFlash](./data-struct-process-lib/README.en.md#easyflash) - A lightweight Key-Value database for embedded data.
- [FlashDB](./data-struct-process-lib/README.en.md#flashdb) - KV and TS databases focused on storage.
- [Nanopb](./data-struct-process-lib/README.en.md#nanopb) - A lightweight C implementation of Protobuf.
- [ITTIA DB](./data-struct-process-lib/README.en.md#ittia-db) - A commercial real-time embedded database.
- [linq4c](./data-struct-process-lib/README.en.md#linq4c) - C implementations of C# LINQ methods.
- [SQLite](./data-struct-process-lib/README.en.md#sqlite) - The widely used embedded SQL database.

### [Compression Libraries](./data-struct-process-lib/README.en.md#compression-libraries)

- [lz4](./data-struct-process-lib/README.en.md#lz4) - A very fast lossless compression library.
- [heatshrink](./data-struct-process-lib/README.en.md#heatshrink) - An ultra-low-resource embedded decompression library.
- [TJpgDec](./data-struct-process-lib/README.en.md#tjpgdec) - A JPEG decompressor optimized for embedded systems.

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

- [dbuglib](./log-term-lib/README.en.md#dbuglib) - A compact logging library with configurable log levels.
- [log.c](./log-term-lib/README.en.md#logc) - A minimalist C99 logging library.
- [log](./log-term-lib/README.en.md#log) - A compact logging module with time and source information.
- [alog](./log-term-lib/README.en.md#alog) - A streamlined colored logging component with mutexes.
- [LwPRINTF](./log-term-lib/README.en.md#lwprintf) - A safe, reentrant standard-output utility library.
- [EasyLogger](./log-term-lib/README.en.md#easylogger) - A flexible, thread-safe logger with async output.
- [zlog](./log-term-lib/README.en.md#zlog) - A reliable, high-performance pure C logging library.

### [Terminal Interaction](./log-term-lib/README.en.md#terminal-interaction)

- [cmd-parser](./log-term-lib/README.en.md#cmd-parser) - A minimalist command parser.
- [LwSHELL](./log-term-lib/README.en.md#lwshell) - A lightweight shell library with command descriptions.
- [debugcmd](./log-term-lib/README.en.md#debugcmd) - A full-featured command-line parser with completion.
- [Argtable3](./log-term-lib/README.en.md#argtable3) - A POSIX-style command-line parser.
- [nr_micro_shell](./log-term-lib/README.en.md#nr_micro_shell) - A command-line interaction library with history and completion.
- [letter shell](./log-term-lib/README.en.md#letter-shell) - A powerful embedded command-line interaction library.
- [Xradio_console](./log-term-lib/README.en.md#xradio_console) - A hierarchical RTOS console extracted from the Xradio SDK.
- [easyShell](./log-term-lib/README.en.md#easyshell) - A simple microcontroller shell with Tab completion.

---

## [Validation, Security, Boot, and Update Library](./secure-boot-update-lib/README.en.md)

### [Validation and Security](./secure-boot-update-lib/README.en.md#validation-and-security)

- [crc-lib-c](./secure-boot-update-lib/README.en.md#crc-lib-c) - A minimalist CRC library with common parameter models.
- [tiny-AES-c](./secure-boot-update-lib/README.en.md#tiny-aes-c) - A compact portable AES library with ECB, CTR, and CBC modes.
- ~~[key](./secure-boot-update-lib/README.en.md#key) - A minimalist key-based encryption algorithm.~~ (pending release)
- [wolfCrypt](./secure-boot-update-lib/README.en.md#wolfcrypt) - wolfSSL's lightweight cryptography library.
- [wolfSSL](./secure-boot-update-lib/README.en.md#wolfssl) - A portable SSL/TLS library for IoT, embedded, and RTOS use.
- [Mbed TLS](./secure-boot-update-lib/README.en.md#mbed-tls) - A widely used SSL/TLS library from TrustedFirmware.
- [wolfHSM](./secure-boot-update-lib/README.en.md#wolfhsm) - A client-server framework for hardware cryptography and secure processing.
- [wolfTPM](./secure-boot-update-lib/README.en.md#wolftpm) - A portable TPM protocol stack.
- [wolfSentry](./secure-boot-update-lib/README.en.md#wolfsentry) - An embedded-ready intrusion detection and prevention firewall engine.

### [Boot and Update](./secure-boot-update-lib/README.en.md#boot-and-update)

- [Tiny Bootloader](./secure-boot-update-lib/README.en.md#tiny-bootloader) - A small bootloader for 8-bit and 32-bit microcontrollers.
- [OpenBLT](./secure-boot-update-lib/README.en.md#openblt) - A well-known microcontroller bootloader.
- [wolfBoot](./secure-boot-update-lib/README.en.md#wolfboot) - A secure 32-bit microcontroller bootloader.
- [mOTA](./secure-boot-update-lib/README.en.md#mota) - A 32-bit MCU update component using YModem-1K.
- [MicorBoot](./secure-boot-update-lib/README.en.md#micorboot) - A bootloader module optimized for MCU updates.
- [MCUboot](./secure-boot-update-lib/README.en.md#mcuboot) - A system-independent secure bootloader for 32-bit MCUs.

---

## [UI and Menu Library](./ui-menu-lib/README.en.md)

### [HMI](./ui-menu-lib/README.en.md#hmi)

- [tslib](./ui-menu-lib/README.en.md#tslib) - A widely used embedded resistive-touchscreen calibration library.
- [tslib_for_mcu](./ui-menu-lib/README.en.md#tslib_for_mcu) - A Linux-trimmed resistive touchscreen calibration library.

### [Monochrome](./ui-menu-lib/README.en.md#monochrome)

- [ECBM_GUI](./ui-menu-lib/README.en.md#ecbm_gui) - A basic monochrome GUI using an internal display buffer.
- [SimpleGUI](./ui-menu-lib/README.en.md#simplegui) - A monochrome-display GUI with simple drawing functions.
- [oledlib](./ui-menu-lib/README.en.md#oledlib) - An open-source OLED graphics library.
- [U8g2](./ui-menu-lib/README.en.md#u8g2) - A monochrome display library with controller support.
- [MonoGUI](./ui-menu-lib/README.en.md#monogui) - A full-featured GUI system for small monochrome devices.
- [WouoUI](./ui-menu-lib/README.en.md#wououi) - An encoder-controlled, smooth MonoUI-inspired interface.
- [astra UI](./ui-menu-lib/README.en.md#astra-ui) - A C++ OLED multi-level menu UI with transition animations.
- [GLCD](./ui-menu-lib/README.en.md#glcd) - A graphical LCD library with drivers, text, and basic graphics.

### [Color](./ui-menu-lib/README.en.md#color)

- [GuiLite](./ui-menu-lib/README.en.md#guilite) - An ultra-lightweight multi-platform GUI library.
- [Olive.c](./ui-menu-lib/README.en.md#olivec) - A simple 2D graphics library for C.
- [microui](./ui-menu-lib/README.en.md#microui) - A tiny portable UI library for basic rendering systems.
- [LingLongGUI](./ui-menu-lib/README.en.md#linglonggui) - A GUI generation library with a graphical editor.
- [LingDongGUI](./ui-menu-lib/README.en.md#lingdonggui) - An Arm-2D wrapper GUI library.
- [AAGUI](./ui-menu-lib/README.en.md#aagui) - A cross-platform Android-like embedded GUI.
- [GT-HMI](./ui-menu-lib/README.en.md#gt-hmi) - A UI library with fonts, a simulator, and PC tools.
- [LVGL](./ui-menu-lib/README.en.md#lvgl) - A lightweight general-purpose graphics library.
- [AWTK](./ui-menu-lib/README.en.md#awtk) - A powerful GUI graphics library.
- [TouchGFX](./ui-menu-lib/README.en.md#touchgfx) - STM32's GUI graphics library.
- [GUIX](./ui-menu-lib/README.en.md#guix) - Azure RTOS's GUI graphics library.
- [emWin](./ui-menu-lib/README.en.md#emwin) - Segger's licensable GUI graphics library.
- [Embedded Wizard GUI](./ui-menu-lib/README.en.md#embedded-wizard-gui) - A powerful paid GUI graphics library.
- [Qt for MCU](./ui-menu-lib/README.en.md#qt-for-mcu) - Qt's paid embedded GUI library.
- [μGFX](./ui-menu-lib/README.en.md#μgfx) - A performance-oriented touchscreen UI library.
- [MiniGUI](./ui-menu-lib/README.en.md#minigui) - A customizable multi-platform UI library.
- [μGUI](./ui-menu-lib/README.en.md#μgui) - A platform-independent, single-source-file graphics library.
- [Aeropoint GUI](./ui-menu-lib/README.en.md#aeropoint-gui) - A paid PPT-based GUI creation tool.
- [Clay](./ui-menu-lib/README.en.md#clay) - A responsive 2D UI layout library.
- [Nuklear](./ui-menu-lib/README.en.md#nuklear) - A dependency-free immediate-mode GUI toolkit.
- [LinaVG](./ui-menu-lib/README.en.md#linavg) - A 2D vector-graphics rendering library.
- [BlurHash](./ui-menu-lib/README.en.md#blurhash) - An image placeholder algorithm and implementation.
- [OpenGL](./ui-menu-lib/README.en.md#opengl) - A cross-platform 2D/3D rendering library.
- [Rawdraw](./ui-menu-lib/README.en.md#rawdraw) - A cross-platform dependency-free UI drawing system.
- [TinyGL](./ui-menu-lib/README.en.md#tinygl) - A compact OpenGL implementation for embedded systems.
- [foolrenderer](./ui-menu-lib/README.en.md#foolrenderer) - A C software renderer with OpenGL-like features.
- [EmberGL](./ui-menu-lib/README.en.md#embergl) - An MCU 2D/3D raster rendering library.
- [Cairo](./ui-menu-lib/README.en.md#cairo) - A multi-output 2D graphics library.

### [Acceleration](./ui-menu-lib/README.en.md#acceleration)

- [Arm-2D](./ui-menu-lib/README.en.md#arm-2d) - A Cortex-M 2D graphics acceleration library.
- [GUIslice](./ui-menu-lib/README.en.md#guislice) - A lightweight GUI framework with a layout tool.

### [Graphics](./ui-menu-lib/README.en.md#graphics)

- [qrencode](./ui-menu-lib/README.en.md#qrencode) - A QR-code generation library for microcontrollers.
- [QR Code generator library](./ui-menu-lib/README.en.md#qr-code-generator-library) - A multi-language general QR-code generator.
- [QRCode](./ui-menu-lib/README.en.md#qrcode) - A QR-code generator optimized for constrained systems.

### [Glyphs](./ui-menu-lib/README.en.md#glyphs)

- [MCUFont](./ui-menu-lib/README.en.md#mcufont) - A library for font compression, decompression, and rendering.
- [Unicorn](./ui-menu-lib/README.en.md#unicorn) - A C99 Unicode encoding and decoding library.

### [Menu Frameworks](./ui-menu-lib/README.en.md#menu-frameworks)

- [zBitsView](./ui-menu-lib/README.en.md#zbitsview) - A virtual multi-level menu in the logic layer.
- [emenu](./ui-menu-lib/README.en.md#emenu) - A menu framework whose structure is represented in code.
- ~~[Menu](./ui-menu-lib/README.en.md#menu) - A simple practical menu framework.~~ (pending release)
- [cotMenu](./ui-menu-lib/README.en.md#cotmenu) - A linked-list-based multi-level menu framework.
- [MiaoUI](./ui-menu-lib/README.en.md#miaoui) - A U8g2 OLED menu framework.
- [MultMenu](./ui-menu-lib/README.en.md#multmenu) - Multi-level menus with monochrome OLED nonlinear animation.
- [SMF](./ui-menu-lib/README.en.md#smf) - A C++ multi-level menu framework.
- [PageManager](./ui-menu-lib/README.en.md#pagemanager) - A C++ page lifecycle management library.

---

## [Kernel and Foundation Framework Library](./kernel-framework-lib/README.en.md)

### [Events](./kernel-framework-lib/README.en.md#events)

- [cpost](./kernel-framework-lib/README.en.md#cpost) - A lightweight event-driven context-switching and task-decoupling library.
- [LwEVT](./kernel-framework-lib/README.en.md#lwevt) - A professional event-module library.

### [Messages](./kernel-framework-lib/README.en.md#messages)

- [YAMI4](./kernel-framework-lib/README.en.md#yami4) - A distributed-system messaging library.
- [ZeroMQ](./kernel-framework-lib/README.en.md#zeromq) - A high-performance asynchronous messaging library.
- [CDIPC](./kernel-framework-lib/README.en.md#cdipc) - An IPC mechanism and library for real-time systems.

### [Pipes](./kernel-framework-lib/README.en.md#pipes)

- [readerwriterqueue](./kernel-framework-lib/README.en.md#readerwriterqueue) - A fast C++ single-producer, single-consumer lock-free queue.

### [Mailboxes](./kernel-framework-lib/README.en.md#mailboxes)

- [DataCenter](./kernel-framework-lib/README.en.md#datacenter) - A C++ publish-subscribe mailbox framework.

### [Thread Management](./kernel-framework-lib/README.en.md#thread-management)

- [C Thread Pool](./kernel-framework-lib/README.en.md#c-thread-pool) - A lightweight embedded thread-pool library.

### [Driver Frameworks](./kernel-framework-lib/README.en.md#driver-frameworks)

- ~~[initcall](./kernel-framework-lib/README.en.md#initcall) - An extracted RT-Thread initialization framework.~~ (pending release)
- ~~[platform_dev](./kernel-framework-lib/README.en.md#platform_dev) - A simplified Linux-inspired driver framework.~~ (pending release)
- [c-periphery](./kernel-framework-lib/README.en.md#c-periphery) - A Linux hardware-peripheral abstraction-layer template.

### [Sensor Frameworks](./kernel-framework-lib/README.en.md#sensor-frameworks)

- ~~[senser_algorithm](./kernel-framework-lib/README.en.md#senser_algorithm) - A sensor data-processing framework for RTOS.~~ (pending release)

### [Module Frameworks](./kernel-framework-lib/README.en.md#module-frameworks)

- [RIL](./kernel-framework-lib/README.en.md#ril) - Wireless module management software for embedded platforms.

### [State Machines](./kernel-framework-lib/README.en.md#state-machines)

- [EFSMC](./kernel-framework-lib/README.en.md#efsmc) - An event-driven finite state machine.
- [signals_slots](./kernel-framework-lib/README.en.md#signals_slots) - A lightweight signal-and-slot framework.
- [UML State Machine in C](./kernel-framework-lib/README.en.md#uml-state-machine-in-c) - A lightweight C state-machine framework.

### [Dynamic Loading](./kernel-framework-lib/README.en.md#dynamic-loading)

- [dynamic_loader](./kernel-framework-lib/README.en.md#dynamic_loader) - A dynamic-loading library trimmed from RT-Thread libdl.

---

## [Exception Snapshot and Testing Libraries](./exception-test-lib/README.en.md)

### [Coredump](./exception-test-lib/README.en.md#coredump)

- [CmBacktrace](./exception-test-lib/README.en.md#cmbacktrace) - A well-known ARM Cortex-M error-tracing library.

### [Exception Handling](./exception-test-lib/README.en.md#exception-handling)

- ~~[try](./exception-test-lib/README.en.md#try) - C-style try-catch exception handling.~~ (pending release)
- [CException](./exception-test-lib/README.en.md#cexception) - Simple portable C exception handling.
- [MLA](./exception-test-lib/README.en.md#mla) - A compact memory-leak analysis library.

### [Testing](./exception-test-lib/README.en.md#testing)

- ~~[MTTEST](./exception-test-lib/README.en.md#mttest) - A registration-based RTOS testing framework.~~ (pending release)
- [MinUnit](./exception-test-lib/README.en.md#minunit) - A minimal C unit-testing framework.
- [CuTest](./exception-test-lib/README.en.md#cutest) - A minimalist C unit-testing framework.
- [cmockery](./exception-test-lib/README.en.md#cmockery) - A lightweight C unit-testing framework.
- [EEMBC](./exception-test-lib/README.en.md#eembc) - Embedded performance-testing suites and standards.
- [Unity](./exception-test-lib/README.en.md#unity) - A C unit-testing framework for embedded toolchains.
- [greatest](./exception-test-lib/README.en.md#greatest) - A compact C testing system.
- [Catch2](./exception-test-lib/README.en.md#catch2) - A lightweight header-only C++ test framework.

---

## [Algorithms and AI Libraries](./algo-ai-lib/README.en.md)

### [Arithmetic](./algo-ai-lib/README.en.md#arithmetic)

- ~~[float_converter](./algo-ai-lib/README.en.md#float_converter) - Floating-point rounding and integer conversion.~~ (pending release)
- [LibBF](./algo-ai-lib/README.en.md#libbf) - A high-precision floating-point arithmetic library.

### [Fundamental Algorithms](./algo-ai-lib/README.en.md#fundamental-algorithms)

- [FXT](./algo-ai-lib/README.en.md#fxt) - A C algorithm collection for bit operations and combinatorics.
- [xxHash](./algo-ai-lib/README.en.md#xxhash) - An extremely fast non-cryptographic hash algorithm.
- [Terathon Math Library](./algo-ai-lib/README.en.md#terathon-math-library) - A C++ library for vectors, matrices, and geometry.

### [AI Frameworks](./algo-ai-lib/README.en.md#ai-frameworks)

- [TinyMaix](./algo-ai-lib/README.en.md#tinymaix) - An AI neural-network inference framework for constrained MCUs.
- [miniMNIST-c](./algo-ai-lib/README.en.md#minimnist-c) - A two-layer C neural network for learning.
- [Genann](./algo-ai-lib/README.en.md#genann) - A minimal C feedforward neural-network library.
- [uTensor](./algo-ai-lib/README.en.md#utensor) - A lightweight TensorFlow-based inference framework.
- [NNoM](./algo-ai-lib/README.en.md#nnom) - A neural-network framework for MCUs.
- [Paddle Lite](./algo-ai-lib/README.en.md#paddle-lite) - A flexible lightweight deep-learning inference framework.
- [TVM](./algo-ai-lib/README.en.md#tvm) - An end-to-end deep-learning compiler framework.
- [tflite-micro](./algo-ai-lib/README.en.md#tflite-micro) - TensorFlow Lite for microcontrollers.
- [ncnn](./algo-ai-lib/README.en.md#ncnn) - A high-performance neural-network inference framework.
- [MNN](./algo-ai-lib/README.en.md#mnn) - A lightweight deep neural-network engine.
- [TensorFlow Lite](./algo-ai-lib/README.en.md#tensorflow-lite) - A machine-learning library for edge deployment.
- [Mediapipe](./algo-ai-lib/README.en.md#mediapipe) - Google's cross-platform machine-learning framework.
- [Edge Impulse](./algo-ai-lib/README.en.md#edge-impulse) - An embedded machine-learning development platform.
- [YMCV](./algo-ai-lib/README.en.md#ymcv) - A pure C cross-platform miniature computer-vision library.
- [NeuralNetwork](./algo-ai-lib/README.en.md#neuralnetwork) - A resource-conscious neural-network library for MCUs.

### [AI Models and Algorithms](./algo-ai-lib/README.en.md#ai-models-and-algorithms)

- ~~[Knn](./algo-ai-lib/README.en.md#knn) - A basic unoptimized KNN algorithm in C.~~ (pending release)
- [NanoDet-Plus](./algo-ai-lib/README.en.md#nanodet-plus) - A lightweight anchor-free object-detection model.
- [pico](./algo-ai-lib/README.en.md#pico) - A lightweight pixel-comparison face-recognition algorithm.

---

## [System and Thread Library](./sys-thread-lib/README.en.md)

### [Time-Slice Scheduling Systems](./sys-thread-lib/README.en.md#time-slice-scheduling-systems)

- [ztask](./sys-thread-lib/README.en.md#ztask) - An extremely simple time-slice scheduler.
- [ETP](./sys-thread-lib/README.en.md#etp) - A time-slice polling framework.
- [cotTask](./sys-thread-lib/README.en.md#cottask) - A timer-based task-scheduling framework.
- [CodeBrick](./sys-thread-lib/README.en.md#codebrick) - A practical bare-metal software management system.
- [vkern](./sys-thread-lib/README.en.md#vkern) - A timer-based foreground-background scheduling kernel.
- [cola_os](./sys-thread-lib/README.en.md#cola_os) - A task-managed foreground-background system.
- [JxOS](./sys-thread-lib/README.en.md#jxos) - A feature-complete foreground-background system.
- [EventOS](./sys-thread-lib/README.en.md#eventos) - An event-driven embedded system.
- [BabyOS](./sys-thread-lib/README.en.md#babyos) - A registration-service bare-metal MCU framework.

### [Quasi-Real-Time Systems](./sys-thread-lib/README.en.md#quasi-real-time-systems)

- [cotOs](./sys-thread-lib/README.en.md#cotos) - A query-based cooperative multitasking system.
- [BasicOS](./sys-thread-lib/README.en.md#basicos) - A cooperative system with a shared task stack.
- [TaskScheduler](./sys-thread-lib/README.en.md#taskscheduler) - A configurable cooperative multitasking framework.
- [QuarkTS](./sys-thread-lib/README.en.md#quarkts) - An event-driven multitasking scheduler.
- [VSF](./sys-thread-lib/README.en.md#vsf) - An event-driven preemptive multitasking framework.

### [RTOS](./sys-thread-lib/README.en.md#rtos)

- [KLite](./sys-thread-lib/README.en.md#klite) - A concise embedded RTOS.
- [FreeRTOS](./sys-thread-lib/README.en.md#freertos) - A widely used RTOS with abundant materials.
- [uC/OS](./sys-thread-lib/README.en.md#ucos) - A mature RTOS with more features than FreeRTOS.
- [RT-Thread](./sys-thread-lib/README.en.md#rt-thread) - A practical RTOS with many components.
- [RTX](./sys-thread-lib/README.en.md#rtx) - ARM's RTOS with strong Keil compatibility.
- [NuttX](./sys-thread-lib/README.en.md#nuttx) - A compact standards-compatible operating system.
- [embOS](./sys-thread-lib/README.en.md#embos) - SEGGER's RTOS for non-commercial use.
- [Azure RTOS](./sys-thread-lib/README.en.md#azure-rtos) - Microsoft's RTOS.
- [Zephyr](./sys-thread-lib/README.en.md#zephyr) - A Linux-maintained RTOS.
- [At-RTOS](./sys-thread-lib/README.en.md#at-rtos) - A user-friendly embedded-controller RTOS.
- [Embox](./sys-thread-lib/README.en.md#embox) - An OS that supports Linux open-source components.
- [YiYiYa OS](./sys-thread-lib/README.en.md#yiyiya-os) - A full-featured OS for phone-like products.
- [LK](./sys-thread-lib/README.en.md#lk) - Little Kernel, a small embedded system.
- [SKRTOS_sparrow](./sys-thread-lib/README.en.md#skrtos_sparrow) - An ultra-small OS with basic scheduling and IPC.
- [CosyOS](./sys-thread-lib/README.en.md#cosyos) - A zero-interrupt-latency operating system.
- [scmRTOS](./sys-thread-lib/README.en.md#scmrtos) - A lightweight C++ RTOS.
- [MuditaOS](./sys-thread-lib/README.en.md#muditaos) - A FreeRTOS-based mobile OS for E-Ink displays.

### [IoT-RTOS](./sys-thread-lib/README.en.md#iot-rtos)

- [Contiki-NG](./sys-thread-lib/README.en.md#contiki-ng) - A low-power IoT operating system.
- [Mbed OS](./sys-thread-lib/README.en.md#mbed-os) - ARM's easy-to-use IoT operating system.
- [Huawei LiteOS](./sys-thread-lib/README.en.md#huawei-liteos) - Huawei's lightweight IoT OS.
- [Xiaomi Vela](./sys-thread-lib/README.en.md#xiaomi-vela) - Xiaomi's NuttX-based IoT OS.
- [AliOS Things](./sys-thread-lib/README.en.md#alios-things) - Alibaba's scalable IoT operating system.
- [TencentOS Tiny](./sys-thread-lib/README.en.md#tencentos-tiny) - Tencent's IoT real-time operating system.
- [OneOS](./sys-thread-lib/README.en.md#oneos) - China Mobile's lightweight IoT OS.
- [LuatOS](./sys-thread-lib/README.en.md#luatos) - An embedded Lua runtime framework.
- [Lua-RTOS-ESP32](./sys-thread-lib/README.en.md#lua-rtos-esp32) - A Lua interpreter RTOS for ESP32.
- [Apache Mynewt OS](./sys-thread-lib/README.en.md#apache-mynewt-os) - An Apache OS for low-power wireless devices.
- [Mongoose OS](./sys-thread-lib/README.en.md#mongoose-os) - An IoT firmware development framework.
- [MicroPythonOS](./sys-thread-lib/README.en.md#micropythonos) - A MicroPython operating system for MCUs and desktops.

### [ROS](./sys-thread-lib/README.en.md#ros)

- [ROS](./sys-thread-lib/README.en.md#ros-1) - A well-known open-source robot operating system.
- [AimRT](./sys-thread-lib/README.en.md#aimrt) - A Modern C++ runtime framework for robotics.

---

## [Module Collection Packages](./module-pack/README.en.md)

- [ToolKit](./module-pack/README.en.md#toolkit) - An embedded toolkit with a circular queue, timer, and event set.
- [lwUTIL](./module-pack/README.en.md#lwutil) - A utility toolkit for values, endianness, bits, and ASCII.
- [sc](./module-pack/README.en.md#sc) - A small high-performance data-structure toolkit.
- [cotUtils](./module-pack/README.en.md#cotutils) - A general C extension library with containers and serialization.
- [mr-library](./module-pack/README.en.md#mr-library) - A lightweight embedded framework with standardized drivers.
- [Zorb Framework](./module-pack/README.en.md#zorb-framework) - A lightweight, trim-friendly embedded framework.
- [Gear-Lib](./module-pack/README.en.md#gear-lib) - General POSIX C foundation libraries.
- [c-algorithms](./module-pack/README.en.md#c-algorithms) - Common algorithms and data structures for C.
- [klib](./module-pack/README.en.md#klib) - A lightweight C library of algorithms, structures, and parsers.
- [AMetal](./module-pack/README.en.md#ametal) - ZLG's bare-metal package with abstract interfaces.
- [eLab](./module-pack/README.en.md#elab) - An integrated embedded development platform.
- [TheAlgorithms](./module-pack/README.en.md#thealgorithms) - A large cross-language algorithms and data-structures collection.
- [simpostOS](./module-pack/README.en.md#simpostos) - A modern C++ modular design methodology and component collection.
- [PetiteDrv](./module-pack/README.en.md#petitedrv) - A layered general SDK library.
- [varch](./module-pack/README.en.md#varch) - Common embedded C algorithms, containers, parsers, and utilities.
- [ctool](./module-pack/README.en.md#ctool) - Utilities for variadic parameters, dates, memory testing, and more.
- [Generic_MCU_Software_Infrastructure](./module-pack/README.en.md#generic_mcu_software_infrastructure) - Software infrastructure for high-level abstractions.
- [appkit](./module-pack/README.en.md#appkit) - A C++ Linux application-development library.
- [GLib](./module-pack/README.en.md#glib) - GTK's core library with many foundational utilities.

---

## [Chip and Toolchain Adaptation Libraries](./chip-toolchain-lib/README.en.md)

### [51](./chip-toolchain-lib/README.en.md#51)

- [8051-ELL](./chip-toolchain-lib/README.en.md#8051-ell) - A 51-series chip extension library.
- [ECBM](./chip-toolchain-lib/README.en.md#ecbm) - A 51-series peripheral function library.

### [AVR](./chip-toolchain-lib/README.en.md#avr)

### [ST](./chip-toolchain-lib/README.en.md#st)

- [STM32F4 Discovery](./chip-toolchain-lib/README.en.md#stm32f4-discovery) - STM32F4 drivers, tutorials, and examples.

### [ESP](./chip-toolchain-lib/README.en.md#esp)

- [LwESP](./chip-toolchain-lib/README.en.md#lwesp) - An AT parser for ESP-device communication.
- [ESPUI](./chip-toolchain-lib/README.en.md#espui) - A simple Web UI library for ESP32 and ESP8266.
- [FluidNC](./chip-toolchain-lib/README.en.md#fluidnc) - CNC firmware optimized for ESP32 controllers.
- [Rabbit GRBL](./chip-toolchain-lib/README.en.md#rabbit-grbl) - Optimized ESP32 CNC firmware.

### [SIMCom](./chip-toolchain-lib/README.en.md#simcom)

- [LwCELL](./chip-toolchain-lib/README.en.md#lwcell) - An AT parser for SIMCom devices.

### [MDK](./chip-toolchain-lib/README.en.md#mdk)

- [flash_blob](./chip-toolchain-lib/README.en.md#flash_blob) - A generic flash-driver generator using MDK FLM files.

### [Driver](./chip-toolchain-lib/README.en.md#driver)

- [LibDriver](./chip-toolchain-lib/README.en.md#libdriver) - An open-source organization with 140+ peripheral drivers.

---

## [Engine (Simulation) Libraries](./engine-sim-lib/README.en.md)

### [SoftFP](./engine-sim-lib/README.en.md#softfp)

- [SoftFP](./engine-sim-lib/README.en.md#softfp-1) - Software floating-point implementation without an FPU.

### [C++](./engine-sim-lib/README.en.md#c)

- [sds](./engine-sim-lib/README.en.md#sds) - A simple heap-based dynamic string library for C.
- [STR](./engine-sim-lib/README.en.md#str) - An advanced string-processing library.
- [etl](./engine-sim-lib/README.en.md#etl) - An embedded C++ template library.
- [LW_OOPC](./engine-sim-lib/README.en.md#lw_oopc) - An embedded object-oriented programming extension.
- [PLOOC](./engine-sim-lib/README.en.md#plooc) - C extensions for object-oriented programming.
- [vlib](./engine-sim-lib/README.en.md#vlib) - A C template library similar to C++ STL.

### [Lua](./engine-sim-lib/README.en.md#lua)

- [MicroLua](./engine-sim-lib/README.en.md#microlua) - A LUA package for Raspberry Pi Pico.
- [eLua](./engine-sim-lib/README.en.md#elua) - A Lua engine for embedded systems.

### [Python](./engine-sim-lib/README.en.md#python)

- [PikaPython](./engine-sim-lib/README.en.md#pikapython) - An ultra-lightweight zero-dependency Python engine.

### [Rust](./engine-sim-lib/README.en.md#rust)

- [Rust Embedded](./engine-sim-lib/README.en.md#rust-embedded) - End-to-end Rust support for constrained and nontraditional platforms.

### [JavaScript](./engine-sim-lib/README.en.md#javascript)

- [mJS](./engine-sim-lib/README.en.md#mjs) - A compact ES6 JavaScript engine for microcontrollers.

### [Arduino](./engine-sim-lib/README.en.md#arduino)

- [ArduinoCore-API](./engine-sim-lib/README.en.md#arduinocore-api) - The hardware-independent Arduino core API layer.

### [Android](./engine-sim-lib/README.en.md#android)

- [rawdrawandroid](./engine-sim-lib/README.en.md#rawdrawandroid) - A lightweight C framework for Android applications.

### [Virtual Machines (Sandboxes)](./engine-sim-lib/README.en.md#virtual-machines-sandboxes)

- [EVM](./engine-sim-lib/README.en.md#evm) - An ultra-lightweight IoT virtual machine.
- [uvm32](./engine-sim-lib/README.en.md#uvm32) - A minimalist RISC-V virtual-machine sandbox.

### [Multimedia](./engine-sim-lib/README.en.md#multimedia)

- [FFmpeg](./engine-sim-lib/README.en.md#ffmpeg) - A cross-platform audio/video processing framework.

### [Game Frameworks](./engine-sim-lib/README.en.md#game-frameworks)

- [Arduboy](./engine-sim-lib/README.en.md#arduboy) - Programming interfaces for making and sharing C/C++ games.
- [raylib](./engine-sim-lib/README.en.md#raylib) - A simple C library for video and game programming.

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
