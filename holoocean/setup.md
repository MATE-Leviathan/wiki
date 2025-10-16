# Setting up HoloOcean

## Downloads

1. Clone the [holoocean-ros](https://github.com/byu-holoocean/holoocean-ros) repo.
2. Clone the [HoloOcean](https://github.com/byu-holoocean/HoloOcean) repo.
3. Download the world(s) and place them in `~/.local/share/holoocean/2.1.0/worlds/`
4. Download docker
4. Download docker-compose: `sudo apt install docker-compose-v2`

## Install

1. Go to `holoocean-ros/docker/dev/`
    - Open `docker-compose.yaml` and replace <PATH TO HOLOOCAN> with $HOME (or wherever you cloned the HoloOcean repo)
    - Run `docker compose up -d --build`

## Run Container

1. Run `docker exec -it holoocean-ros bash`
2. Run `source ros2_ws/install/setup.bash`

## Run HoloOcean

Run `ros2 launch holoocean_main holoocean_launch.py`
