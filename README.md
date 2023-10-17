#GIT
sudo apt-get update
sudo apt-get install git

git config --global user.name "USERNAME"
git config --global user.email "EMAIL"

sudo apt-get install python3-dev python3-pip

#MAVLProxy(python3)
sudo apt-get install python3-dev python3-opencv python3-wxgtk4.0 python3-pip python3-matplotlib python3-lxml python3-pygame
pip3 install PyYAML mavproxy --user
echo "export PATH=$PATH:$HOME/.local/bin" >> ~/.bashrc
pip3 install mavproxy --user --upgrade
pip3 install mavproxy --user git+https://github.com/ArduPilot/mavproxy.git@master

#DRONEKIT
sudo pip install future pymavlink MAVProxy
sudo apt install python3-future libtool autoconf
sudo apt-get update && sudo apt-get dist-upgrade -y
sudo pip install pymavlink mavproxy dronekit dronekit-sitl
sudo apt autoremove -y && sudo apt autoclean

git clone https://github.com/ArduPilot/ardupilot.git
cd ardupilot
git checkout Copter-4.4.1
git submodule update --init --recursive

sudo apt install python3-matplotlib python3-serial python3-wxgtk4.0 python3-wxtools python3-lxml python3-scipy python3-opencv ccache gawk python3-pip python3-pexpect
sudo pip install future pymavlink MAVProxy

Tools/environment_install/install-prereqs-ubuntu.sh -y
. ~/.profile

Here are some commands to configure waf for commonly used boards:

./waf configure --board bebop --static # Bebop or Bebop2
./waf configure --board edge           # emlid edge
./waf configure --board fmuv3          # 3DR Pixhawk 2 boards
./waf configure --board navio2         # emlid navio2
./waf configure --board Pixhawk1       # Pixhawk1
./waf configure --board CubeBlack      # Hex/ProfiCNC Cube Black (formerly known as Pixhawk 2.1)
./waf configure --board Pixracer       # Pixracer
./waf configure --board skyviper-v2450 # SkyRocket's SkyViper GPS drone using ChibiOS
./waf configure --board sitl           # software-in-the-loop simulator
./waf configure --board sitl --debug   # software-in-the-loop simulator with debug symbols
List of available vehicle types

Here is a list of the most common vehicle build targets:

./waf copter                            # All multirotor types
./waf heli                              # Helicopter types
./waf plane                             # Fixed wing airplanes including VTOL
./waf rover                             # Ground-based rovers and surface boats
./waf sub                               # ROV and other submarines
./waf antennatracker                    # Antenna trackers

Run Simulator
cd ~/ardupilot/ArduCopter
sim_vehicle.py -w
