# Power Supply Design Patterns

This is a collection of basic building blocks for electronic circuits.

All circuits need a power supply.
Even if this is external, it's not done connection a Vcc and GND cable.

- Battery charger
- Current source 
- Decoupling capacitors
- HV generation circuits
- Separated supplies (analog/digital)
- Symmetric power supplies
- Transformator + rectifier

# DC-DC Converter

DC is a constant voltage. 
A DC-DC converter is used to generate a desired voltage output from a given or even an unreliable DC input voltage.

- [Linear Regulator](linear-regulator/README.md)
  generate a lower output voltage from a higher input voltage, best for small voltage drops and small current. 
- Zener diode
- Switch mode power supply
  - Buck converter
  - boost converter
  - Buck-boost
  - Fly back
  - Cuk

--- 

[back](../README.md)