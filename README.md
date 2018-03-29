Beaglebone Black GPIO C++ Library
=================================

Build Library:
-------------

```bash
cd
mkdir catkin_ws #if a workspace does not already exist
cd catkin_ws
git clone https://github.com/rosmod/lib-bbbgpio.git src/lib-bbbgpio
catkin build bbbgpio
```

Update Library:
-----------------

```bash
cd ~/catkin_ws
catkin clean bbbgpio
cd src/lib-bbbgpio
git pull
cd ..
catkin build bbbgpio
```


Rosmod Source Library Setup:
-------------------------------

1. In this github repo navigate to [releases](https://github.com/rosmod/lib-bbbgpio/releases), right click on `bbbgpio.zip` (not the source code zip!) and select `Copy link address'
2. In a rosmod project, drag in a new source library to the software model
3. Paste the link in the url attribute
4. Name the source library `bbbgpio`
5. Drag the library into the `set editor` of any component that uses it
6. In the forwards section of the component add `#include "bbbgpio/gpio.h`
