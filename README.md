# Proxmox Home Assistant Operating System
Welcome to my github repository, where you can find everything regarding our Home Assistant environment and beyond. You can find details and config (examples), information and explanation in this repo.  
Want to know more about our HomeLab hardware setup: https://github.com/kippesikgithub/proxmox_hardware  
Want to know more about our Home Assistant Interface: https://github.com/kippesikgithub/ha_cards_interface  
Home Assistant installed from: https://tteck.github.io/Proxmox/  

# Home Assistant Virtual machine
#### Settings
HAOS Proxmox VM  
6-cores  
16GB RAM  
Google Coral TPU M2 passthrough (frigate)  
100GB Diskspace on 512GB nvme m2 drive  

#### Hardware Passthrough
Google Coral TPU M2 passthrough (Proxmox to HAOS)  
USB Conbee2 Zigbee Dongle (Proxmox to HAOS)  

# Home Assistant Operating System (HAOS)

### Interface
Since our Home Assistant interface is mostly custom build by me, I have a separate Github repository for explanation and examples about our cards and configurations.  
Home Assistant Interface: https://github.com/kippesikgithub/ha_cards_interface

## Addons
Detailed explanation of the used Addons in Home assistant.
#### Frigate
Frigate running as addon in HA  
Frigate uses the M2 Google Coral TPU  
Frigate Setup: https://github.com/kippesikgithub/frigate  

#### Double Take
Double Take (face recognition) running as addon in HA  
Double Take uses 'person' detected snapshots from frigate as source images  

#### Node-Red
Node-Red running as addon in HA  

#### ESPHome
EspHome running as addon in HA  
I use EspHome a lot to create controllers for products, home-build custom projects, sensors, and more!  
##### Links to projects
ESP-mmWave motion detection: https://github.com/kippesikgithub/esp_motion_mmwave  
ESP-Playhouse for the kids: https://github.com/kippesikgithub/esp_playhouse  
ESP-Wifi controller (autonomous) Car: https://github.com/kippesikgithub/esp_rc_car  
ESP-Clock: https://github.com/kippesikgithub/esp_pixelclock  
ESP-Speakers: https://github.com/kippesikgithub/esp_speaker  
ESP-Duplo Train Controller: https://github.com/kippesikgithub/esp_bt_duplo  

#### MQTT
MQTT broker running as addon in HA  

#### Zigbee2MQTT
Z2M running as addon in HA  

#### Go2RTC
Go2RTC running as addon in HA  

#### AppDaemon
AppDaemon running as addon in HA  
##### ControllerX app

#### Ring2MQTT
Ring2MQTT running as addon in HA  
Connecting Home assistant to the Ring services via mqtt. Getting the switches, sensors and videostream.  

#### Tailscale
Tailscale running as addon in HA  

#### ADB
ADB running as addon in HA  
Controlling the Android television by ADB commands.  

#### Google Drive Backup
Google Drive backup running as addon in HA  
Creating Home assistant backup every night, upload to Google Drive.  
  
## Integrations
Detailed explanation of the used Integrations in Home assistant.

#### WLED
I use WLED a lot to create custom (status) lights/lamps, or just for fun!  
##### Links to projects
WLED Garbage Truck indicator: https://github.com/kippesikgithub/wled_garbagetruck  
WLED Kids Nightlight / Sleeptrainer: https://github.com/kippesikgithub/esp_kids_nightlight  

#### EsPresense BLE Tracking
I use Espresense throughout the home for BLE tracking (using our phones + HA companion app)  
Setup EsPresense: https://github.com/kippesikgithub/espresense  

#### Shelly devices
We use a lot of Shelly devices throuout the home (30+)

#### Tesla (car) 
To receive data and monitor the car, we use the Tesla integration from HACS.  
https://github.com/alandtse/tesla

#### Buienradar
Using Buienradar integration to receive weather information.

#### Neerslag app
Using the Neerslag app from HACS to receive information about upcoming rain/snow/hail.  
https://github.com/aex351/home-assistant-neerslag-app

#### Enphase Envoy
To receive data from our Solar Envoy installation.

#### Solar Forecast
Forecasting how much solar energy there will be.

#### Homewizard
Using the HomeWiazerd P1 meter to receive data about Electricity and Gas usage

#### Frigate
https://github.com/blakeblackshear/frigate

#### Toon
Toon to receive data from the Eneco electricity/gas company.

#### Google Cast
For casting dashbaords, audio and video to multiple Google devices.

#### LG Horizon
To connect to the Ziggo Smart TV box.

#### Philips TV
Conncecting to our Philips television (android tv)

#### Mitsubishi WF-RAC
To connect to our Climate devices (Mitsubishi Heavy Industries).  
https://github.com/jeatheak/Mitsubishi-WF-RAC-Integration

#### IRobot Roomba
To connect to our Vaccuum cleaner(s).

#### NOA Aurora Sensor
Picking up space weather about aurora, to capture with camera's

#### Notifications for Android TV / Fire TV
To display doorbell stuff on Live on the TV.

#### ESP-SomfyRTS
Controlling our screens via the SomfyRTS protocol.  
https://github.com/rstrouse/ESPSomfy-RTS

#### Tasmota
Running a lot of Tasmota devices throughout the home.

#### Volumio
Controlling Volumio (audio) instances throughout the home

#### Radio Browser
For sending radio streams to the mediaplayers throughout the home.

#### PowerCalc
Calculating power usage of devices that are not measured.

#### Google Calendar
Integrate the family calendar into HA

#### Tile
BLE tracker on our Bakfiets.

#### WebRTC Camera
Displaying camera streams in dashboards gathered by Go2RTC

#### Sabnzbd
Receiving data from our Sabnzbd instance about downloads

#### Browser MOD
Using to display modded cards in our interface.  
https://github.com/thomasloven/hass-browser_mod

#### Sun, Moon
Receiving data from Sun and Moon

### Other Home Assistant related Projects
Wall Tablet in Living room: https://github.com/kippesikgithub/hass_walltablet  
Hue Remotes Glow in the dark: https://github.com/kippesikgithub/remote_wall_switch_solutions  
Monitor Washing Machine / Dryer: https://github.com/kippesikgithub/hass_washing_dryer  
Detailed Power Monitoring: https://github.com/kippesikgithub/hass_detailed_power_monitoring  

## Possible Issues / Fixes

### Free Diskspace in HAOS smaller than expected
Sometimes backups created by HAOS are not pruned automatically. Most of the times you can only see it because of the ./backup folder is very big, while in the HA interface you wont see any stored backups.  
Resolve the issue:  
- Install Terminal & SSH addon in HA
- Install SMB addon in HA
- Start the addon, and open the terminal
- first change directory to root: 'cd ..'
- than list the underlaying folders with the command: 'du -hs -d 1'
- take a look at the list of folders and sizes
- if your ./backup folder is greater than 0, and you dont see any backups in HA
![image](https://github.com/kippesikgithub/proxmox_haos/assets/100353268/43be29ea-b143-4bea-8d2b-752f909c375c)  
In the example you see the ./backup folder is over 20gb ......but .......  
![image](https://github.com/kippesikgithub/proxmox_haos/assets/100353268/e5348cd3-e868-4b06-a54d-53f09076efc1)
im HA we don't see any backups listed ......but .......
![image](https://github.com/kippesikgithub/proxmox_haos/assets/100353268/0f274f69-5830-4b7d-aee5-e89af7e8754d)  
If we open the SMB share from HA in the folder Backups we do see a left-over created backup.
- We can delete the backup via SMB, and the diskspace will be freeed to HA


