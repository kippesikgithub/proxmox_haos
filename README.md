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
##### Links to projects
ESP-mmWave motion detection: https://github.com/kippesikgithub/esp_motion_mmwave  
ESP-Playhouse for the kids: https://github.com/kippesikgithub/esp_playhouse  
ESP-Wifi controller (autonomous) Car: https://github.com/kippesikgithub/esp_rc_car  
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


  

