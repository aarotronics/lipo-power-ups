# Lipo Power UPS

DC uninterruptible power supply specially designed for 3D printers. It can be used in both 24V and 12V systems. 
For the recovery battery use a high capacity LiPo or LiIon battery, 6S for 24V and 3S for 12V. High power 
diodes conmutate power from power supply or battery so printer will no turn off even when electrical lines 
goes down. While 3D Printer is powering from power supply, current from battery will be 0A because of diode 
barrier, so it wont be discharged at all.

The time that system can keep the 3D Printer working with battery depends directly on how much power the 3D Printer 
drains itself; and also on the battery size, bigger battery will keep the system working for more time.

LiPo and LiIon batteries will damage if they get down of about 3V per cell, thats why the system has an integrated 
power MOSFET and a voltage sensing circuit that will turn off power from battery if it goes down the security 
voltage of 3V per cell. You may have to print again, but battery will be safe.

# Configuration

System can be used both for 24V and 12V systems. In case you are using 12V system, you will not have to use Q4, D17, 
R6 and C8 components. These components make a basic discrete 12V regulator to get 12V from a 24V system.

For 12V system you will have to close the jumper JP1, but for 24V leave it open!!

For 12V R1 should be 33K and for 24V R1 should be 75K. Make sure you are using precise resistor!! These resistors 
make part of the voltage sensor and measurement will be affected by these resistors.

![Schematic](/img/LipoPowerUPS.svg)

![3D Render TOP](/img/render01.png)

![3D Render BOT](/img/render02.png)
