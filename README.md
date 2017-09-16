# stairpad
Firmware for a cheap pressure pad using capacitance

We use a very simple pressure pad - 

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
------------------------------
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
------------------------------
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

Where x is card and - is aluminium foil. This forms a simple capacitor.
When someone steps on it the middle layer of cardboard is compressed and increases
the capacitance of the capcitor

Each piece of foil is connected to a wire; then everything is connected to a simple
8 pin microcontroller, which alternately charges and discharges the capacitor through
a high value resistor (1 MOhm). The time taken to charge the capacitor to a certain voltage
is recorded; if it increases substantially, then we know that someone is standing on it!


At the microcontroller we use two pins - one to charge the capacitor, and one to measure the charge and also discharge it.
Finally we use the microcontroller to communicate on a serial line to register when it senses pressure...

