# installROS2
Scripts modified to install ROS2 (foxy) on the VOXL2 Development Kits

In order to install ROS2 on voxl2:

## Upgrade cmake
First, upgrade the cmake :

```
./upgrade_cmake.sh
```
## Install ROS2
Then run,
<blockquote>$ ./install_ROS2_voxl2.sh</blockquote>

The script roughly follows the 'Install ROS From Source' procedures from:

<blockquote>https://index.ros.org/doc/ros2/Installation/Foxy/Linux-Development-Setup/</blockquote>

Much of the code is taken from the dusty-nv Github repository jetson-containers. The dusty-nv jetson-containers should be used to create a Docker container for the ROS2 on the Jetson. For more information:

<blockquote>
Dockerfile.ros.foxy
https://github.com/dusty-nv/jetson-containers
</blockquote> 

## Install DDS

To install dds, simply run :
```
./install_dds.sh
```

<h3>Notes</h3>
Currently the NVIDIA Jetsons run Ubuntu 18.04. ROS2 foxy requires Ubuntu 20.04. However, by providing some of the 20.04 equivalents, it is possible to run ROS2 foxy on the Jetsons. This script provides workarounds. Note that this is not exhaustive, you may run into situations where there are gaps, and certain packages may have issues.

<br><p>The file ~/.bashrc is modified using this script; You will want to make sure that the modifications match your expectations. For example, you may have a preference for having the install/setup.bash in another place (i.e. /root/.bashrc).
 

<h3>Release Notes</h3>

<b>January, 2021</b>
* Tested on JetPack 4.5, L4T 32.5
* Tested on Jetson Xavier NX

<b>August, 2023</b>
* Tested on VOXL2 