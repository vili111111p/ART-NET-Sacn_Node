---
title: "ART-NET-sACN_NODE"
github: "https://github.com/vili111111p/ART-NET-Sacn_Node/"
description: "This is an ART-NET, sACN node with a couple of my features!"
created_at: "2026-10-5"
total_time: "1h"
---

## Oct 5, 2026: Plans

So i want to make a sturdy Art-Net and sACN node with 4 universe. I want it to have an etherCON for data input, maybe two, one for control and one for the lights with POE for power. I want it to have powerCON or truCON in and out, not sure which yet. I want it to have a battery for power failure. And for control interface i want a display with a pushable rotary encoder and also a web interface.

The plan (something that looks like this (i hope)):

<img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/89ec921d-2b7a-4f64-bf24-cc041b52a621" />



## Oct 5, 2026 (2. entry): Research and Parts

# MCU
For the MCU i choose an STM32F407 for its power and UART pins for the dmx outputs. I will see if it will work.
<img width="475" height="421" alt="image" src="https://github.com/user-attachments/assets/07a81fba-383c-44fd-adc1-4c89fd8bc1ef" />

# Networking
It will have to ways one for Art-NEt and one for control. On the Artnet side i want to use a LAN8720 PHY with the MCU's MAC. and for the control a W5500. I didnt decide on which i want the POE, because i have it on both it will be more expensive.

#230V Power
It needs a 230V AC to 5V DC converter from the powerCON or truCON to the other electronics. It will be a bit dangerous to handle it, but i have to make it safe. I think i will use an IRM-20-5.

powerCON connector

<img width="638" height="480" alt="image" src="https://github.com/user-attachments/assets/f781bfdd-ef27-4457-b519-43e8163849f2" />

# POE
For POE i think i will use a complete modul, to make things less comlicate and expensive. Maybe two for both connectors. The modul will be an Silvertel AG5300.

<img width="738" height="396" alt="image" src="https://github.com/user-attachments/assets/336e8a03-ec2c-4e0b-bf5e-a9c68d2290a3" />

# Battery
For the battery i will use one cell 5AH ex phone battery. It needs a TP4056 charger and a boost converter.

# Power multiplexer
I will need one if power failure happens to switch seamlessly. I think a TI TPS2121 would be good.

# DMX
For the 4 uni i want to use a TI SN65HVD75DR with 20 Mbit/s which is much more than i need, so thats good and uses 3.3v. I also need a dedicated digital isolator and isolated supply.

# User Interface
I want to use a simple OLED I2C display and rotary encoder.

<img width="554" height="554" alt="image" src="https://github.com/user-attachments/assets/f2361bdd-107f-4adb-823d-195bb59295c8" />
<img width="564" height="595" alt="image" src="https://github.com/user-attachments/assets/4cd921b1-b420-4776-a928-9316ddd76ec9" />

**Total time spent: 5h**
