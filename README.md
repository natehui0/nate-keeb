# nate-keeb
# Custom Mechanical Keyboard

A custom mechanical keyboard designed and built from scratch using **KiCad** and **Onshape**.

This project started as a way for me to learn more about PCB design, electronics, CAD, and mechanical keyboards. Rather than using an existing PCB or case, I'm designing the electronics and physical enclosure myself and documenting the process.

---

# Why I Built This

I've always been interested in mechanical keyboards, but I wanted to understand what actually goes into making one instead of just buying a pre-built keyboard or kit.

This project has turned into a crash course in **PCB design, electrical schematics, CAD, mechanical design, component sourcing, and manufacturing constraints**.

I'm also documenting the process as I learn. A lot of this project has involved following tutorials, making educated guesses, realizing I misunderstood something, and figuring it out along the way.

---

# Hardware

| Component            | Description                                   |
| -------------------- | --------------------------------------------- |
| Raspberry Pi Pico    | Microcontroller                               |
| Cherry MX Red        | Mechanical switches                           |
| Gateron 3D Models    | Used as a substitute for Cherry MX Red models |
| Screw-in Stabilizers | Used for larger keys                          |
| Keycaps              | 3D models used for CAD assembly               |
| 1N4148 Diodes        | Keyboard matrix                               |
| Custom PCB           | Designed in KiCad                             |
| 3D Printed Case      | Designed in Onshape                           |
| Integrated Plate     | Part of the case design                       |

---

# Software & Tools

* **KiCad** — Schematic and PCB design
* **Onshape** — 3D modeling and case design
* **GitHub** — Documentation and version control
* **KMK / Keyboard Firmware** — Planned firmware
* **3D Printing** — Case manufacturing

---

# Design Process

The project has gone through several stages, starting with an electrical schematic and eventually turning into a complete 3D model.

```text
Keyboard Layout
       ↓
KiCad Schematic
       ↓
PCB Design
       ↓
3D PCB Model
       ↓
Component Models
       ↓
Onshape Assembly
       ↓
Case Design
       ↓
Integrated Plate
       ↓
3D Printing
       ↓
Assembly & Testing
```

---

# Progress Log

## Progress 1 - Planning the Keyboard

**9/9/2026 4:00 - 4:50 PM EDT**

Found a simpleish design that I thought looked relatively nice and cool. This is for planning the keyboard. I also measured the size of the different keys. 1 = regular keys on a keyboard, 1.25 = slightly bigger keys (control, windows, etc), 1.5 = tab. 1.75 = (Caps lock, backspace, etc.), 2 = enter key, 2.25 = large shift, 6.25 = spacebar. This layout seems relatively easy to design.

## Progress 2 — Creating the Schematic

**September 9, 2026 — 5:00 PM–7:00 PM EDT**

I was half-lost when designing this PCB.

I followed the instructions on the Keeb website and ended up with the result shown below. The main difference I noticed was that the example on Keeb had the entire keyboard arranged in a grid, meaning the keys were essentially 1×1 or 1×2 and weren't laid out like a standard keyboard.

Because of this, I wasn't sure if the schematic itself needed to match the physical layout of the keyboard. I ended up playing it safe and designed the schematic to match the layout of the actual keyboard.

This was **extremely tedious**, since I constantly had to adjust the spacing between components to make the schematic resemble the physical keyboard.

I also wasn't sure whether the Raspberry Pi Pico needed to be within the grid, so I threw it at the bottom of the grid.

Another thing I wasn't sure about was which stabilizers were which.

Overall, this step taught me a lot about **KiCad** and how schematic design works. I'm looking forward to seeing how this design translates into the next stage.


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


## Progress 4 — Creating the 3D Model

**September 10, 2026 — 5:00 PM–10:00 PM EDT**

I wanted to make a 3D model of the keyboard and import it into Onshape so I could design the case more efficiently.

This turned out to be a pretty timely decision — although I wouldn't necessarily call it a mistake.

I wasn't sure what kind of switches I wanted to use. I ended up choosing **Cherry MX Red switches**, but I couldn't find any usable 3D models of them online.

Luckily, Cherry switches are extremely similar to Gateron switches, so I ended up using 3D models provided by Gateron.

The annoying part was placing each switch individually into its respective switch position and making sure the pins of each switch were accurately aligned with the pinholes on the PCB.

After I finished that, I realized that I needed keycaps as well.

I couldn't find a good source for a keycap 3D model, but luckily I found a Reddit user who had designed keycaps and provided both STEP and STL files.

**What a goat.**

Placing the keycaps accurately also took quite a while.

Finally, I added 3D models of the screw-in stabilizers from Gateron. There was a slight issue with the spacebar because the stabilizer model wasn't long enough.

I ended up opening the model in Onshape and lengthening the support bar for the spacebar stabilizer.

After everything was finally in place, I was pretty satisfied with the result. For the first time, I could actually see a feasible version of the finished keyboard.



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


# Challenges So Far

Some of the biggest challenges I've encountered throughout the project have been:

* Understanding how a schematic should correspond to the physical keyboard layout
* Figuring out component spacing and placement in KiCad
* Routing traces around the Raspberry Pi Pico
* Finding accurate 3D models for components
* Individually placing every switch and keycap
* Modifying the spacebar stabilizer model
* Designing the case around the Raspberry Pi Pico's USB port
* Creating an integrated plate while accounting for 3D printing constraints

---

# What I've Learned

### KiCad

* Creating electrical schematics
* Designing a keyboard matrix
* Component placement
* PCB routing
* Design Rule Checks
* Working with footprints and 3D models

### Onshape

* Importing STEP files
* Creating assemblies
* Positioning components
* Designing around existing hardware
* Modifying existing models
* Designing a 3D-printable case
* Creating an integrated plate

### Hardware Design

* How mechanical switches interact with a PCB
* Why diodes are used in keyboard matrices
* How a microcontroller connects to the keyboard matrix
* The importance of physical clearances
* Designing around USB access and manufacturing limitations

Most importantly, I've learned that **not knowing how to do something doesn't mean I can't figure it out.**

A lot of this project has been learning by doing, making mistakes, and figuring out why something didn't work.

---

# 🗓️ Timeline

| Date                  | Progress              |
| --------------------- | --------------------- |
| September 9, 2026     | Schematic             |
| September 10, 2026    | PCB layout & routing  |
| September 10, 2026    | 3D component modeling |
| September 11–13, 2026 | Case & plate design   |
