# SX1276-LoRa-driver

This is a driver code implementation for the SEMTECH SX1276 LoRa/FSK modules for long range communications.
<br>
This code is based on Libelium implementation for the previuos version SX1272 LoRa modules, The configuration registers were re-defined for SX1276
<br>
Test of the code was done using inAir9B LoRa from Modtronix. 

inAir9B advantages:
- Cheaper 15 $ per module 
- SX1276 has higher receiver sensitivity 
- SX1276 higher output power through the PA_BOOST connection and not RFO pin like in the Libelium modules.
