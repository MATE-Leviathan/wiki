# Setting up HoloOcean

## Downloads

1. Clone the [holoocean-ros](https://github.com/byu-holoocean/holoocean-ros) repo into the same directory as 24-25WaterCode.
2. Clone the [HoloOcean](https://github.com/byu-holoocean/HoloOcean) repo in the same directory.
3. Download the world(s) and place them in `~/.local/share/holoocean/2.1.0/worlds/`
4. Download docker
4. Download docker-compose: `sudo apt install docker-compose-v2`

## Install

1. Go to 24-25WaterCode/docker
2. Do you have and Nvidia GPU?
    - On Nvidia: Run `docker compose --profile holoocean up -d --build`
    - On non-Nvidia: Run `docker compose --profile holoocean-no-nvidia up -d --build`

## Run Container

1. Run `docker exec -it holoocean-ros bash`

**Note**: `colcon build` takes a minute to run, so you may need to run `source ros2_ws/install/setup.bash`

## Run HoloOcean

Run `ros2 launch holoocean_main holoocean_launch.py`

**Note**: When removing the containers, you still need to pass `--profile <profile>`, otherwise the holoocean container will not be removed.
