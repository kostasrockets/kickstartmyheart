Mach 2 and 20,000' under $500

![image](https://github.com/user-attachments/assets/21e450f0-e342-4c68-abad-834a23f65ef6)

This is my rocket, which I designed with the goal of flying past 20,000' and Mach 2. It uses a custom Reliant Robin propellant rocket motor in a custom machined casing, which I have flown a similar design to before. It will have a fiberglass nosecone a metal 3d printed fin can, which gains me signifigant altitude over traditional manufacturing methods (24,000' vs 22,000'). I've built nearly identical rockets with this structure before, and they've worked, which gives me the confidence to build this rocket in this way. 

The casing is identical to a design I have flown before as well, and has been tested in flight to about 750psi, and hydrostatically to 1600psi. It uses radial bolts to hold the two closures in, and the bolts are loaded in shear when the casing is pressurized. If my math is correct, which I did with a simulator and hand calculations, the casing should fail at 2000psi, at the nozzle end (the safer, and cheaper failiure mode, as it does not risk hitting the electronics if it blows up)

For recovery, the most important part of the entire rocket's flight (because it's dumb and irresponsible to let it recover ballistically) I use an EasyMini flight computer to deploy the parachutes (drouge at apogee, and a main is released at 2000') and a Featherweight GPS to track the rocket during all stages of flight. The GPS uses LoRa to communicate with a ground station, and a GPS chip to have GPS connection. The EasyMini uses a barometer to estimate the altitude of the rocket, which is very reliable up until about 30k', and I use the GPS to give me the actual altitude of the flight. GPS also tends to overestimate the altitude, so I prefer to use that number :). Finally, I use a redundant RDF beacon which just beeps at 433Mhz, and I have a radio on the ground with a directional antenna, which I can use to at least get an idea of the direction the rocket is in, if the GPS fails. The EasyMini and GPS are powered by 400mAh batteries, and the RDF beacon is powered by a small coin cell (It is an independent unit, and is not featured on the wiring diagram because there is no wiring!) This is not by any means an electronics project, so I use COTS altimiters and GPS for their reliability and the fact that I'm familiar with them. 

Wiring Diagram: 

![Wiring Diagram drawio](https://github.com/user-attachments/assets/41453370-f20e-471d-a6e4-4fd68dacfbdd)


Bill of Materials:
| Item                                            | Use                  | Vendor/Source            | Item Price   |
|:------------------------------------------------|:---------------------|:-------------------------|:-------------|
| Craftcloud 3d Printed Fin Can                             | Fin Can (Very important for keeping the rocket straight)          | Craftcloud3DP | $165         |
| 91375A437 - Alloy Steel Cup-Point Set Screw     | Bolts for casing     | McMaster-Carr            | $15          |
| 8870A45 - Uncoated High-Speed Steel Drill Bit   | Drill Bit for grains | McMaster-Carr            | $11          |
| 8870A54 - Uncoated High-Speed Steel Drill Bit   | Drill Bit for grains | McMaster-Carr            | $26          |
| 54mm Nozzle, 0.455" Throat | Nozzle | RocketMotorParts         | $45       |
|                                              |                   | Total Price:             | $262         |
