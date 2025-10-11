# Jamboard

We're so back with v2.
This is a 75% keyboard which I designed over the course of a couple of days back in Feb for fun and to see just how hard designing a keyboard could be!
(Minor note: I know the branding on the case says "Just Another Hackboard". That was the original name for the project and is the branding I want for the keyboard. + I'm printing the case myself so it shouldn't be an issue.)

Spoilers: It was difficult.

## Schematic:
![image](https://github.com/user-attachments/assets/e7a38927-3d77-436f-b328-701bc1124f09)
![image](https://github.com/user-attachments/assets/6f2aa29f-deaf-46ef-ac56-3ba0a11f4d1b)
![image](https://github.com/user-attachments/assets/6607ca3a-f9d2-424d-bef2-c37913acca1f)

Arguably the easiest part of the project, the schematic was more just tedious in the sense that wiring the LED matrix along with the switches got pretty tiring after the first 5 or so minutes.
However, it didn't take me too long to make the whole schematic, people on slack helped me with choosing the correct MRC to wire it all to.

## PCB:

![image](https://github.com/user-attachments/assets/79c1f397-91e0-4369-9c15-ad88463334f2)

Ever felt like wiring 700 wires on a pcb? Well now you can!
The pcb design was probably my favourite part and took me more than a few hours over a few days to get all the wiring done to a point where I was happy with it.
The initial positioning also took a while because I was pulling my hair out trying to calculate the sizes of different keycaps (e.g. Tab and caps lock) so the keycaps didn't overlap.
That *was* until I was helping someone on slack and saw they had different sized outlines for the keycaps and decided to take a second look at the footprint library... and lo and behold, people aren't masochists and made different sized footprints for the different keys...
Good news - I got all the measurements right on my own :D.
Bad news - I wasted about an hour doing that :(.

## Case:

Fully Assembled:

<img width="1149" height="733" alt="Screenshot 2025-10-12 001306" src="https://github.com/user-attachments/assets/4cf5864c-4dc0-4cdd-8e43-61d8dbcd7df0" />

<img width="1179" height="563" alt="image" src="https://github.com/user-attachments/assets/0878b6bc-178d-46c8-9722-12602787eae1" />

(Note: MRC pins are clipping through the case in the second screenshot, this shouldn't be an issue when building the keyboard because I'm gonna trim the mrc pins after soldering them :3)

Top Case:

<img width="1218" height="661" alt="image" src="https://github.com/user-attachments/assets/c0aa3871-8f96-4b81-bd45-65bc00948165" />

<img width="1160" height="527" alt="image" src="https://github.com/user-attachments/assets/23197673-5be2-4661-b4e7-1fe9116868c7" />

Bottom Case:

<img width="1234" height="675" alt="image" src="https://github.com/user-attachments/assets/e1e368fd-6b27-4d62-a9ae-80fd0501bfae" />

<img width="1189" height="459" alt="image" src="https://github.com/user-attachments/assets/93ae0392-186b-4edb-a02a-a5fe14c835e2" />

This is the part I changed after my initial PR since there was an issue with the switch holes not aligning properly with the switches themselves along with there not being holes for the stabilsers and 2 screws. This in itself took a while seeing as I initially eyeballed the measurements for the stabilisers before being told to just go to ai03's plate generator (which I should've done from the start). That turned out to be much quicker than scouring the internet for the dimensions thankfully).
After fixing those issues, I saw a nice design from aryatajne28's reaperboard and decided to make one of my own - initially making a separate top and middle plate but merging them in the end in order to fix an issue where screwing the case together wouldn't actually attach the case layers.

I also changed how the art for my board is done - I liked the idea of seeing the MRC through the case but thought that a grate would look weird on the board. The top of my case also looked barren at the top due to it having a "massive forehead" (thanks ben) so I also had to find a solution for that. Luckily, I thought of the idea of using the top of the PCB (also barren) as the art, putting a lot of silkscreen art there to make it look nicer! This not only solved the art problem, but also lets me see the MRC (yay!).

The art includes boywithuke, chiikawa, orpheus and some handpicked quotes from my friends. I've put a gap in the top plate so I can put an acrylic plate there when I order my parts.

The cutouts on the bottom of the case are for if I want to add keyboard feet later on, which is the reason why there isn't a CAD file for keyboard feet. As it stands right now I don't really care about keyboard feet sooooooo...

## Firmware:

There's not much to put here since I've learned a lot from the hackpad firmware incident, meaning this part only took like 30 minutes to do :D.
It's basic firmware (led controls, matrix and rotary encoder controls) which I plan on expanding and developing when I have the board to experiment with since it'll be easier to do then.

## BOM

**NOTE: All items here are ordered in the lowest amount available, even if the quantity is >1. The quantity references the amount of items inside the pack.**

[BOM Table (In Google Sheets)](https://docs.google.com/spreadsheets/d/10ayODNDgifRF8TIKmW62j9T8PxfnleCE7DduQY3qoK8/edit?gid=501465466#gid=501465466)

| Item | Quantity | Price | Source |
|------|----------|-------|-------|
| Orpheus Pico | 1 | N/A | HQ |
| PCB | 5 (min) | $25.60 | Grant |
| Case | 1 | N/A | Printed myself |
| [Gateron Red Switches](https://www.aliexpress.com/item/1005005550328893.html) | 90 | $26.60 | Grant |
| [EC11 Rotary Encoder](https://www.aliexpress.com/item/1005005983159472.html) | 1 | $1.91 | Grant |
| [SK6812 MINIE LEDs](https://www.aliexpress.com/item/1005007863635868.html) | 100 | $3.57 | Grant |
| [1N4148 Diodes](https://www.aliexpress.com/item/4000142272546.html) | 100 | $1.65 | Grant |
| [PBT Side Printed Keycaps](https://www.aliexpress.com/item/1005008769598276.html) | 1 | $19.34 | Grant |
| [Aluminium Alloy Knob](https://www.aliexpress.com/item/1005008054145777.html) | 2 (1pk) | $4.72 | Me |
| [DUROCK Plate Mounted Stabilisers](https://www.amazon.co.uk/Sarini-Stabilizers-Stabilizer-Replacement-Accessories/dp/B0D6VF4SQB/) | 1 Set (4x2U 1x6.25U) | $7.81 | Grant |
| [M3 Allen Bolt](https://www.aliexpress.com/item/32810872544.html) | 50 | $2.11 | Grant |
| [M3 4.5mmOD 6mm Length Threaded Inserts](https://www.aliexpress.com/item/1005004535859664.html) | 50 | $2.83 | Grant |
| [Acrylic Sheet (1mm thickness)](https://www.simplyplastics.com/catalog/sheet/cast-acrylic-sheet/clear-cast-acrylic-sheet/c-24/c-83/p-203) | 1 | $5.34 | Me |
| Shipping (Aliexpress) | N/A | $6.74 | Grant |
| Shipping (JLCPCB) | N/A | $12.45 | Grant |
| Shipping (Acrylic) | N/A | $9.37 | Me |

HQ Total: $110.59

Self-Funded: $19.43

BOM Total: $130.02
