# Meshed Banana
Meshed Banana is LoRa Router for the Reticulum Mesh protocol. It consists of a ESP32 LoRa device connected to a Banana Pi Zero M2 running the [reticulum mesh network stack](https://unsigned.io/projects/reticulum/).

<img src="https://github.com/Vault2501/Meshed-Banana-Device/wiki/pictures/Meshed_Banana.jpg" width="160">

## Price
All parts currently cost about 80 Euros.

## Case
All files for the 3D printed case are included in this repo, the stl files are also available on [thingiverse](https://www.thingiverse.com/thing:5359788).

## OS Image
Instructions on how to build an Armbian image can be found in the [Meshed Banana Image repo](https://github.com/Vault2501/Meshed-Banana-image)<br>
A pre built Meshed Banana OS image with reticulum stack and configuration is available on [Google Drive](https://drive.google.com/file/d/1DScvHtO_SD-lXaykb0QlwCe_j3PSC_U4/view?usp=sharing).

## Instructions
- [Parts](https://github.com/Vault2501/Meshed-Banana-Device/wiki/Parts)
- [Build](https://github.com/Vault2501/Meshed-Banana-Device/wiki/Build)
- [Assembly](https://github.com/Vault2501/Meshed-Banana-Device/wiki/Assembly)

## Usage
- [Setup](https://github.com/Vault2501/Meshed-Banana-Device/wiki/Setup)
- [Applications](https://github.com/Vault2501/Meshed-Banana-Device/wiki/Applications)

## Features
Reticulum, despite its stability, is still in an early stage. Therefor a number of features have not yet been implemented.<br>
It is an own protocol, requiring applications to make use of it. Currently there are only a number of examples and a chat application that can be used for testing.<br>
However, creating your own applications in Python is not very difficult and an introduction can be found [here](https://markqvist.github.io/Reticulum/manual/gettingstartedfast.html#develop-a-program-with-reticulum).<br>

Here a short overview of what works and what does not work yet:

### Working
- Mesh network functionality over TCP/IP, I2P, KISS, LoRa
- SMS like direct 1on1 chat using a terminal application or an Android phone
- Serving and accessing pages written in a markdown like language
- Sending and receiving files
- Using the reticulum capable [Sideband Android App](https://unsigned.io/sideband/)

### Not working
- Group chat
- A lot I can't think of right now
- For more details on reticulum features and a road map, please check out the [documentation on reticulum](https://markqvist.github.io/Reticulum/manual/)

## FAQ
**Q:** Why a Banana Pi Zero?<br>
**A:**<br>
Simply due to the sparsity of the Raspberry Pi Zero, the Banana Pi version was chosen as it has the same size and thus can be exchanged, giving you the option of a Meshed Raspberry. All build instructions given here can also be applied to a Raspberry Pi zero, only the Banana Pi Zero disk image will not work on a Raspberry Pi.

**Q:** Why Reticulum?<br>
**A:**<br>
Other than mesh networking projects like e.g. meshtastic, the reticulum stack is not restricted to a LoRa network, but can also be used over other rf based networks like cb radio as well as internet protocols like TCP/IP or I2P. This enables users to bridge LoRa networks into the internet and thus giving the ability to connect separated rf based networks or extend connectivity via rf.<br>

**Q:** What can I do with it?<br>
**A:**<br>
The principle of Meshed Banana is to connect to other LoRa nodes in range and to a local Wifi network. It then runs a reticulum mesh node which is accessible from Wifi and LoRa and forwards reticulum packages from one network to the other. This gives some possible use cases:<br>

- Run sensors in a LoRa network, and access the data via your WiFi network on e.g. a mobile phone that runs a reticulum enabled app
- Put a Meshed Banana in your and your neighbors home and enjoy your fully private encrypted mesh network
- Connect a cb radio via an TNC to two Meshed Bananas and connect two isolated sites over large distances<br>

**Q:** Why don't you just connect a ESP32 Lora device to your Laptop?<br>
**A:** That would be too easy ;)<br>
The main reason for this project was to create a an easy way to build a bunch of LoRa devices to play with the mesh functionality, which needs more than 2 devices at least.<br>
