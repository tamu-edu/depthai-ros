# Depthai ROS Repository
Hi and welcome to the main depthai-ros respository! Here you can find ROS related code for OAK cameras from Luxonis. Don't have one? You can get them [here!](https://shop.luxonis.com/)

You can find the newest documentation [here](https://docs.luxonis.com/software/ros/depthai-ros/)

# Syncing changes from upstream
```bash
cd depthai-ros
git checkout humble
git remote add upstream https://github.com/luxonis/depthai-ros.git
git fetch upstream
git merge upstream/humble
git push origin humble
```
