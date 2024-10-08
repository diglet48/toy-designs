
# Project description

This is a pneumatic actuator intended to drive venus 2000 style sex toys. 
The large bore diameter and 2:1 pulley reducer makes this design relatively compact. 
A powerful NEMA23 servo motor, borrowed from the OSSM project, handles control.

Keep fingers away during operation.


![](images/overview.jpg)
![](images/top.jpg)
![](images/belt-view.jpg)
![](images/belt-closeup.jpg)

# Bill Of Materials

Mechanical parts:

1. SC63-150 pneumatic cylinder from aliexpress.
2. MGN12H Rail and bearing, 250mm or 300mm (300mm in pics). If you use any longer rail, it will stick out in the front.
3. NEMA23 motor. I use IHSV57 180W.
4. 8x MR115-2RS 5x11x4mm bearings
5. 2x 608 8x22x7mm bearings
6. 2MGT timing belt, 1 meter. Design allows for a maximum belt width of 10mm.
7. 20-tooth 2MGT pulley. You must use 20-tooth or the pulley mechanism will bind.

Nuts and bolts:

1. 4x M3 6mm cap head for linear rail.
2. 4x M3 8mm for rail idler, any head type. 
3. 2x M3 8~16mm for piston arm, any head type.
4. 6x M3 nut.
5. 1x M5 30mm button or cap head for tracking adjustment.
6. 2x M5 30~50mm button or cap head for tensioner and motor bracket.
7. 1x M5 20~40mm button or cap head for motor tracking adjustment.
8. 2x M5 24~27mm button or cap head for rail idler, button head preferred.
9. 3x M5 nut.
10. 1x M8 50mm cap head for idler. Can be substituted for 8x30mm pin (modify design yourself).
11. 5x M8 20mm countersink for mounting the big prints to the cylinder.
12. Something to mount the motor. 4x M4 16+mm countersink, or various short M5 nuts/bolts.

Electronics/software:

Not part of this design. You could use the OSSM reference board.

Plumbing:

8 to 9mm ID is likely the best choice.
You can use 12mm aquarium tubing or 9mm ID garden hose. Test details below

12x8 aquarium tubing (measured 8.5mm ID) will press-fit on the original venus 2000 receiver.
A few wraps of teflon tape will make the connection airtight.

# Plumbing details

The original venus uses approx 9mm ID, NimbleStroker 16mm ID.
I tested 8mm aquarium tube (5mm ID) and 12mm aquarium tube (8.5mm ID).

Here are some numbers about volume:

| part                                                      | volume |
|-----------------------------------------------------------|--------|
| SC63-150 pneumatic cylinder                               | 460 ml |
| venus 2000 (8.2cm diameter * 4cm displacement, estimated) | 211 ml |
| tremblr (6.3cm diameter * 7cm displacement, estimated)    | 218 ml |
| 1 meter of 5mm id tubing                                  | 20 ml  |
| 1 meter of 9mm id tubing                                  | 63 ml  |
| 1 meter of 16mm id tubing                                 | 200 ml |
| venus 2000 receiver (5cm * 16cm)                          | 314 ml |

I find myself using between 60% and 80% of the SC63-150 volume, so I'm a bit surprised the 
volume of the commercial devices is so low.

I attempted to isolate the power usage of the different components of this build at 60% stroke length, 2 strokes per second.

| Component              | power usage                     |
|------------------------|---------------------------------|
| motor + belt + rail    | 8w                              |
| cylinder friction      | 16w                             |
| air resistance 1m tube | 20w (5mm ID) <br> 3w (8.5mm ID) |
| venus 2000 receiver    | 5w                              |

It can be concluded that 5mm tubing adds significant extra resistance,
8.5mm appears to be large enough. You probably don't want to go larger because extra air
makes the system less responsive.




# Printing

All parts can be printed without supports, bridging mode required.

The back motor plate must be printed in a temperature resistant material 
such as ABS. 
This is the only part that needs with withstand high temperatures.

The rail idler and rail arm benefit from being printed in a 
creep-resistant material such as ABS, but they will work fine
if printed in PLA if you re-tighten the bolts regularly.

The front idler should be printed with 3x the normal amount of top/bottom layers.

Rest can be printed with default settings.


# Assembly instructions

The rail-mounted idler needs to be oriented with the cutout towards the front.

Adjust the motor support bracket and idler bolts to adjust belt tracking.

The belt tensioner insert must be inserted from the back, or it may slip. If you can't insert the tensioner, make it 5% / 0.1mm thinner and try again.

After assembly, loosen and re-tighten the bolts securing the linear rail to ensure it's parallel to the piston.


# Changelog

26/06/2024 Update front idler design with longer bolt, added washer to put between bearings.  
27/08/2024 Update rail idler for shorter belt path, improves tracking.
17/09/2024 Update motor mounting solution.
