# OGC.Engineering
## ogc_project_data_link_915 - a 915 MHz serial data link end node
Developer contact - dustin ( at ) ogc.engineering

---
## Description
* Planniing of a multipath wireless network reveals the need to develop a series of plug and play data link communication modules.  This data link project will develop a 915 MHz based system to communicate between nodes using direct FSK/OOK.
---
## Release Planning/Tracking
- [ ] v0.1 DEV DEMO - Development tools exists, the lights blink, and the debug port echos back at you giving proof of life, collect baseline metrics
- [ ] v0.2 DEV DEMO - The NRTPS is running and mirroring the v0.1 functionality, compare metrics
- [ ] v0.3 DEV DEMO - NRTPS optimizations needed for battery operated devices, compare metrics ( rolling development of the NRTPS into this project as the driving force for improvement )
- [ ] v0.4 APP DEMO - Application development showing logging output, status indicator and command handling of all current features ( indication, logging, commands ), compare metrics
- [ ] v0.5 APP DEMO - Radio power/configuration control ( focus on OOK and FSK direct node to node configurations and message validation needs ) with CLI commands, compare metrics
- [ ] v0.6 COMMS DEMO - Radio Communications with associated CLI commands and data buffers/handlers, echo between two devices, wake on receipt, and validation of contents, compare metrics
- [ ] v0.7 COMMS DEMO - Add button functionalities ( halt ( short press )/resume( long press ) all radio transmissions ), CLI commands and separate offline warning status indicator, compare metrics
- [ ] v0.8 UX DEMO - Passthrough operation, attach a dedicated serial buffer to radio communications and have handlers split and recombine as needed for connected device, compare metrics
- [ ] v0.9 UX DEMO - Add EEPROM persistant memory for savable configurations and associated CLI commands to get/set device configuration(s), compare metrics
- [ ] v1.0 MVP - Auto load and apply persistant configuration at boot to get a standalone, configurable communication module ( attach metrics comparison and test outputs )

---
## OGC Layered Development
---
### Project
* This repository documents the project and collects together all the needed resources for tagged deployments
```
git clone https://github.com/OGC-dustin/ogc_project_data_link_915.git
git submodule update --init
```
---
### Deployment

```
TBD
```
---
### Software
#### Application(s)

```
TBD
```
#### Libraries

```
TBD
```
---
### Firmware
#### HAL

```
TBD
```
#### Drivers

```
TBD
```
#### CSP

```
TBD
```
---
### Hardware
* ST B-L072Z-LRWAN1 Discovery Kit - https://www.st.com/en/evaluation-tools/b-l072z-lrwan1.html
* Active marketing ~$50 as of 07/2023
```
TBD
```

---
# MISC Notes
* FCC’s time-on-air limits (400 ms)
* ST1276 radio in the Murata module ( still showing as active on the market ) may be end of life as the SX1262 has been pushed to market
    * Research and update project with latest hardware before moving past v1.0 MVP features
    * Explore multi configuration of FSK and LoRa operating together for network and direct communication
    * 900 MHz is susceptible to high levels of interference ( common used open band )
    * LoRa can achieve about 50 Kbps max
    * LoRa payload is 243 bytes per message
