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

![03 - Casing(2)](https://github.com/user-attachments/assets/188f017e-1392-4817-90e0-35d20af51a2f)


This is a bolted casing, a type of casing that has been used by professional and amateur rocketeers for a very long time. There are bolts (316 set screws in this case) which screw into bolt rings which are intended to hold the pressure. It has a phenolic liner which prevents the propellant from melting the casing itself (very useful to do this, as it helps your rocket not blow up). I designed this casing using some [some pretty simple math](https://static1.squarespace.com/static/60d8d9b060e90a67c5c69db4/t/62997fbfa1150834ce0a9556/1654226881895/How+to+Design+Pressure+Vessels%2C+Propellant+Tanks%2C+and+Rocket+Motor+Casings.pdf) to calculate my safety factor for bolt shear. (I honestly just realized how simple this math is, used to treat it like black magic). The casing is calculated to fail at 2000psi, and yield at 1500psi, but I really don't want to hit anywhere near that pressure, because it's made from 6063 T832, and my friend thinks that the case will lose it's temper after a short burn, meaning that it will blow up. This rocket is supposed to prove him wrong (I hope...)

Next, I designed the avionics bay:

![01 - 02 - Avionics   Nosecone(6)](https://github.com/user-attachments/assets/45d15fdf-dce4-42e6-bbf6-3f1e8f5ce66d)

I use all COTS computers in here. A Featherweight GPS, an Altus Metrum Easymini, a Featherweight Blue Jay, as well as a RDF (radio direction finding) beacon for backup tracking if all else fails. The avionics bay structurally is just a 3d printed part. In the past I have had 3dp parts survive in the tip of a nosecone, and so I'm not worried about it. I've also used G10 to make an avionics bay, but it's expensive. 

Afterwards, I designed the fins: 

![00A - Main(6)](https://github.com/user-attachments/assets/750db845-f4cf-44e4-95e0-cdf02a9ea054)

This fin concept is very weird. I want to etch aluminum using a 1 mol sodium something or other solution. It's kinda hard and grueling to do. 

# Day 2: Simulations & CAD Updates

I started by immediatley getting rid of the weird aluminum fins concept, and replacing it with a traditional 'fin can', where I simply bond some carbon fiber fins onto a tube that I lay up using the casing as a mandrel. I have a little metal lip in front to prevent the front of the tube from getting delaminated/rolled over, because that has happened on similar flights by others in the past, which risks destroying the rocket, or even worse, losing performance. 

![05 - Fin Can](https://github.com/user-attachments/assets/fbce54e4-2ba5-44e1-991a-e2d0de6f2f52)

I ran some simulations, for the motor & rocket itself:

![image](https://github.com/user-attachments/assets/411bda44-b619-40db-916e-c96b11028655)
![image](https://github.com/user-attachments/assets/3f499533-810d-4cc9-a0dc-0f53188a4b87)

I ran these simulations in both openrocket and RASaero. They agreed pretty closely. I made sure I had a decent static stability margin during my entire flight regime, ensured my CNalpha was above 10 for the entire flight regime, but did NOT check damping ratio, because it requires one math equation in a spreadsheet and I was lazy. These are also rules of thumb which I follow instead of actually learning a bunch about stability because supersonic rocket stability can get weird, and the math is far too complicated for me. 

# Days 3-5 Manufacturing

I didn't actually count how many days I spent manufacturing, so this is an estimate, which is probably less time than I actually spent manufacturing. 

Before even starting the CAD, I already had machined a nosecone tip because I was bored in class, and it came out really really nice. My process for machining it on the lathe was to essentially machine it 'backwards' with the sharp end towards the chuck, allowing me to only need one setup for my nosecone tip, so everything is perfectly concentric. I used the taper attachment tool on my schools lathe in order to get a 5* taper. I tapped it M8 (why? no idea...)

![image](https://github.com/user-attachments/assets/8cfc06ae-b4db-4589-bb72-f7d298e141ef)
![image](https://github.com/user-attachments/assets/438fc658-376b-44d8-8b51-1c981e81cef7)

I first manufactured the nozzle extension/aft closure, the part which holds the nozzle end of the motor in the casing through radial bolts. This was a more difficult part to manufacture because it needed good ID/depth tolerances. I hit those good tolerances though, and that's something I'm pretty proud of as I've struggled with them in the past :) 

![image](https://github.com/user-attachments/assets/5508589d-2963-4026-9b7b-f4f83603a612)
![image](https://github.com/user-attachments/assets/183afa35-66dd-4cbc-a6d9-e8c81f7fd5f2)

Then I manufactured the other 3 parts... and for some reason, I didn't take pictures as I did it. (Good shop practice, or whatever). 
- For the forward bolt ring (tube in the picture), I polished it up to 220, and then just used a parting tool. I was okay with the tolerances, but the calipers at the shop have messed up depths, so what I thought was 3.500" was actually like 3.489" :( 
- For the forward closure, I had already drilled my only stock to the tap diameter of 1/4" NPT, so I tapped it 1/4" NPT instead. This gives me the added bonus of being able to use this closure on a static test if I want to. Silly mistake, but I rolled with it and it was okay in the end.
- For the nozzle carrier (the part on the nozzle), I used an internal grooving tool to make the O ring groove which seats against the nozzle. I'm bad at using internal grooving tools, so I kinda struggled with it, but it ended up ok in the end. 

![image](https://github.com/user-attachments/assets/03a898bd-5936-4156-af38-9981c0dea0a3)
 
# Day 6 - Oopsie! 

I needed to do the last operation to manufacture my casing - cutting the aluminum tube on a chop saw. I ended up cutting it EXACTLY 1" too short, because I burned an inch when measuring and then forgot to account for it. 

However, I got to put the radial bolt hole guides on and see the whole thing assembled, which is nice:
![image](https://github.com/user-attachments/assets/76e4d55d-2e0c-4222-934b-a3799e3f5f25)

When I got home from the shop, I went home and did some further fin shape optimization to deal with the fact I had 1" less propellant. More importantly, I made the nosecone a very pretty shade of green. 
 
![00A_-_Main5](https://github.com/user-attachments/assets/24583e4f-f26e-4470-a64d-dfbe6afba09e)

Updated sims agreeing very closely!

![image](https://github.com/user-attachments/assets/c3da2d71-c753-4d87-8c88-a3b732c6b695)

# Day 7 - Finalization of the casing
I drilled the bolt holes in the casing. I still need to tap them and drill the clearance holes, but that's not a big deal, and can probably be knocked out in an hour or so. 

![image](https://github.com/user-attachments/assets/9628171f-9f25-41e3-acf3-183b33f308eb)

Incredibly proud with how the casing turned out. Not bad for a quick build, and I really hope it doesn't blow up. I plan on working on the composites in the coming few weeks. 

# Day 8 - Optimization & Actually finishing casing

I actually finished the casing today, tapping the holes, etc.

I also added even more motor to the motor, made it a little less likley to blow up (made sure my nozzle exit pressure was ok) 

![image](https://github.com/user-attachments/assets/70588f15-2ba4-44b9-a50b-cabdd224c5f3)

# Day 9 - Avionics Bay Work

This day, I went to a friends house and he repaired my broken tracker (I previously planned to buy another, but I couldn't afford it) He fixed a broken communication trace on the side of the tracker which prevented the GPS from functioning, and replaced the antenna with a much more compact, but mildly worse wire antenna. (if you're reading this thank you x1000!)

<img width="344" alt="image" src="https://github.com/user-attachments/assets/79f933f6-9e74-4cf1-80f6-e014b3f705b5" />

Afterwards, I put the avionics on the 3d printed sled. 

<img width="246" alt="image" src="https://github.com/user-attachments/assets/b9355073-f057-44c4-a53a-e9beed8034a2" />
<img width="211" alt="image" src="https://github.com/user-attachments/assets/ca47db36-3a88-49b1-8901-71eb206eaa41" />

The darker green board with a buzzer is an Altus Metrum [EasyMini](https://altusmetrum.org/EasyMini/). This particular EasyMini has been through a lot... Mach 2.7, hitting the ground at 110mph, and then left in the desert for 3 months... I will test it before I fly the rocket, to make sure it can still fire charges with the battery I am using (I am using regulated 1s batteries, so I'm a little bit worried about browning out when it tries to fire the charge) 

The lighter green board with a GPS antenna is a [Featherweight GPS](https://www.featherweightaltimeters.com/featherweight-gps-tracker.html). In the configuration in the pictures, It would not have worked very well due to RF interference between the GPS and LoRa antenna, which someone on an online forum pointed out (Thank you!). I moved the LoRa antenna by the side and out of the way of the GPS antenna, batteries, and the central threaded rod. I don't want to take any chances with RF...

# Day 10 - Composite Layups & More Optimization

I did two composite layups this day, one for the nosecone, and one for the fin can. 

The nosecone layup is fairly simple. I made a mold which interfaced with the coupler part which would attach to the casing, which would hopefully lead to me having a perfect fit of the nosecone on the coupler. Good fits are very very important when you are going fast, because any slop can lead to instability, etc... 

My process for making the nosecone was very simple. Like [this](https://www.youtube.com/watch?v=jRbXzujI6ho) video, I used a condom laid up over a sanded down mold, which was designed not to have any sharp edges as to risk breaking the condom. Afterwards, I put a fiberglass sleeve on the nosecone carefully, being sure to not touch the mold until the sleeve is over the mold (in order to avoid stressing the condom/messing up the weave of the fiberglass). Afterwards I wet out the sleeve with laminating epoxy, and then repeat the process for the amount of layers I plan to use. I planned to use 4 layers for this flight based on previous flights of other peoples rockets which have worked using that many sleeves, but I added another layer of sleeve to sand down for a nice surface finish. 

<img width="131" alt="image" src="https://github.com/user-attachments/assets/81ef3996-6333-44a2-ac0c-94bc7552c40d" />

<img width="249" alt="image" src="https://github.com/user-attachments/assets/18e9c96d-37cb-47c4-b8a4-3c59083804c7" />

Afterwards, I roll wrapped a tube for the fin can. 

I havent really roll wrapped tubing before, so my friend helped me. We used a mandrel made from the same tube that the casing was made from in order to lay it up. We used mylar for mold release (not really, but it serves the same process), which was taped together in a roll around the tube. Then, we cut a peice of carbon that was 14" x 18". It was 18" wide because it needed to be 3 rolls around the tube for strength (likely overkill, but that's ok)

<img width="476" alt="image" src="https://github.com/user-attachments/assets/b23d5944-3467-41b2-a5ff-e4bca013b514" />

# Day 11 - Day #1 of nosecone post processing

The nosecone came off the mold really ugly, as most nosecones do. I then put the nosecone onto my friends lathe in order to sand it coencentric. This was my first time using the lathe for sanding, and it was so incredibly useful. It is VERY important to note that I was wearing proper PPE while doing this. Never sand Fiberglass, Carbon Fiber, Phenolic, and many other materials often used for rocketry without wearing proper PPE, because they really like to shred your lungs if they get in there. Not fun.
 
<img width="498" alt="image" src="https://github.com/user-attachments/assets/8a2e266b-70cc-40bd-aa42-34856f9f7fed" />

This was the result afterwards, very shiny, sanded 60-100-220-400-600-1000 grit sandpaper: 

<img width="327" alt="image" src="https://github.com/user-attachments/assets/7305cf1e-b9c8-4ee2-89bb-7e7afc7f21f1" />

# Day 12 - Day #2 of nosecone post processing

I painted without primer for this nosecone because I thought it would be pretty and easy. The first coat of paint was drippy and the finish wasnt great, and I sanded it on the lathe. This turne out to be a bad idea because it sanded through the paint... oops. My process was fairly standard, being: paint, sand, repeat. I eventually did this enough to get to this result: 

<img width="294" alt="image" src="https://github.com/user-attachments/assets/d9dee45a-c5ef-4f63-84ff-658905356eee" />

This is by far the best nosecone I have manufactured yet, so that is a pretty huge win. I'm happy with the result and pretty confident in it being good enough. 

I also released the tube this day,took no pictures, but it looks good.

# Day 13 - Optimization (Metal Fin Can!!)

Today I explored the idea of using a metal 3d printed fin can. I've done this before with good success, and metal printed fincans are often just as straight as a well made composite fin can. I cadded one quickly, and ran some more simulations to see I gained some pretty signifigant altitude and speed. (I don't have exact numbers atm) 

![06 - Metal Fin Can(2)](https://github.com/user-attachments/assets/d1c9832a-97b2-4cf4-82fb-e898b8ddeb90)

I also changed the fin planform to be have more root chord, which made me more comfortable with having the tiny fillets I have on the printed can. It is still good enough for stability. Overall it makes the rocket pretty signifigantly lighter because there isnt any heavy epoxy for the fillets. The rear corner of the fin is filleted so I don't have to risk shock cord getting cut there after deployment. 



