# Depthai ROS Repository
Hi and welcome to the main depthai-ros respository! Here you can find ROS related code for OAK cameras from Luxonis. Don't have one? You can get them [here!](https://shop.luxonis.com/)

You can find the newest documentation [here](https://docs.luxonis.com/software/ros/depthai-ros/)

# Syncing changes from upstream
Ensure all checks are passed in the upstream repo before proceeding.
```bash
cd depthai-ros
git checkout humble
git remote add upstream https://github.com/luxonis/depthai-ros.git
git fetch upstream
git merge upstream/humble
git push origin humble
```
# PoE camera - no router setup
Use this command in the scenario that you have a unmanaged switch -> camera, laptop. This will temporarily assign a network interface to the ethernet port of your laptop. It assigns an IP address of `169.254.1.100` and accepts all devices with address of `169.254.x.x`, which works because the camera is automatically assigned an IP of `169.254.1.222` if nothing is assingned by a router. It will not persist across reboots.
```bash
sudo ip addr add 169.254.1.100/16 dev eno0
ping 169.254.1.222
```
# View camera outside of Docker
```bash
python3 -m depthai_viewer
```
