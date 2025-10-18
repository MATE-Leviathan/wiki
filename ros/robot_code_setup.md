## **Robot Code Setup**

### [**Install Ubuntu**](#install-ubuntu)
#### [**Windows**](#windows)
- Install [WSL2](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
- Should basically just be `wsl --install`
- Use `wsl` to open a terminal

#### [**Mac**](#mac)
- Install docker desktop from [here](https://docs.docker.com/docker-for-mac/install/)
- Build the docker container (see below at [**Set up Docker container**](#set-up-docker-container))

#### [**Native Linux**](#native)
- Just follow the steps below, you should be able to figure it out :) 

### [**Install Docker**](#install-docker)
- `sudo apt update`
- `sudo apt install docker.io`
- `sudo gpasswd -a $USER docker`
- Restart your VM (for WSL, close and reopen your terminal)

### [**Set up GitHub SSH key**](#set-up-github-ssh-key)
- `ssh-keygen -t ed25519 -C "your_email@example.com"`
    - Replace `your_email@example.com` with your actual email
    - Hit enter until you get back to a command line
- Copy the output of `cat ~/.ssh/id_ed25519.pub`
- Go to [https://github.com/settings/keys](https://github.com/settings/keys) and click "New SSH Key"
- Paste what you copied into the "Key" field
- Name the key whatever you want

### [**Clone robot code**](#clone-robot-code)
- `cd ~`
- `git clone git@github.com:MATE-Leviathan/24-25WaterCode.git`

## Set up Docker container - Using `docker-compose`

### Set up Docker container
- `cd ~/24-25WaterCode/docker`
- `docker compose up -d`
- Wait for download to finish

### How to enter Docker
- `docker start leviathan`
- `docker exec -it leviathan /bin/bash`

## Set up Docker container - Using `docker-run.sh`

### [**Set up Docker container**](#set-up-docker-container)
- `cd ~/24-25WaterCode/docker`
- `docker build -t mate2025 .`
- Wait for things to download
- `./docker-run`
- `cd 24-25WaterCode` and `ls` and you should see stuff, if not you probably didn't clone the repo into /home/ubuntu 


### [**How to enter Docker**](#how-to-enter-docker)
The general Docker reference is [here](/tools/docker.md).
- `docker ps -a`, find the name of your container
- `docker start [container name]`
- `docker exec -it [container name] /bin/bash`

### [**Build code**](#build-code)
- `natbuild`, then `rosstd`, then try ros2 and tab complete your way into some commands. See here for some things to try https://docs.ros.org/en/rolling/Tutorials/Beginner-CLI-Tools/Introducing-Turtlesim/Introducing-Turtlesim.html
