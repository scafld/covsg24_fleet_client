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

# Usage examples
## Robot: Jackal
Running Clearpath Jackal in Delta 3rd floor. 

### Jackal Simulaion
```bash
roslaunch covsg24_fleet_client jackal_sim.launch
```