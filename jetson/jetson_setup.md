# Jetson Setup

## Inital Flash
- Follow the offical [Jetson Setup](https://developer.nvidia.com/embedded/learn/get-started-jetson-orin-nano-devkit) to flash and get the latest jetpack installed. 

## Static IP and SSH
It is very imporant to set up a static IP for the Jetson as it lets us connect to it when in the tube and redeploy code as needed. Addtionally it will let anyone on Eduroam connect to it and do development. The current process for getting a static IP is to just ask IT for it and provide the info they ask for.

The current Orin has the IP 10.50.2.100 and can be accessed with
`ssh ubuntu@10.50.2.100`. 

## Software install
- ROS2 from source (we are actually just gonna wait for jetpack 6 with a mid nov release)

