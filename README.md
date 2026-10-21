# HearIT-Sense
A smart wearable communication glove using ESP32 and 8 push buttons to help people with hearing and speech impairments communicate through predefined messages and a web interface.

HearIT Sense is an assistive technology project developed by Team Strategix at S.A. Engineering College. It aims to help people with hearing and speech impairments communicate more easily with people who do not understand sign language.

**Problem Statement**

People who use sign language often face communication barriers in schools, hospitals, workplaces and public places because many people do not understand sign language. HearIT Sense aims to reduce this gap through a simple wearable communication system.

**Proposed Solution**

HearIT Sense uses a wearable glove with eight push buttons connected to an ESP32 microcontroller. Each button cycles through five predefined messages, providing a total of 40 messages.

**When a button is pressed:**

1. The ESP32 detects the input.
2. The corresponding message is selected.
3. The message is displayed on a web interface.
4. The audio output system can provide sound feedback.

The planned speech functionality will allow the selected message to be spoken through the physical speaker and the web browser.

**Key Features**

- Wearable glove-based input system.
- Eight push buttons and 40 predefined messages.
- ESP32-based processing.
- Wi-Fi-enabled web interface.
- Real-time message display.
- MAX98357A I2S audio amplifier and external speaker.
- Planned AI-based hand gesture recognition.

**Hardware Components**

- ESP32 development board
- Eight push buttons
- MAX98357A I2S amplifier module
- Compatible external speaker
- Power supply
- Wearable glove and connecting wires

**Software and Technologies**

- Arduino IDE
- Embedded C/C++
- ESP32 Wi-Fi
- Arduino WebServer
- HTML, CSS and JavaScript
- I2S digital audio interface

**System Architecture**

Button Input → ESP32 Processing → Message Selection → Web Interface / Audio Output

**Hardware Connections**

MAX98357A to ESP32
MAX98357A Pin| ESP32 Pin
BCLK| GPIO 26
LRC / WS| GPIO 25
DIN| GPIO 22
GND| GND
VIN| Compatible power supply
Connect the speaker to the amplifier's designated speaker output terminals. Follow the module's voltage and wiring specifications.

**Push Buttons**

Button| ESP32 GPIO
Button 1| GPIO 14
Button 2| GPIO 27
Button 3| GPIO 32
Button 4| GPIO 33
Button 5| GPIO 12
Button 6| GPIO 13
Button 7| GPIO 15
Button 8| GPIO 4

The current program uses "INPUT_PULLUP", so each button should connect its GPIO pin to GND when pressed.

**Installation and Setup**

1. Install the Arduino IDE.
2. Install the ESP32 board package by Espressif Systems.
3. Open the Arduino sketch from the "src" folder.
4. Select the correct ESP32 board and serial port.
5. Connect the ESP32 to the computer using USB.
6. Upload the program.
7. Open the Serial Monitor at 115200 baud.
8. Connect to the configured Wi-Fi network and open the IP address printed by the ESP32 in a browser.
Ensure that the Wi-Fi configuration in the source code matches your setup.

**Prototype Validation**

The prototype was tested with students at The Clarke School for the Deaf. The students found the device easy to use, and the voice-output concept helped other people understand their intended messages.

**Current Development Status**

The ESP32 prototype and web interface have been developed. The existing tone-generation code produces audio tones rather than spoken words. Actual spoken output through the physical speaker and browser requires additional audio playback and text-to-speech implementation.

**Future Enhancements**

- AI-based hand gesture recognition.
- Automatic conversion of recognized gestures into speech.
- Improved wearable design and concealed wiring.
- Multilingual voice output.
- Better battery efficiency and compact hardware integration.

**Project Team**

Team Strategix — S.A. Engineering College

- Logarakshika A
- Kamalini D
- Arshiya Samreen K
- Delfie Deril

Vision

To help people with hearing and speech impairments express themselves more confidently and communicate more effectively in everyday situations.

License

This project is intended for educational and research purposes. See the LICENSE file for applicable terms.
