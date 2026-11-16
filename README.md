# z8114ax-openwrt
# OpenWrt Support for ZBT Z8114AX-DS

Hi! 👋

This is my **very first time working on OpenWrt device support**, and this repository is where I'll document my journey of bringing OpenWrt support to my ZBT Z8114AX-DS router.

## Screenshot
![screenshot](https://github.com/vigilante-1337/openwrt-zbt-z8114ax/blob/main/assets/Screenshot_20261117_054227.png)

## Why This Router?

Funny enough, I originally bought this router to use as a travel router. The funny part? I actually hate going outside and don't really travel. 😂

I could have bought a device that already has official OpenWrt support, but I wanted something with specifications closer to my ZBT Z8102AX V2. That's how I ended up discovering the ZBT Z8114AX-DS.

It's compact enough to carry around, has a cool design, and has hardware that makes it an interesting device to experiment with.

Instead of choosing the easy route, I decided to try bringing OpenWrt support to it myself.

## Current Progress

- [x] Identify the SoC
- [x] Collect basic hardware information
- [x] Develop and test the device tree (DTS)
- [x] Verify NAND flash layout and partitions
- [x] Build and test a working OpenWrt image
- [x] Submit device support upstream (eventually!)

## Hardware

| Component      | Specification     |
|:-------------- |:------------------|
| SoC            | MediaTek MT7981B  |
| CPU            | 2× ARM Cortex-A53 |
| Wi-Fi          | MediaTek MT7976CN |
| RAM            | 512MB DDR4        |
| Flash          | 128MB SPI-NAND    |
| Ethernet       | 1× WAN + 1× LAN   |
| Switch         | MediaTek MT7531   |
| 5G Slot        | 1× M.2 slot       |
| SIM            | 2× Nano-SIM       |
| Wi-Fi antennas | 2× external       |
| 5G antennas    | 4× external       |
| MicroSD        | 1×                |
| UART           | 3.3V TTL          |
| USB            | 1× USB            |

## Mac Address
So the mac address live on the Factory partition so you just want to dump the partition and run hexadecimal dump tool like *xxd* and you will see something like this

| Label | Mac Address       | Offset |
|:-----:|:-----------------:|:------:|
| LAN   | f8:5e:3c:9d:b9:xx | 0x2a   |
| WAN   | f8:5e:3c:9d:b9:xx | 0x24   |
| 2.4G  | f8:5e:3c:9d:b9:xx | 0x04   |
| 5.8G  | f8:5e:3c:9d:b9:xx | 0x0a   |

## Disclaimer

This is a work in progress and my first attempt at adding support for an OpenWrt device. Some information and changes may be experimental or untested.

I'm learning as I go, documenting my findings, and figuring things out one step at a time.

If you're interested in this device or have any suggestions, feel free to follow along!

Thanks for stopping by! ❤️
