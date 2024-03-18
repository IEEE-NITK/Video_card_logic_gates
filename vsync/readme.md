### VSYNC

The VSYNC is the other sub-circuit of the video card. This signal handles the timings of the vertical positioning of the pixels. The HSYNC circuit has 4 NAND gates which handle the logic for the diplay, front porch, sync and the back porch timings. 
The circuit allows the placement of pixels from 0 to 200. After that front porch comes in between 600 and 601, the sync between 601 and 605 and back porch between 605 and 628.

These different pixel number ranges make for the image to be properly displayed. 

## The VSYNC Schematic


<img width="535" alt="image" src="https://github.com/IEEE-NITK/Video_card_logic_gates/assets/111945991/897e109d-6c90-402b-ad0e-22824c1196aa">


## The VSYNC Circuit


![vsync](https://github.com/IEEE-NITK/Video_card_logic_gates/assets/111945991/77744c8c-41df-4eb7-9b24-ef9c82cbcd6f)


The lower breadboard comprises of the counters and the NOT gates. Each counter has 4 outputs each, so having 3 counters in total means we have 2^12 bits whearas we only need 10. The 10 outputs ar ethen taken into the NOT gates to make sure a compliment to each of the counter bits are available for logic building.

The upper breadboard has the 4 NAND gates for the aforementioned "timestamps" i.e. 600, 601, 605, 628. The 4 NAND gates go low respectively for these pixel values. The other IC on the board is the SR Latch is configured so as to give a low for the sync pixels and keep a high for the rest of the signal. 

## VSYNC Timing Diagram

![timing jpeg](https://github.com/IEEE-NITK/Video_card_logic_gates/assets/111945991/e5eb7e9d-e364-48dd-bc85-42b0c1a162e4)


