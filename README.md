# foxglove-onboard
Repo demonstrating Foxglove Studio for F1Tenth

## [installing foxglove](https://foxglove.dev)

## live telemetry

### prereqs: 

  - install ros bridge: 
```bash
sudo apt-get install ros-<rosdistro>-rosbridge-suite
```
  - launch:
```bash
# 1. connect to remote 
ssh -L 9090:localhost:9090 -E /dev/null nvidia@<your.ip.address>
# 2. launch
ros2 launch rosbridge_server rosbridge_websocket_launch.xml
```
  - this will create a server on port 9090. ssh should have forwarding setup already, check `localhost:9090` on local machine to verify

### visualization

  - open Foxglove and choose "ros bridge" as data source

## bagging

### run bagging

  - install mcap
  ```bash
  sudo apt install ros-$ROS_DISTRO-rosbag2-storage-mcap
  ```
  - run
  ```bash
  ros2 bag record -s mcap -a -o <save_path>
  ```

### view bag

- bags are stored on remote by default. scp is a good way to transport it to local for viewing
