# vr_helmet_driver
This is the ros driver package for Samsung vr helmet, including image retrieving and imu message reading.

# Dependency
1. libuvc <br>
We modify the original [libuvc](https://github.com/ktossell/libuvc) and put it in the thirdparty directory. 

2. libhidapi;<br>
```bash
sudo apt-get install libhidapi-dev
```
# How to run

1. Enable access to USB devices <br>
Modify the file Samsung-helmet-usb.rules (typically set GROUP to your USER NAME) and copy it to /etc/udev/rules.d. Reload udev rules,
```bash
sudo udevadm control --reload
```
2. Build the package in a catkin workspace and run
```bash
rosrun vr_helmet_driver vr_helmet_driver_node
```
