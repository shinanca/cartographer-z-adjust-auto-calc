# Auto calculate Z_ADJUST for Cartographer 3D

# Install

```
[include z_adjust.cfg]
```

# How to use

On plate and nozzle at room temp
```
CARTOGRAPHER_AUTO_Z_ADJUST_CALC
```
After calculation macro will print table:

```
Change value in OFFSET_TEMP Macro: variable_coefficient: 0.009
| Temp  | Z-Adjust
----------------------------------------
...
| 210C  | 0.54
...
```

Add to slicer in filament g-code:
```
SET_GCODE_OFFSET Z_ADJUST=+0.54
```

You can change in z_adjust.cfg macro TEMP_OFFSET variable_coefficient, then add to START_PRINT macro or in filament g-code:

For PrusaSlicer/SuperSlicer:
```
OFFSET_TEMP TEMP={first_layer_temperature[0]}
```
For OrcaSlicer:
```
OFFSET_TEMP TEMP=[nozzle_temperature_initial_layer]
```
