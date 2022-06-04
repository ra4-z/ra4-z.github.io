Two methods are provided, where one using commands and the other via a brilliant public tool.

# 1. Commands
## 1.1 Check all your monitors
```bash
$ xrandr | grep " connected" | cut -f1 -d " "
HDMI-1
DP-2
```
See, mines are `HDMI-1` and `DP-2`.
## 1.2 Adjusting brightness by percent
```bash
# Command line
$ xrandr --output [monitor-name] --brightness [brightness-level]
# e.g. Setting brightness of DP-2 to 75%
$ xrandr --output DP-2 --brightness 0.75
```

Then, boom! Your monitor is set up!

# 2. A user-friendly tool, [Brightness](https://github.com/lordamit/Brightness) by [LordAmit](https://github.com/lordamit)

This tool can automatically detect all your monitors, and provides a GUI with scrollers as below.
![GUI](https://github.com/LordAmit/Brightness/raw/master/img/BrightnessController.gif)
```
# Installation
$ sudo add-apt-repository ppa:apandada1/brightness-controller
$ sudo apt update
$ sudo apt install brightness-controller

# launching it
brightness-controller
```
Apparently, there's more than barely sliding brightness. XD

# References
1. [linux终端调节亮度,从Ubuntu终端控制屏幕亮度](https://blog.csdn.net/weixin_35960434/article/details/116717942)
2. [lordamit-Brightness](https://github.com/lordamit/Brightness)