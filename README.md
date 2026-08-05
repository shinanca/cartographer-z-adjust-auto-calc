# Auto calculate Z_ADJUST for Cartographer 3D

# Install

```
[include z_adjust.cfg]
```

# How to use

```
CARTOGRAPHER_AUTO_Z_ADJUST_CALC
```

After calculation macro will print table:

```
| Temp  | Z-Adjust
----------------------------------------
...
| 210C  | 0.0183
...
```

Add to slicer in filament g-code:
```
SET_GCODE_OFFSET Z_ADJUST=+0.0183
```
