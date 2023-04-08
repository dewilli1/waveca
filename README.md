# WAter ValvE CAscade
A DIY box with a water in+out and 12V DC in+out, that can be cascaded. It shall be low-cost but provide basic l-safety. Hence, only one valve is used and water shall be connected in "parallel" while the cascading is referring to the current supply to reduce wiring (without dealing with wireless 
stuff). The box shall somehow be mounted on a bucket (plant pot without drain) to realize either an ebb and flow system (requiring a backflow) or simply allow refilling water to a certain level (with the minimum of the box's height). The function may double as a switch to controll a pump with a lower and an upper fluid level sensor.

It consists of
- housing (probably 3d-printed as I already fetched some cheap but oddly shaped components)
- pcb + some electronic parts
- floater, valve, maybe hose connector

## Requirements
### Housing
  - fluid resistant for pH-levels 3.0 to 8.5
  - keeps the pcb from overheating by direct sunlight
  - holds the pcb in a orientation no water drips on it
  
 ### Floater, valve, etc
  - cheap and 12V DC
  
 ### (main-)Board (referred to as pcb)
  - easy to solder
  - about half size of a credit card
  - "slides" into the housing
  - absorbs some mechanical force from the external sockets
  - manifests an electric circuit
  - temperature range is 270K to 320K ambient temperature
  
 ### electric circuit
  - shall never take more than 1.2 A
  - must not take more than 1W when incactive (forwarding current to the next box)
  - has 9-14 VDC supply voltage
  - a fluid level sensor is connected to a valve
  - the valve is open on the fluid side when a current flows through the coil
  - the fluid level sensor opens the electric connection when it's fluid level is exceeded
  - (optional:) a voltage of 5V to 16V resets the "state" which can be active or inactive
  
 #### description using a relay
  - the normally open (*NO*) port is used to pass current to the next cascade element
  - once the *NO* port is connected, it latches the present coil current
  - the normally connected (*NC*) port is used to power the valve (and the fluid level switch evaluation logic)
  - the coil current only needs to be "reset" when unpowering the entire cascade (if doubling as pump controller, it may still be required to reset it via 2nd fluid level switch)
