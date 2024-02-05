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

### Addons
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
  
### Integrations
Detailed explanation of the used Integrations in Home assistant.

#### WLED
I use WLED a lot to create custom (status) lights/lamps, or just for fun!  
##### Links to projects
WLED Garbage Truck indicator: https://github.com/kippesikgithub/wled_garbagetruck  
WLED Kids Nightlight / Sleeptrainer: https://github.com/kippesikgithub/esp_kids_nightlight  

#### EsPresense BLE Tracking
I use Espresense throughout the home for BLE tracking (using our phones + HA companion app)  
Setup EsPresense: https://github.com/kippesikgithub/espresense  

### Other Home Assistant related Projects
Wall Tablet in Living room: https://github.com/kippesikgithub/hass_walltablet  
Hue Remotes Glow in the dark: https://github.com/kippesikgithub/remote_wall_switch_solutions  
Monitor Washing Machine / Dryer: https://github.com/kippesikgithub/hass_washing_dryer  
Detailed Power Monitoring: https://github.com/kippesikgithub/hass_detailed_power_monitoring  
