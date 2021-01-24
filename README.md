# Marlin 2.0.7.2 - Anet A8 (Custom)

![GitHub](https://img.shields.io/github/license/marlinfirmware/marlin.svg)
Please see the [original repository](https://github.com/MarlinFirmware/Marlin/releases) for more information about Marlin.


## Features
  - SKR 1.4 Turbo mainboard
  - BTT TFT35
  - E3D V6 Hotend
  - TMC2209 Drivers + sensorless homing
  - BLTouch/3DTouch auto-leveling
  
## DO BEFORE PRINTING!
  - Check stepper motor direction
    - Put X and Y axis in center, move Z axis to create clearance
    - Move all axis 1mm and check the direction, only continue if these are correct
  - With PLENTY of clearance on the Z axis, and your reset button ready, check the probe
    - Home the Z axis and check if the BLTouch/3DTouch probe deploys
    - Push the probe by hand and check if the axis stops moving
  - Sensorless homing is enabled, check the sensitivity (keep reset button ready)
    - Move axis to max position (creates room for error) and home the axis
    - Try to stop it with your hand, use reset button if it doesn't stop
    - I would reduce the sensitivity by 5 or 10, might be easier with [GCode M914](https://marlinfw.org/docs/gcode/M914.html)
  - Check your NOZZLE_TO_PROBE offset, I set it to 0, 0, -0.300 (XYZ) for now
    - If you're going to level your bed without changing this (leveling will be less acurate), please watch if the probe ends up next to the bed
  - Not really needed before printing, but check if the controller knob works right in legacy mode

For bed leveling I used to have the 3-point probe, but then I discovered OctoPrint has a plugin called Bed Visualiser. Now I'm probing all corners so I can see how bad my leveling is :P
You might change it back to 3-point
