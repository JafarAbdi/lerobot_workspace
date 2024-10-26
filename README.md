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
