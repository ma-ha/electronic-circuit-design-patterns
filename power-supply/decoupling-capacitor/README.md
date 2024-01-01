# Decoupling capacitors

ICs with the need to generate quick raise from 0 V to Vcc need a quick current pulse.
Since any cable or PCB has an impedance depending on the way the current has to travel, the current cant deliver high slew rates.
In digital circuits in the MHz region this can lead to malfunction.

The solution: Place a capacitor with a low ESR as close as possible to the (every) ICs Vcc Pin to GND. 
This can also prevent ICs from unwanted self oscillating (e.g. 78xx regulators).

In SMD designs any low ESR capacitor (MLCC) with high enough (> 100 nF) can be placed less than 1 mm to the ICs Vcc pin. 
Since the ICs are very small (bonding cable length), the Vcc impedance can be neglected.

![decoupling-capacitor-smd](decoupling-capacitor-smd.png)

Example: A 100 nF X7R 0805 has its lowest impedance at ca 30 MHz and even at 200 MHz its only 390 $m\Omega$. 10 uF has only 15% higher impedance at 200 MHz. A 10 nF has 320 $m\Omega$ at 200 MHz. By this a 10 nF performs not much better than a 100 nF or a 10 uF.

![SMD ESR](smd-esr.png)

(Source: https://ksim3.kemet.com/capacitor-simulation)


If you face slew rate problems with a 100 nF SMD MCLL, you must carefully select a capacitor to work best at for the desired rise time
(which might be faster than the clock speed of the IC).

For THT designs it's more complex since the effective distance between the capacitor and the IC semiconductor is 1 cm or even more.
A combination of different sized capacitors can help to mitigate this issue.
