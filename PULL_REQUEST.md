# Controls-MinionTestPCB
 
# Quality Assurance Checklist 
To make reviews more efficient, please make sure the board meets the following standards and check everything off once the board meets the quality check. Once everything has been checked, the assigned reviewers will begin the review process. 
 
There are exceptions with all guidelines. As long as your decisions are justified, then you are good! Contact the reviewers or the leads about any exceptions. 
 
### Minimum Prerequisites 
- [X] Pushed changes to branch. 
- [X] The board passes ERC and DRC. 
	- Note some ERC warnings are acceptable. 
- [X] All traces are routed. 
- [X] Units are in metric. 
- [X] Everything in schematic level is annotated and all components have datasheets associated with them. 
- [X] BOM was generated at schematic level and price of all components is listed in BOM somewhere. 
- [X] 2 Members of the team have already reviewed my PR 
- NOTE: Approver will not look at PR if 2 other members haven't reviewed first 
 
## Schematic Level Requirements 
- [X] (NOT APPLICABLE) Is proper noise resistance given to all peripheral devices (bypass caps and coils/ferrites)?  
- [X] (NOT APPLICABLE) Is proper ESD protection given to all MCU input pins (zener diodes)?  
- [X] (NOT APPLICABLE) Is proper power protection given to peripheral devices (zener diodes)?  
- [X] Are peripheral units used properly (reading datasheet)?  
- [X] Are testing points added at useful places?  
- [X] (NOT APPLICABLE) Is there proper short to GND protection at MCU outputs (inline resistors)?  
- [X] (NOT APPLICABLE) Do ADC inputs have caps?  
- [X] (NOT APPLICABLE) Are ADC inputs biased so there is room above expected value to determine if value is being overflowed?  
- [X] Are LED's located at useful places (comm, power, debugging, extra GPIO)?  
- [X] Are parts chosen easy to collect?  
- [X] Are parts chosen easy to solder?  
- [X] (NOT APPLICABLE) Is there reverse polarity protection on inputs?  
- [X] Schematic should have version number in Revision portion on bottom right of top level sheet. 
 
## Layout Level Requirements 
 
### 2D Spacing 
- [X] The components are spaced out at an optimal distance. 
	- All components can be easily hand-soldered. 
	- IPC-SM-782A Standard requires a minimum distance of 1.0mm from edge to edge. 
- [X] Components that are in parallel with each other are spaced out at an equal distance when possible. 
- [X] The components are aligned with each other when possible. 
- [X] Components are grouped based off of functionality. 
	- E.g. all components for CAN should be grouped. 
- [X] (NOT APPLICABLE) Bypass capacitors are less than 1cm away from their respective IC's power pins. 
 
 
### 3D Spacing 
- [X] Layout of components have been placed with mounting location and usage of the board in mind. 
	- Are PCBs going to be stacked on above/below this board? Are tall components placed accordingly? 
	- Are buttons and lights easily accessible and viewable? 
	- When mounted into the car, are the heights of the components and connectors accounted for? 
- [X] Location of connectors and wires going out of the board will prevent messy wiring. 
	- Are all the wires that are going in the same direction placed on the same edge of the board? 
 
### Components 
- [X] Custom footprints have been double checked with the datasheet. 
- [X] Pin 1 of the footprint is labeled in some way. 
- [X] Are LED's in easy to see places? 
- [X] Are test points in easy to reach places?  
- [X] Are critical paths of switching converters as small as possible?  
 
### Copper Layer 
- [X] The trace widths and trace clearances are greater than JLCPCB's minimum requirements. 
	- [X] Are signal traces 6mils unless provided with reasoning?   
    	- NOTE: One net can have multiple trace widths  
- [X] The trace lengths are as short as possible. 
	- Can there be a more optimal route if you go to another layer? 
- [X] Each trace's width is capable of handling the expected current flow. 
	- Use PCB width calculator to calculate trace width. 
    - 2mA for LED diodes (trace 0.25mm can handle 400mA)
    - 400mA max for switches (trace 0.25mm can handle 400mA)
    - 3A for banana plugs (trace 3.6mm can handle 3A)
- [X] *No sharp corners. No trace angles equal to or less than 90 degrees. 
	- Orthogonal traces should have vias if necessary. 
- [X] (NOT APPLICABLE) Are edges of board surrounded by clean ground on both layers with stitching vias? 
- [X] Traces are in parallel with each other when possible. 
	- E.g. traces connected between an IC and MCU can be placed in parallel with each other. 
- [X] There are no random trace appendages. 
- [X] No vias on copper pads 
- [X] Through-hole components do not have extraneous vias. 
 
*Not really a problem for modern manufacturing techniques but good practice and important for high speed signal integrity. 
 
### Silkscreen Layer 
- [X] Visible text sizes are greater than JLCPCB's minimum requirements. 
- [X] All visible text is on the silkscreen layer. 
- [X] All reference labels of each component are not overlapping a copper pad or another component. 
- [X] All connector pins are labeled with a meaningful and helpful name. 
- [X] All LEDs are labeled with a meaningful and helpful name. 
- [X] Silkscreens are mostly facing one direction (or 2). 
- [X] Version number is located next to UTSVT Logo 
- [X] Hallocks Image is somewhere on board. 
 
### Edge Cut Layer 
- [X] The dimensions of the board and the mounting holes are nice values in metric i.e. no long decimals. 
- [X] The physical outline of the board is on the edge cut layer. 
- [X] Edge cuts are straight and parallel with opposite edge of the board. 
- [X] Mounting holes are aligned. 
- [X] Corners are curved and contoured to mounting holes. 
 
### IMPORTANT NOTICE 
- [X] I am confident that this board will be safe to use in a safety critical environment. 
- [X] I had fun :) 
 
## Other Comments 
_Write any comments about the board that would help the reviewers here._ 
 

