# OGC.Engineering
## ogc_project_data_link_915 - a 915 MHz serial data link
Developer contact - dustin ( at ) ogc.engineering

---
## Feature list
### Development Base
- [ ] Development Tools - Edit, Compile, Program, Debug and Communicate with a local connected device ( GDB and Terminal )
- [ ] Development Tools - Edit, Compile, Program, Debug and Communicate with a network connected device ( OpenOCD & Netcat )
- [ ] Base Hardware - description header with processor validation, main clock speed, debug resource group [ status indicator, and debug serial port ]
- [ ] Demo Baremetal Firmware - CSP, Drivers, and HAL ( blink the status indicator and echo data on the debug serial port )
- [ ] Metrics - Measure average power consumption during baremetal demo activities as a baseline for a non optimized system
### Scheduler Operation
- [ ] NRTPS Firwmare CSP, Driver, and HAL additions - add features needed to support NRTPS, Status indicator, and CLI libraries
- [ ] NRTPS Software Library additions - add libraries for NRTPS scheduler, Status indicator, CLI command handling, and Data logging
- [ ] NRTPS Software Application additions - add demo application to match functionality of Baremetal demo ( blink the status indicator and echo data on the debug serial port )
- [ ] Metrics - Measure average power consumption during scheduler demo activities as a secondary baseline for a non optimized system
### Scheduler Optimization
- [ ] NRTPS sleep during inactivity - A glaring optimization is to sleep when the scheduler detects there are no tasks to be executed in the near future, set threshold and put system to sleep
    - [ ] add ability to configure periodic timers and ability to wake from external interrupt source as needed
- [ ] Metrics - Measure average power consumption during scheduler demo activities as a optimization comparison
### Wireless Communication
- [ ] Network - Serial port for data link
- [ ] Network - switchable communications, direct FSK/OOK
- [ ] Network - switchable communications, LoRa Class A ( Listens all the time ) [ basestation needed ]
- [ ] Network - switchable communications, LoRa Class B ( Class C plus Listens at regular predetermined intervals ) [ basestation needed ]
- [ ] Network - switchable communications, LoRa Class C ( Listens only after it has brodcasted for a short amount of time ) [ basestation needed ]
### MVP 
- [ ] package up current resources into base BSP and release project on Github

---
## OGC Layered Development
---
### Project
---
### Deployment
---
### Software
#### Application(s)
#### Libraries
---
### Firmware
#### HAL
#### Drivers
#### CSP
---
### Hardware
* PLACEHOLDER for link to repository
* ST B-L072Z-LRWAN1 Discovery Kit - https://www.st.com/en/evaluation-tools/b-l072z-lrwan1.html
* Active marketing ~$50 as of 07/2023

---
# MISC Notes
* 900 MHz is susceptible to high levels of interference ( common used open band )
* LoRa can achieve about 50 Kbps max
* LoRa payload is 243 bytes per message
* FCC’s time-on-air limits (400 ms)