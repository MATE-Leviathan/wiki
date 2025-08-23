## **Robot Code Setup**

### [**Install Ubuntu**](#install-ubuntu)
#### [**Windows**](#windows)
- Install [WSL2](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
- Should basically just be `wsl --install`
- Use `wsl` to open a terminal

#### [**Mac**](#mac)
- Install docker desktop from [here](https://docs.docker.com/docker-for-mac/install/)
- Build the docker container (see below at [**Set up Docker container**](#set-up-docker-container))

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

### [**Set up Docker container**](#set-up-docker-container)
- `cd ~/2023WaterCode/docker`
- `docker build -t mate2023 .`
- `./docker-run`
- Wait for things to download

### [**How to enter Docker**](#how-to-enter-docker)
The general Docker reference is [here](/tools/docker.md).
- `docker ps -a`, find the name of your container
- `docker start [container name]`
- `docker exec -it [container name] /bin/bash`

### [**Build code**](#build-code)
- `natbuild`, this will take a while
