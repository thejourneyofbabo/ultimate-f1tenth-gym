# F1Tenth Simulation Workspace

This ROS2 workspace contains F1Tenth racing simulation and teleoperation tools for easy car control via terminal.

## Clone Repository

To clone this repository with its submodules:

```bash
git clone --recurse-submodules <repository-url>
```

Or if you already cloned the repository without submodules:

```bash
git submodule update --init --recursive
```

## Packages

### f1tenth_gym_ros
F1Tenth racing simulator with ROS2 bridge. Launch files have been fixed to use relative map paths for easier deployment.

### Teleop Tools
Multiple teleoperation options for controlling the simulated race car:

- **key_teleop**: Control car using keyboard keys (requires `pip install pynput`)
- **joy_teleop**: Control car using joystick/gamepad
- **mouse_teleop**: Control car using mouse input

## Quick Start

1. Source the workspace:
   ```bash
   source ./install/setup.zsh
   ```

2. Launch the F1Tenth simulator:
   ```bash
   ros2 launch f1tenth_gym_ros gym_bridge_launch.py
   ```

3. Control the car (in a new terminal):
   ```bash
   # Keyboard control
   ros2 run key_teleop key_teleop
   
   # Or joystick control
   ros2 run joy_teleop joy_teleop
   
   # Or mouse control
   ros2 run mouse_teleop mouse_teleop
   ```

## Dependencies
- pynput (for key_teleop): `pip install pynput`
