# Progress Log

## Progress 1 - Planning the Keyboard

**9/9/2026 4:00 - 4:50 PM EDT**

Found a simpleish design that I thought looked relatively nice and cool. This is for planning the keyboard. I also measured the size of the different keys. 1 = regular keys on a keyboard, 1.25 = slightly bigger keys (control, windows, etc), 1.5 = tab. 1.75 = (Caps lock, backspace, etc.), 2 = enter key, 2.25 = large shift, 6.25 = spacebar. This layout seems relatively easy to design.

Keyboard Design

![image alt](https://github.com/natehui0/nate-keeb/blob/cdcc3f970cb1d8ffc97841481b7d620428d1d1a9/keyboard-layout-2.png)

## Progress 2 — Creating the Schematic

**September 9, 2026 — 5:00 PM–7:00 PM EDT**

I was half-lost when designing this PCB. I followed the instructions on the Keeb website and ended up with this result. The only difference that I noticed was that, in the example on Keeb, the entire keyboard was in a grid (meaning that either the keys were 1x1 or 1x2 and was not designed similarly to a standard keyboard. As a result, I was not sure if the schematic needed to match the layout of the keyboard). So I ended up playing it safe and designed the schematic to match the layout of the keyboard (which was extremely tedious, as I had to keep altering the spacing to ensure a similar design). I also wasn't sure if the pico needed to be within the grid or not, so I threw it in the bottom of the grid. Overall, this step has taught me a lot about KiCad so far, and I'm looking forward to the next step. Also, I wasn’t sure which stabilizers were which.

Schematic

![image alt](https://github.com/natehui0/nate-keeb/blob/d9eb6e57f53638d1765ce57265051df7d152bb8b/keyboard-design-layout-pcb.png)

## Progress 3 — PCB Layout & Routing

**September 10, 2026 — 6:00 AM–10:00 AM EDT**

Arranging the components took the longest time of this progress. Honestly, I was not sure about how far apart the components had to be, but I ended up eyeballing it, and it worked out. I followed the Keeb website regarding putting the diode on the right of the switches, and overall I felt like this part could’ve been optimized the most, but it still took me too long. Figuring out the wiring was not bad. I just copied how the Keeb’s examples looked, and it ended up looking pretty decent. The only thing that was quite difficult and took me quite a bit was figuring out how to wire some keys to the Pico, as there were wiring overlap issues, but it ended up working well. As for the design rule check, I only ended up with 3 issues, which I resolved quite quickly. 
PCB

![image alt](https://github.com/natehui0/nate-keeb/blob/3b72c3838103031ade60765d348505d58b7929e0/Screenshot%202026-09-14%20180927.png)


## Progress 4 — Creating the 3D Model

**September 10, 2026 — 5:00 PM–10:00 PM EDT**

I wanted to make a 3d model to import into Onshape so it's easier to design the case efficiently (this turned out to be a timely mistake (not really a mistake tho)). I was not sure what kind of switches to use. I ended up picking Cherry MX Red switches, but I couldn’t find any 3d models of them online. Luckily, Cherry switches are extremely similar to Gateron switches, so I ended up using 3d models provided from the Gateron website. It was extremely annoying to put each switch individually into each switch spot and ensure the pins of the switch were accurate relative to the pinholes. When I finished, I realized that I needed keycaps as well. I couldn’t find any real source that had a 3d model of keycaps. Luckily, on Reddit, there was a guy who designed keycaps (what a goat) and provided the STEP and STL files for it. Placing the keycaps accurately also took quite a while. Finally, I added 3d models of the screw-in stabilizers from the Gateron website. A slight issue was that the 3d model for the stabilizer didn’t work for the spacebar, so I went into Onshape to lengthen the support bar for the spacebar stabilizer. I was quite satisfied with the result, and I could see feasible results from this project.

3D Model

![image alt](https://github.com/natehui0/nate-keeb/blob/cdcc3f970cb1d8ffc97841481b7d620428d1d1a9/pcb-image.png)
![image alt](https://github.com/natehui0/nate-keeb/blob/cdcc3f970cb1d8ffc97841481b7d620428d1d1a9/keyboard-image-2.png)

## Progress 5 — Case Design

**September 11, 2026 — 8:00 AM–9:00 AM EDT**
**September 12, 2026 — 3:00 PM–5:00 PM EDT**
**September 13, 2026 — 10:00 PM–11:00 PM EDT**

While creating the case, I realized that the Pico wasn’t placed outward enough, so I had to create a larger hole to allow the USB cable to fit in. Overall, this step went the smoothest, as I had prior experience with Onshape. I decided to choose an integrated plate type of mounting (due to simplicity). Then I split the bottom and top into two parts to fit the 3d printing process. In the end, the most tedious process was creating the plate, as I had to create each individual square, which took a long time. In the end, I am extremely satisfied with the end result and am excited to see how it turns out.

Case

![image alt](https://github.com/natehui0/nate-keeb/blob/64aad61f469792b6b9a88adb46decc7ab656453c/images/Screenshot%202026-10-28%20012710.png)
    
## Progress 6 — 

**10/21/26 11 AM - 2 PM EDT**

I used Rust and RMK to help me create the code for the keyboard. I utilized other example projects listed in the KEEBS Slack and cross-referenced my code to theirs to ensure accuracy. This was my first time coding with Rust and using RMK, so it was kind of difficult learning the syntax for it, but overall, it went smoothly. 
Code

![image alt](https://github.com/natehui0/nate-keeb/blob/ee3830fa33cd0445370b799dee3dc28af3778705/Screenshot%202026-10-26%20014929.png)
![image alt](https://github.com/natehui0/nate-keeb/blob/ee3830fa33cd0445370b799dee3dc28af3778705/Screenshot%202026-10-26%20014922.png)


## Progress 7 — 

**10/27/26 11 PM - 10/28/26 2 AM EDT**

I fixed some issues that were apparent in my repository. I rewrote my README and journal. I also re-rendered my case with the PCB and switches, as I did not have a .step file for it. I still have more issues to fix, but I think I made some great progress today.

![image alt](https://github.com/natehui0/nate-keeb/blob/a267f609b57ab1e50978a479a7ad785d0c152ee4/images/Screenshot%202026-10-28%20015840.png)
![image alt](https://github.com/natehui0/nate-keeb/blob/64aad61f469792b6b9a88adb46decc7ab656453c/images/Screenshot%202026-10-28%20012710.png)
