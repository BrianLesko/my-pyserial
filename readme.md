# USB and Serial

USB is used everywhere to charge and transmit data, but what is it?

Serial means sending a series of data, one piece at a time. 

&nbsp;

<div align="center"><img src="docs/preview.gif" width="800" alt="Serial Signal used to control the brightness of an LED"></div>

&nbsp;

## Examples 
- PCIe, the common interface for computers to talk at high speeds with graphics cards, wifi chips, and storage devices
- Ethernet
- CAN bus
- HDMI
- UART 

Even Wifi and Bluetooth packets are read serially.

Used for long and short range. Ethernet and its predecessor coaxial cable both send data in series. 

## Benefits
Serial links need only a pair of wires. Can run at faster clock speeds. 

## Disadvantages

Serial has more software overhead with serialization and deserialization, but makes up for this overhead by being simple enough to run at a very high clock speed.

The alternative is running numerous wires to deliver data simultaneously, which can be advantageous in some scenarios. 

## Parameters

All cables and devices that transmit or send data in series are not equal. The voltage levels can differ. But also the information density, called the baud rate among others. 

Overall, the common parameters of a serial communication device include

Baud rate - bits per second
Start bit - signals the start of a new data frame
Data bits - often one byte or 8 bits
Parity Bits - help check data integrity
Stop Bit - signals the end of the data frame.

For each different type of communication, these concepts are generally used. 

## Simple implementation

In simpler serial architectures, like RS232 or UART, there is normally a set of only two wires for transferring data, often denoted Rx and Tx or Receive and Transmit. In addition there is a common ground, and sometimes a fourth wire to carry power. Each of the transmission wires are either high or low voltage.

## Increasing reliability

USB-A uses two wires to transmit. Setting the same signal on both lines with one inverted to reduce noise. USB-A uses the same two wires to receive. So, it can only send data in one direction at a time

## Modern Implementations 

USB C has at least one pair for transmission and another for receiving. USB C adds even more wires to enable video and audio transmission.

The most advanced cables can communicate 20 GB/s in each direction simultaneously 

## Compatibility

Computers come equipped with the ability to detect different types of devices and cables at the hardware level. Libraries like PySerial let users take advantage of this and connect to even the oldest devices  - like RS232 from a brand new computer! RS232 was invented in 1960. Thats modern technology and legacy interacting at a gap of 64 years (2024). Without a library like PySerial. A massive amount of knowledge on how the specific cable works would be required to write your own communication protocol. That would include knowing voltage levels, number of wires, how many are for communication, are they single or bidirectional? What is the tolerance for noise? What is the information density, the baud rate? how long is the message what is the stop and start bit or byte? How many parity bits or bytes? Is there a checksum? What is the checksum? how is it calculated. How do we translate English to bytes and bits. What if any adapter is needed to actually plug the device in. The list could go on. 

## Software Dependencies

This code uses the following libraries:
- `pyserial`: The Python Library studied
- `Streamlit`: for creating a user interface

&nbsp;

## Hardware Dependencies
1. A computer
2. Some adapters or devices to test communication with

## Usage
```
git clone ...
python3 -m venv my_env
source my_env/bin/activate
pip install pyserial streamlit
streamlit run app.py
```

This will start the local Streamlit server, and you can access the interface by opening a web browser and navigating to `http://localhost:8501`.

&nbsp;

## Topics 
```
Python | Low Code UI | Mobile robot | Internet IP 
HIDapi | decode bytes | PS5 | Sony | Dualsense | external device | communication 
Mechanical and Robotics engineer
```
&nbsp;

<hr>

&nbsp;

<div align="center">



╭━━╮╭━━━┳━━┳━━━┳━╮╱╭╮        ╭╮╱╱╭━━━┳━━━┳╮╭━┳━━━╮
┃╭╮┃┃╭━╮┣┫┣┫╭━╮┃┃╰╮┃┃        ┃┃╱╱┃╭━━┫╭━╮┃┃┃╭┫╭━╮┃
┃╰╯╰┫╰━╯┃┃┃┃┃╱┃┃╭╮╰╯┃        ┃┃╱╱┃╰━━┫╰━━┫╰╯╯┃┃╱┃┃
┃╭━╮┃╭╮╭╯┃┃┃╰━╯┃┃╰╮┃┃        ┃┃╱╭┫╭━━┻━━╮┃╭╮┃┃┃╱┃┃
┃╰━╯┃┃┃╰┳┫┣┫╭━╮┃┃╱┃┃┃        ┃╰━╯┃╰━━┫╰━╯┃┃┃╰┫╰━╯┃
╰━━━┻╯╰━┻━━┻╯╱╰┻╯╱╰━╯        ╰━━━┻━━━┻━━━┻╯╰━┻━━━╯
  


&nbsp;


<a href="https://twitter.com/BrianJosephLeko"><img src="https://raw.githubusercontent.com/BrianLesko/BrianLesko/main/.socials/svg-grey/x.svg" width="30" alt="X Logo"></a> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <a href="https://github.com/BrianLesko"><img src="https://github.com/BrianLesko/BrianLesko/blob/main/.socials/svg-grey/github.svg" width="30" alt="GitHub"></a> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <a href="https://www.linkedin.com/in/brianlesko/"><img src="https://raw.githubusercontent.com/BrianLesko/BrianLesko/main/.socials/svg-grey/linkedin.svg" width="30" alt="LinkedIn"></a>

follow all of these for pizza :)

</div>


&nbsp;


