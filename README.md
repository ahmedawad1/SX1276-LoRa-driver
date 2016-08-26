# SX1276-LoRa-driver

This is a driver code implementation for the SEMTECH SX1276 LoRa/FSK modules for long range communications.
<br>
This code is based on Libelium implementation for the previuos version SX1272 LoRa modules, The configuration registers were re-defined for SX1276

The Libelium liberary is the easiest implementation to show and understand how LoRa works besides FSK as well. 
<br>
Test of the code was done using inAir9B LoRa from Modtronix. 

inAir9B advantages over Libelium LoRa modules:
- Cheaper 15 $ per module 
- SX1276 has higher receiver sensitivity 
- SX1276 higher output power through the PA_BOOST connection and not RFO pin like in the Libelium modules.


<b>Using the Liberary</b>

1- On Raspberry Pi 3, create a directory, navigate to this directory using the shell and execute this command:


<code>wget http://www.cooking-hacks.com/media/cooking/images/documentation/raspberry_arduino_shield/raspberrypi2.zip && unzip raspberrypi2.zip && cd cooking/arduPi && chmod +x install_arduPi && ./install_arduPi && rm install_arduPi && cd ../..</code>

This will download the liberaries required for Libelium modules but we will make some changes to make it compatible with inAir9B from Modtronix.

2- after download is finished, execute also 

<code>wget http://www.cooking-hacks.com/media/cooking/images/documentation/tutorial_SX1272/arduPi-api_LoRa_v1_4.zip && unzip -u arduPi-api_LoRa_v1_4.zip && cd cooking/examples/LoRa && chmod +x cook.sh && cd ../../..  </code> 

3- after you have downloaded eveything, you are ready to use the modified library, navigate to /cooking/examples/LoRa 

and replace the exisiting "SX_01a_TX_LoRa.cpp" with the modified file from this repository found on
<url>https://github.com/ahmedawad1/SX1276-LoRa-driver/blob/master/SX1276_LoRa_TX/SX_01a_TX_LoRa.cpp</url>

4- do the same for the liberaries, navigate to /cooking/liberaries/arduPiLoRa and replace all 2 exisiting files by the modified liberaries "arduPiLoRa.h" and "arduPiLoRa.cpp" found on
<url>https://github.com/ahmedawad1/SX1276-LoRa-driver/tree/master/SX1276_LoRa_TX</url>

5- navigate back to /cooking/examples/LoRa and execute the following 2 commands 
<code>sudo ./cook.sh SX_01a_TX_LoRa.cpp</code>
and to run it use:
<code>sudo ./SX_01b_RX_LoRa.cpp_exe</code>

