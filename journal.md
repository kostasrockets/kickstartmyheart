# Day 1:  Ideation & Cad 
The design constraints of the rocket are as follows: 
- The rocket shall go at a velocity above Mach 2
- The rocket shall reach an altitude > 20,000' 
- The rocket shall be optimized
- The rocket shall utilize an Ammonium Perchlorate Composite Propelant motor designed by me
- The rocket shall be tracked by GPS for the entire descent
- The rocket shall descend under a parachute
- The rocket shall utilize an avionics bay that is reasonable to work with.

At this point, I have mostly locked down my deployment, but my GPS has been unreliable (My last rocket lost GPS at apogee and has not yet been found). I also chose to require a less space efficient avionics bay, as though it could gain me altitude, on my last rocket, it made me lose my sanity. 


The avionics bay in question:

![image](https://github.com/user-attachments/assets/4eb27a74-df6e-4821-b1a7-46e59f37ffeb)

With these requirements set, I started the CAD by making a master sketch of what the entire rocket would look like. 

![image](https://github.com/user-attachments/assets/d70af87b-d513-48ae-9055-af36fc86d184)

From that, I designed the casing. A casing for a rocket motor is the pressure vessel, it is meant to hold all of the pressure (700 psi is my MEOP, I hydrostatic tested a similar casing to 1500 psi) 

![image](https://github.com/user-attachments/assets/bd6f9877-c4cf-46d9-9508-803272104d6a)

This is a bolted casing, a type of casing that has been used by professional and amateur rocketeers for a very long time. There are bolts (316 set screws in this case) which screw into bolt rings which are intended to hold the pressure. I designed this casing using some [some pretty simple math](https://static1.squarespace.com/static/60d8d9b060e90a67c5c69db4/t/62997fbfa1150834ce0a9556/1654226881895/How+to+Design+Pressure+Vessels%2C+Propellant+Tanks%2C+and+Rocket+Motor+Casings.pdf) to calculate my safety factor for bolt shear. (I honestly just realized how simple this math is, used to treat it like black magic). The casing is calculated to fail at 2000psi, and yield at 1500psi, but I really don't want to hit anywhere near that pressure, because it's made from 6063 T832, and my friend thinks that the case will lose it's temper after a short burn, meaning that it will blow up. 
