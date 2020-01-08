# raspberry-pi-4b-fan
Code for systemd service that controls fan.

# Hardware requirements
- Fan
- NPN Transistor
- 1kΩ Resistor
- Some cable
- Soldering equipment

# Setup
1. Connect power (5V; PIN 4) directly to fan.
2. Connect ground to transitor base (0V; PIN 6).
3. Connect GPIO21 (PIN 40) to collector.
4. Connect emitter to fan's ground.
5. Solder as required.

# Installation
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
