# foxglove-onboard
Repo demonstrating Foxglove Studio for F1Tenth

## [installing foxglove](https://foxglove.dev)

### prereq: setup ros bridge

  - install: 
```bash
sudo apt-get install ros-<rosdistro>-rosbridge-suite
```
  - launch:
```bash
ros2 launch rosbridge_server rosbridge_websocket_launch.xml
```
  - this will create a server on port 9090. ssh should have forwarding setup already, check `localhost:9090` on local machine to verify

### visualization

  - choose "ros bridge" for data source
