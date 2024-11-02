# LeRobot Workspace

## Usage

### Generate udev rules

```bash
# Only plug leader board
./generate_udev_rule.bash /dev/ttyACM0 LeRobotLeader | sudo tee /etc/udev/rules.d/99-usb-serial-lerobot-leader.rules
# Only plug follower board
./generate_udev_rule.bash /dev/ttyACM0 LeRobotFollower | sudo tee /etc/udev/rules.d/99-usb-serial-lerobot-follower.rules
sudo udevadm control --reload-rules
sudo udevadm trigger
```

### Configure the motors

```bash
pixi run config-leader X # Replace X with 1,2,3,4,5,6
pixi run config-follower X # Replace X with 1,2,3,4,5,6
```

### Calibrate the follower robot


```bash
pixi run calibrate-follower
```
