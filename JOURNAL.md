# Progress Log

## Progress 1 - Planning the Keyboard

**9/9/2026 4:00 - 4:50 PM EDT**

Found a simpleish design that I thought looked relatively nice and cool. This is for planning the keyboard. I also measured the size of the different keys. 1 = regular keys on a keyboard, 1.25 = slightly bigger keys (control, windows, etc), 1.5 = tab. 1.75 = (Caps lock, backspace, etc.), 2 = enter key, 2.25 = large shift, 6.25 = spacebar. This layout seems relatively easy to design.

Keyboard Design

![image alt](https://github.com/natehui0/nate-keeb/blob/cdcc3f970cb1d8ffc97841481b7d620428d1d1a9/keyboard-layout-2.png)

## Progress 2 — Creating the Schematic

**September 9, 2026 — 5:00 PM–7:00 PM EDT**

I was half-lost when designing this PCB.

I followed the instructions on the Keeb website and ended up with the result shown below. The main difference I noticed was that the example on Keeb had the entire keyboard arranged in a grid, meaning the keys were essentially 1×1 or 1×2 and weren't laid out like a standard keyboard.

Because of this, I wasn't sure if the schematic itself needed to match the physical layout of the keyboard. I ended up playing it safe and designed the schematic to match the layout of the actual keyboard.

This was **extremely tedious**, since I constantly had to adjust the spacing between components to make the schematic resemble the physical keyboard.

I also wasn't sure whether the Raspberry Pi Pico needed to be within the grid, so I threw it at the bottom of the grid.

Another thing I wasn't sure about was which stabilizers were which.

Overall, this step taught me a lot about **KiCad** and how schematic design works. I'm looking forward to seeing how this design translates into the next stage.

Schematic

![image alt](https://github.com/natehui0/nate-keeb/blob/d9eb6e57f53638d1765ce57265051df7d152bb8b/keyboard-design-layout-pcb.png)

## Progress 3 — PCB Layout & Routing

**September 10, 2026 — 6:00 AM–10:00 AM EDT**

Arranging the components took the longest time during this stage.

Honestly, I wasn't sure how far apart the components needed to be, so I ended up eyeballing it. Somehow, it worked out.

I followed the Keeb website's example and placed the diodes to the right of the switches. Overall, I felt like this part could have been optimized the most, but it still took me way too long.

### Wiring

Figuring out the wiring wasn't too bad. I mostly copied how the Keeb examples looked, and it ended up looking pretty decent.

The part that gave me the most trouble was figuring out how to wire some of the keys to the Raspberry Pi Pico. I ran into several wiring overlap issues, which meant I had to move things around and figure out different routing paths.

Eventually, I got everything connected and it worked out well.

### Design Rule Check

For the Design Rule Check, I only ended up with **3 issues**, which I was able to resolve pretty quickly.

At this point, I finally had a PCB design that looked like an actual keyboard.

PCB

![image alt](https://github.com/natehui0/nate-keeb/blob/3b72c3838103031ade60765d348505d58b7929e0/Screenshot%202026-09-14%20180927.png)


## Progress 4 — Creating the 3D Model

**September 10, 2026 — 5:00 PM–10:00 PM EDT**

I wanted to make a 3D model of the keyboard and import it into Onshape so I could design the case more efficiently.

This turned out to be a pretty timely decision, although I wouldn't necessarily call it a mistake.

I wasn't sure what kind of switches I wanted to use. I ended up choosing **Cherry MX Red switches**, but I couldn't find any usable 3D models of them online.

Luckily, Cherry switches are extremely similar to Gateron switches, so I ended up using 3D models provided by Gateron.

The annoying part was placing each switch individually into its respective switch position and making sure the pins of each switch were accurately aligned with the pinholes on the PCB.

After I finished that, I realized that I needed keycaps as well.

I couldn't find a good source for a keycap 3D model, but luckily I found a Reddit user who had designed keycaps and provided both STEP and STL files.

**Nice.**

Placing the keycaps accurately also took quite a while.

Finally, I added 3D models of the screw-in stabilizers from Gateron. There was a slight issue with the spacebar because the stabilizer model wasn't long enough.

I ended up opening the model in Onshape and lengthening the support bar for the spacebar stabilizer.

After everything was finally in place, I was pretty satisfied with the result. For the first time, I could actually see a feasible version of the finished keyboard.

3D Model

![image alt](https://github.com/natehui0/nate-keeb/blob/cdcc3f970cb1d8ffc97841481b7d620428d1d1a9/pcb-image.png)
![image alt](https://github.com/natehui0/nate-keeb/blob/cdcc3f970cb1d8ffc97841481b7d620428d1d1a9/keyboard-image-2.png)

## Progress 5 — Case Design

**September 11, 2026 — 8:00 AM–9:00 AM EDT**
**September 12, 2026 — 3:00 PM–5:00 PM EDT**
**September 13, 2026 — 10:00 PM–11:00 PM EDT**

While creating the case, I realized that the Raspberry Pi Pico wasn't placed far enough outward, so I had to create a larger opening to allow the USB cable to fit.

Overall, this step went the smoothest because I already had prior experience with Onshape.

I decided to use an **integrated plate mounting design** because of its simplicity.

I then split the bottom and top of the case into two separate parts to make the design more practical for the 3D printing process.

### Plate

The most tedious part of this stage was creating the plate.

I had to create each individual square for the switches, which took a long time. It wasn't necessarily difficult, but there was a lot of repetitive work involved.

Eventually, everything came together.

I'm extremely satisfied with the end result, and it's exciting to finally have a complete case design that I can actually print and turn into a physical keyboard.

Case

![image alt](https://github.com/natehui0/nate-keeb/blob/cdcc3f970cb1d8ffc97841481b7d620428d1d1a9/Screenshot%202026-09-13%20234251.png)
![image alt](https://github.com/natehui0/nate-keeb/blob/cdcc3f970cb1d8ffc97841481b7d620428d1d1a9/Screenshot%202026-09-10%20002551.png)
    
## Progress 6 — 

**10/21/26 11 AM - 2 PM EDT**

I used Rust and rmKit to help me create the code for the keyboard. 

I utilized other example projects listed in the KEEBS Slack and cross-referenced my code to theirs to ensure accuracy. 

This was my first time coding with Rust and using rmKit, so it was kind of difficult learning the syntax for it, but overall, it went smoothly. 

Also fixed missing items in this time period.

Code

![image alt](https://github.com/natehui0/nate-keeb/blob/ee3830fa33cd0445370b799dee3dc28af3778705/Screenshot%202026-10-26%20014929.png)
![image alt](https://github.com/natehui0/nate-keeb/blob/ee3830fa33cd0445370b799dee3dc28af3778705/Screenshot%202026-10-26%20014922.png)

