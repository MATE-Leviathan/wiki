## **Current Progress Towards ROS2**

## Development Enviorment
- Currently pretty well set up for local development
- Docker container + setup for ROS2
- Able to build code within container
- ~~Waiting on Jetson Orin Nano DevKit for hardware testing and install~~
- DevKit has arrived, set up and working following [Jetson Setup](../tools/jetson_setup.md)

## Camera integration
- Done, `fish_cam` package
- Inital benchmarks show about 15fps, could be fast enough but might not be

## Sonar integration
- Done, `ping2_sonar` package

## Motor Control
- Still work in progress
- Have testing setup but have yet to have succesfull control of motors, potential bad motor
- Need to follow troubleshooting steps [here](https://bluerobotics.com/learn/thruster-usage-guide/#troubleshooting) to see if it is a hardware issue or not
- Also looking at PWM breakout board to hopefully not have to run PWM through another board

## Controller Integration
- Everett is on this one, going to use `joy` package for ROS2

## Simulation
- Still looking around for a good simulation package underwater and for ROS2

