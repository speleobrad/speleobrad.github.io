---
layout: single
title:  "Architecture and design principles of Mutljomer"
date:   2023-03-20 15:44:00 +0100
categories:
  - mutljomer
  - tinkering
tags: 
  - idea
header: 
  teaser: /assets/images/architecture/teaser.jpg 
---
Network of probes sounds like a (by now) classical IoT problem. Is it the case? 

# Architecture

Mutljomer, as a system is designed in a classical client-server architecture: 

Central server is used for collecting, storing and visualizing data, and is less of a concern to build and maintain. However, as we'll see, it will have multiple communication entry points, as not all data will be able to nativelly come in "TCP/IP" form to central place.

Clients (probes) themselves are more interesting as they will be distributed in the field, measuring all the good stuff we need to know. Since no network works inside water, it's clear that probes will have 2 parts: 
- Water sensor - in-water sensor that measures properties of the water. Should be placed only where fellow cave divers can reach it, to prevent the theft or intentional damage. Clearly, should be waterproof and be able to survive spingtime rush of water.  
- Communication box - box outside of water that uses some method of communicating to "backend". Should blend into the surroundings and be as sturdy as possible to withstand elements as well as be our of reach from possible vandalism.

These two would be connected by wire(s) that again have to be hidden and protected. 

# Design principles 

I know myself, I can easlily get carried away in all fancy (and expensive) options, so I decided to write down simple design principles that will eventually put me back on the right track. List will grow over time... 

(2023-03-21)
- Components should be cheap and easily accesible. Aliexpress is a great source. 
- MCU platform of choice is Atmel and sensor bus of choice is I<sup>2</sup>C, unless there are cheaper alternatives on a BOM level.
- Measurement accuracy can be sacrificed for simplicity and price, as long as it's "good enough" to show trends of data.
- In general, we're not interested in absolute and calibrated values of individual readings but at the trends. 
- Each part should be cheap enough to be considered "disposable", especially if it gets vandalized, stolen or destroyed by the elements. 
