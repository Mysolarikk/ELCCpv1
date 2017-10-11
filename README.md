**OPEN standard for the Tx Message Space for IoT/blockchain interaction** 

This is to define the ELCC text space standard for ElectriCChain/ blockchain IoT standard that is **portable across blockchains**. For more information please see ElectriCChain.org project no.3 or some of the work we are doing at chainofthings/solcrypto.

We want to certify components into the blockchain TX message space. This means that if the component is in operation and confirmed in the field by a human, it can be added also by a human input. Otherwise this standard is designed to be working on IoT/Inverters, data-loggers as a python script that requests human input interactions at setup.

Additionally, if we just want to certify the existance of a solar industry product, we can do that as well. 
Also, if we want to link a certain GPS anchored system into the SolarCoin blockchain, we can do that too. We can see where it is and it links to off chain web layer web links. For privacy, if you want to certifiy your solar system you can limit the GPS decimal length to three characters.

API's can be written to specifically search and scrape this Tx data. For example with Node-red calling JSON requests.

This is also designed to work with the SolarCoin granting Engine. This will need to link with the existance of the module and components in the SolarCoin blockchain. And then it can assign a unique GUID, use the SolarCoin blockchain (or **any other blockchain** as a immutable ledger for other programs to search this ledger and grant rewards, or mine information about weather, climates, power generation etc.)

**Specifics**

These files are curently in Python 2.7 and should work natively on Raspberry Pi 2/3 with Raspian-lite/ ROKOS.
ROKOS is a Jessie 8 variant for Linux specifically running and designed for IoT/ RPI3b etc.

ElectriCChain certification syntax for SLR Blockchain Tx messaging field which is limited to 516 characters.

Example in SLR chain: https://chainz.cryptoid.info/slr/tx.dws?b9ceac11c9e2c1998f95897bea3f5545d019ed1727ac9cf46a31d8a7843eb32e.htm

There are two types of in-chain datalogs. The sysv1 instance and and ongoing instance (genv1).

**"""Example: sysv1{"UID":"7859bc519a67977e06d5e9d58860ab0546f65a29","tilt":"40", "azimuth":"180", "module":"Solarworld Sunmodule Plus SW 265 mono black SW-01-6023US","inverter":"Enphase M250 Microinverter 800-00181-r06","data-logger":"","pyranometer":"","windsensor":"","rainsensor":"","waterflow":"","Web_layer_API":"","Size_kW":"3.975","lat":"51.678N","long":"0.301E","Comment":"Hello World- I am the first Raspberry Pi Node"}"""**

The genv1 instance is for ongoing generation.
**"""Example: genv1{"UID":"7859bc519a67977e06d5e9d58860ab0546f65a29","t0":"2017-09-24 16:13:57","MWh0":11.358824,"t1":"2017-09-24 16:50:12","MWh1":11.358953,"t2":"2017-09-24 17:26:26","MWh2":11.358986,"t3":"2017-09-25 06:43:19","MWh3":11.359,"t4":"2017-09-25 07:19:33","MWh4":11.359062,"t5":"2017-09-25 07:55:46","MWh5":11.359141,"t6":"2017-09-25 08:31:59","MWh6":11.359224,"t7":"2017-09-25 09:08:13","MWh7":11.359468,"t8":"2017-09-25 09:44:26","MWh8":11.359678,"t9":"2017-09-25 10:20:41","MWh9":11.360017}"""**

**List of additions**
Updated 2017/10/10- Megred pull request for removing tracking, explained the azimuth conditions in a comment. Added @dommsko as a contributer, reviewer.

Updated 2017/09/28- Added tilt angle, azimuth and tracking (fixed, single or dual axis) so then on-chain solar due-diligence providers can scrape the SolarCoin blockchain with their bots and perform their own analysis on the solar install, and then estimate the solar energy production for that install to within 7-10% uncertainty using their own methods and a GUM method Type B based uncertainty budget similar to a PVSYST standard. Because the information is all open soruce, some specialist firms can perform this task and then get rewarded with SolarCoin for their efforts to increase the accuracy of the ecosystem.

Updated 2017/09/26- Megred pull request for split generation and datalogs for sysv1 anf genv1 instances. See examples above.

Updated 2017/09/11- 12- Removed the water flow sensor, changed the time format from XX-XX-XX to XX:XX:XX for hours:minutes:seconds. Added some general comments to make things clearer. Reduced the Comment space to a maximum of 40 characters. Usually in the comment space you can comment on what IOT you are running the .py script on.

Updated 2017/07/24- We had to allow a space for a solarcoin affiliate website's user ID, the user ID is currently open and it can be used up to 40 characters.

Updated 2017/04/21- Added elliptical curve cryptography standard for device identity based on the Chain of things protocol to the Tx Message Space. More information (here):-[https://www.chainofthings.com/]. Currently this option isn't working because it is commented out. The ECHDE public fingerprint is too long. We are looking for a way around this.

Updated 2017/04/20- Open comments reduced to 40 characters (one-quarter twitter). Updated example for SLR chain.

Updated 2017/04/20- Supports JSON. Please limit your Open comment to about 80 characters (half twitter).
