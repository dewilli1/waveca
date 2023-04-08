# Libraries to run simulation

As Kicad has only very limited simulation support, we need some additional stuff for our some waveca components. As even the LT-Spice basics are missing, the schematics are created by LT spice, but they still require some changes. For some, a testbench may exists to directly verify it in kicad, including the transient simulation setup. The netlists for all asc's are modified to suit Kicad's LT-Spice compatibility requirements (figured out by trial and error) and collected in **subcircuits.lib**. It consists of the following models:

##G5V-1

The relay I bought actually to be connected directly to the switch. I picked some random coil wattage as trigger level and an arbitrary value for inductance as I haven't measured it yet.

## TBD
- The fluid level switch is not simulated yet, maybe a model triggers it after an imaginary capacitor is charged.
- The fluid valve is neither simulated yet, but a 24 ohms resistor may do.
