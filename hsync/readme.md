### HSYNC

The HSYNC is one of the two sub-circuits of the video card. This signal handles the timings of the horizontal positioning of the pixels. The HSYNC circuit has 4 NAND gates which handle the logic for the diplay, front porch, sync and the back porch timings. 
The circuit allows the placement of pixels from 0 to 200. After that front porch comes in between 200 and 210, the sync between 210 and 242 and back porch between 242 and 264.

These different "timestamps" which are actually just values between different pixel numbers make for the image to be properly displayed. 

## The HSYNC Schematic

 
<img width="527" alt="image" src="https://github.com/IEEE-NITK/Video_card_logic_gates/assets/111945991/a480b33f-cacc-4370-8194-c4052e4f577e">


## The HSYNC Circuit


![WhatsApp Image 2024-03-06 at 19 59 32_017317c1](https://github.com/IEEE-NITK/Video_card_logic_gates/assets/111945991/8872cbd5-ab8b-4a62-a921-54619d3528ae)


The lower breadboard comprises of the counters and the NOT gates. Each counter has 4 outputs each, so having 3 counters in total means we have 2^12 bits whearas we only need 9. The 9 outputs ar ethen taken into the NOT gates to make sure a compliment to each of the counter bits are available for logic building.

The upper breadboard has the 4 NAND gates for the aforementioned "timestamps" i.e. 200, 210, 242, 264. The 4 NAND gates go low respectively for these pixel values. The other IC on the board is the SR Latch is configured so as to give a low for the sync pixels and keep a high for the rest of the signal. 

## HSYNC Timing Diagram


![timing jpeg](https://github.com/IEEE-NITK/Video_card_logic_gates/assets/111945991/e5eb7e9d-e364-48dd-bc85-42b0c1a162e4)


