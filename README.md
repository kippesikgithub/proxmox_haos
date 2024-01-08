# Proxmox Home Assistant Operating System
installed from: https://tteck.github.io/Proxmox/  

# Home Assistant Virtual machine
## Settings
HAOS Proxmox VM  
6-cores  
16GB RAM  
Google Coral TPU M2 passthrough (frigate)  
100GB Diskspace on 512GB nvme m2 drive  

## Hardware Passthrough
Google Coral TPU M2 passthrough (Proxmox to HAOS)  
USB Conbee2 Zigbee Dongle (Proxmox to HAOS)  

# Home Assistant Operating System (HAOS)

## Addons
### Frigate
Frigate uses the M2 Google Coral TPU  
Frigate Setup: https://github.com/kippesikgithub/frigate  

### MQTT

### Zigbee2MQTT

### Go2RTC

## Interface
Since our Home Assistant interface is mostly custom build by me, I have a separate Github repository for explanation and examples about our cards and configurations.  
Home Assistant Interface: https://github.com/kippesikgithub/ha_cards_interface  

