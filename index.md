---

layout: col-sidebar
title: OWASP Automotive EMB 60
tags: example-tag
level: 1
type: 
pitch: 

---

## Description
Automotive security can be difficult to get into. Resources are limited and specialized hardware is needed. This open source project's goal is to lower this hurdle by providing an inexpensive and highly customizable device designed for practical automotive security use-cases.

The Automotive EMB60 (Embedded60) is a single-board computer which in its basic form can be used as a CAN-to-USB interface to connect a device to a CAN-Bus (Controller Area Network) over USB. It was developed in the context of a research project for penetration test driven safety and security system improvements for cyber-critical systems. The EMB60 specifically targets penetration testing in the automotive area where CAN is the prevalent communication standard. It's a full open source project providing open hardware and software. This allows for extensive customization and various other use-cases. 

## Feature Overview
* Powerful Microcontroller
* Real-time capabilities
* Supports CAN FD
* Supports common communication interfaces
* Growing software ecosystem
* Customizable
* Open source

## Hardware

* Microchip ATSAME70N21B Microcontroller
* 2 MCP2562FD High-Speed CAN FD Transceiver
* 2-Channel CAN FD Interface (Single D-Sub 9 Connector)
* USB-1.0/2.0 Type B
* Various other interfaces for expandability
* 40-pin Header (Pinout similar to a RaspberryPi: SPI, I2C, GPIO, ADC, ...)
* Button & 2 LEDs (Freely programmable)
* Memory Protection Unit (MPU)
* True Random Number Generator
* Hardware AES and SHA support

<p float="left">
    <img width="300" src="/pics/IMG_0171_small.jpg">
    <img width="300" src="/pics/IMG_0145_small.jpg">
    <img width="300" src="/pics/IMG_0170_small.jpg">
</p>


## Software
The EMB60 provides some libraries and firmwares out of the box. Since the device can be freely programmed it is not limited to them.
Existing firmwares include:

**CAN-to-USB Interface**
Provides two CAN interfaces through a USB connection. It implements the SocketCAN interface which is natively supported on linux and thus provides linux sockets to use. This allows the usage with already established tools like can-isotp and scapy.

**Secure Bootloader**
An open source secure bootloader being improved continuously.
* Firmwareupdate over automotive protocols (CAN using the protocols ISOTP and UDS)
* Confidentiality: Secure distribution of updates utilizing hardware accelerated AES-128-GCM encryption
* Integrity/Authenticity: Secure boot utilizing HMAC-SHA256 signatures (hardware accelerated)
* Keys stored in flash memory protected through MPU
* Does not rely on the firmware being secure
* Extensive RAM clear and other protection mechanisms








