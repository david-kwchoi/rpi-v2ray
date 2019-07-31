# rpi-v2ray
A Dockerfile for building v2ray with balenalib/raspberrypi3:buster as the base image

## Getting Started
### Run in detached mode
```
docker pull b1iz4rclavid/rpi-v2ray
docker run -d -p <docker_host_port>:<config_server_inbound_port> -v <folder_with_config_json>:/home/v2ray/ -it b1iz4rclavid/rpi-v2ray
```
### Shell access to the running container
```
docker exec -it <container id> /bin/bash
``` 

## Configuration
Customization is done by updating ```config.json``` at mount it to the container
Please refer to https://www.v2ray.com/en/ for configuration details

### Prerequisites
You will need to have docker installed on your rpi. 
Please refer to https://www.raspberrypi.org/blog/docker-comes-to-raspberry-pi/

```
curl -sSL https://get.docker.com | sh
```
