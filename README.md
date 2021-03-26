## Home assistant docker compose for raspberry 4

### Getting Started
Add this repo to portnainer or start with docker-compose  
You need to create a /docker directory where all the volumes  
will be mounted  
  

#### Volume binding
/docker/volumes/home-assistant  
/docker/volumes/mosquitto  
/docker/volumes/zigbee2mqtt  
/docker/volumes/postgres  
  

#### Home Assistant
The configuration directory (usually .home-assistant) will be mounted to  
/docker/volumes/home-assistant/config  
  

#### Mosquitto
You can place the mosquitto.conf inside the root of mosquitto volume  
/docker/volumes/mosquitto/mosquitto.conf  
  

#### Zigbee2Mqtt
The data directory along with the configuration.yaml will be mounted to  
/docker/volumes/zigbee2mqtt/data
  

#### Postgres
Can be used as a recorder in home-assistant  
For Segmentation fault fix (for latest postgres images 13.2+):  
```
wget http://ftp.us.debian.org/debian/pool/main/libs/libseccomp/libseccomp2_2.5.1-1_armhf.deb
sudo dpkg -i libseccomp2_2.5.1-1_armhf.deb 
```
https://github.com/docker-library/redis/issues/269#issuecomment-778588162  
  

Portnainer Config:  
Repository URL: https://github.com/georgesofianosgr/hass-compose.git  
Repository reference: refs/heads/main  
Compose path: docker-compose.yml  
