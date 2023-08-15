# nRF ZBOSS NCP

This repository contains compiled ZBOSS NCP firmware images for Nordic Semiconductor with nRF52840 SoC, like the [nRF52840 Dongle](https://www.nordicsemi.com/Products/Development-hardware/nrf52840-dongle).

Compared to Nordic Semi's default NCP Host example this image has been configured to use maximum memory.

This is a prebuilt hex image of Nordic Semi's NCP Host example (a ZBOSS-based tool for running the host side of the Network Co-Processor design) that has been tested with [zigpy-zboss](https://github.com/kardia-as/zigpy-zboss) (a ZBOSS radio library for [zigpy](https://github.com/zigpy/)).

You can flash the device with this firmware image using for example the programmer application from the [nRF Desktop application](https://www.nordicsemi.com/Products/Development-tools/nrf-connect-for-desktop).

References:
* https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/protocols/zigbee/tools.html#ug-zigbee-tools-ncp-host
* https://developer.nordicsemi.com/Zigbee/ncp_sdk_for_host/
* https://developer.nordicsemi.com/nRF_Connect_SDK/doc/zboss/3.11.2.1/zboss_ncp_host_intro.html
* https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/nrf/samples/zigbee/ncp/README.html#zigbee-ncp-sample
