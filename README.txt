This is my personal test data
Tested with Neptune 4 Max

The following modifications will be made

X motor -> 0.9 degree stepper
Expected benefits: Reduce/Lower VFA (Vertical Fine Artifacts)

Y motor -> Stronger stepper, testing out 16T pulley along with stock 20T
Expected benefits: Higher maximum usable acceleration

E motor -> Different motor (Benefits unknown yet)
Expected benefits: Higher torque -> higher maximum volumetric flowrate

Notes:
Current is the motor run current in Klipper, not the maximum rated current of the motor
VFA test would be done at 20mm/s, 50mm/s, 100mm/s, 150mm/s specifically on X axis and Y axis independently
Accel test would have velocity limited to 500mm/s
Accel value would be taken at 100mm^2/s intervals, and the closest result that does not skip steps will be taken. ie: skips at 21000mm^2/s -> result: 19900mm^2/s
Accel tests will have the max accel to decel value of klipper = accel value
Volumetric speed will be taken in 2.4mm^3/s interval (1mm of filament = 2.4mm^3 of volume)
Volumetric speed value will be taken as extruded 300mm of filament successfully without skipping (equals to long walls, short span volumetric speed may get higher)
Extruder in question: dual drive extruder with 52:10 gear ratio, bondtech BMG style extruder gears
Hotend in question: 65W bambu TZ2.0 hotend fitted with biMetal (nickel plated copper/hardened steel) CHT 0.6mm clone nozzle
These tests are done with TMC2209 drivers

Details:
X: Target: reduce/eliminate VFA
Stock motor serial:
Stock motor current: 0.8A

Upgraded motor serial:
Upgraded motor current: 0.8A

Y: Target velocity: 500mm/s (All tests are done with this velocity)
Stock motor serial:
Stock current: 1.4A (Unsure if it can be pushed higher)
20T pulley stock motor max usable accel: 7800mm^2/s
16T pulley stock motor max usable accel: ?

Upgraded motor serial:
Upgraded motor current: 1.7A
20T pulley upgraded motor max usable accel: ?
16T pulley upgraded motor max usable accel: ?

E: Target volumetric speed: higher than stock
Stock motor serial:
Stock motor current: 0.9A (Specsheet unknown, but usually these NEMA14 are rated at 1A max)
Stock max volumetric speed: 38.4mm^/s

Upgraded motor serial:
Upgraded motor current: 0.8A
Upgraded motor max volumetric speed: ?