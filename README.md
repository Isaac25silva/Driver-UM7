Drivers-um7
===========

Driver for the CH Robotics UM7 inertial measurement device without ROS.  
Supports standard data and mag topics as well as providing temperature and rpy outputs.

###Compile (linux)

To compile execute the command on directory.   

    cmake CMakeLists.txt  
    make all

###Execute

To execute:  

    ./imu

The port address of the UM7 is "*/dev/ttyUSB0*", you can change the address in the file *imu.cpp*.

Ubuntu Build Notes
------------------
**apt-get should have these**

Boost library dependencies:  

    sudo apt-get install libboost-all-dev


**If you need install serial.h**  
    To install *serial.h* execute the commands on serial folder (first remove the build folder):  

    mkdir build  
    cd build  
    cmake ..  
    make  
    sudo make install  

**Perhaps you need change the permissions** 

    chmod 777 /dev/ttyUSB*
