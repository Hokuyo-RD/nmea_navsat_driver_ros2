# nmea_navsat_driver
ROS driver to parse NMEA strings and publish standard ROS NavSat message types. Does not require the GPSD daemon to be running.

## API
This package has no released Code API.

The ROS API documentation and other information can be found at http://ros.org/wiki/nmea_navsat_driver

## BUILD
nmea_navsat_driverをビルドする
```
cd ~/colcon_ws/src
git clone https://github.com/ros-drivers/nmea_navsat_driver.git -b ros2
cd ~/colcon_ws
rosdep update && rosdep install --from-paths src --ignore-src -y
colcon build --packages-select nmea_navsat_driver
```
依存モジュールをインストールする
```
pip install src/nmea_navsat_driver/
pip install transforms3d
pip uninstall numpy
pip install "numpy<1.24"
sudo apt-get install ros-humble-tf-transformations
```
