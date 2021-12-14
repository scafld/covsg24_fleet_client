Free Fleet client configuration package for various real and simulated robots used within the project

# Installation

First install this repository:
```bash
cd <your_catkin_ws>/src
git clone --recursive https://github.com/project-covsg24/covsg24_fleet_client
```

## Set up Free Fleet:

### Ubuntu 18.04
```bash
sudo apt update && sudo apt install \
  git wget \
  python-rosdep \
  python-catkin-tools \
  python3-vcstool \
  python3-colcon-common-extensions \
  maven default-jdk   # CycloneDDS dependencies
```

### Ubuntu 20.04
```bash
sudo apt update && sudo apt install \
  git wget qt5-default \
  python3-rosdep \
  python3-vcstool \
  python3-colcon-common-extensions \
  maven default-jdk   #To install dependencies for message generation
```
### Setting Network Interface

The network interface used for by free_fleet for communication can be set in cyclonedds.xml.
You should export the path to the cyclonedds.xml in your termianl before running fleet client and server. The command below can be used for this purpose.

```bash
export CYCLONEDDS_URI=file://$PWD/cyclonedds.xml
```

# Usage examples
## Robot: Jackal
Running Clearpath Jackal in Delta 3rd floor. 

### Jackal Simulaion
```bash
roslaunch covsg24_fleet_client jackal_sim.launch
```