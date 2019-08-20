# LiFi Workshop Steps

# Circuit Connections:

Receiver Arduino Wiring:
  •	Connect the pin on the receiver with the S to Pin 0 (Rx) on the Arduino as in the diagram.
  •	Connect the pin on the receiver with the – to a GND on the Arduino as in the diagram.
  •	Connect the middle pin on the receiver to 5V on the Arduino as in the diagram.
  
Sender Arduino Wiring:
  •	First start by placing the IR Led on the breadboard.
  •	Connect the negative leg of the led (shorter leg) to the GND rail.
  •	Next connect the NPN Transistor’s Collector Leg on the positive leg of the LED.
  •	From the base pin of the NPN transitor, connect a 1kΩ resistor and the other leg of the resistor to Pin 1 (Tx) on the sender Arduino.
  •	Also, from the Collector leg on the NPN Transistor, Connect a 100Ω resistor in between the LED positive leg and the Transistor’s legs. Connect the other end of the resistor to Pin 9 on the Arduino.
  •	Finally, Connect the Emitter’s Leg to the GND rail through a jumper wire, and connect the rail to a GND Pin on the Arduino.
  
# Coding

Coding the Sender:
  •	Begin by defining the “cr” pin used for modulation.
  •	Next, Open the Serial Port at a Baud Rate of 1200.
  •	Modulate the signal at 38kHz.
  •	In the loop, Define the message that we’ll be receiving as a string.
  •	Read the serial port and save the message in the variable “incomingByte”
  •	Add a conditional statement to keep checking and print only valid results.
  •	In the Serial Monitor, change the Baud Rate to 1200 before sending.
  •	Type the message on the Serial Monitor and hit enter.

Coding the Receiver
  •	Begin by defining the Serial port at a Baud Rate of 1200.
  •	In the loop, define a conditional statement to check if the serial connection is available.
  •	Before receiving, in the Serial Monitor, change the Baud Rate to 1200.
  •	If there is a message, “Serial.print(char(Serial.read()))” will display what is being received.
