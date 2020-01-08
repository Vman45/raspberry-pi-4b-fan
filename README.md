# raspberry-pi-4b-fan
Code for systemd service that controls fan.

# Hardware requirements
- Fan
- NPN Transistor
- 1kΩ Resistor
- Some cable
- Soldering equipment

# Hardware setup
1. Connect power (5V; PIN 4) directly to fan's power (5V).
2. Connect ground (0V; PIN 6) to collector.
3. Connect GPIO21 to transitor base (PIN 40).
4. Connect emitter to fan's ground.
5. Solder as required.

# Installation
Install dependencies:
```
sudo apt-get install python3-gpiozero
```
Clone the repo:
```
git clone https://github.com/seandlg/raspberry-pi-4b-fan
mkdir -p /home/pi/Scripts && mv raspberry-pi-4b-fan /home/pi/Scripts
```
Copy and enable the service:
```
sudo cp /home/pi/Scripts/fan.service /etc/systemd/system/fan.service
sudo systemctl enable fan.service
```
