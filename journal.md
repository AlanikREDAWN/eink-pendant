# eink pendant

## June 17 2026

### 11:15am - planning (10 mins)

Right now I'm trying to figure out how to make the idea that I have in my head. So, what I want to make is a eink-display cycler. It's going to have a small eink display, a keyswitch, some kind of neopixel LED (not sure what kind yet, I need to figure out what I'm actually capable of soldering), a lipo battery, and a Seeed Studio XIAO RP2040 microcontroller to control everything. 

The idea is that you press the keyswitch and it changes the color of the LED and cycles through different images on the eink display. 
I'm still trying to figure out how I can realistically make something like this without a guide though, considering that the only other pcb projects I've made have been with guides (adding my own stuff ofc, but still following a guide so I kind of know what I'm doing).

I'm thinking what I need to do is just open KiCad and start throwing stuff together, so that's what I think I'm going to do now

### 11:25am - throwing stuff into KiCad + researching (15 mins)

started putting together what I knew I could (switch to gnd and xiao), and researching what I didn't know (eink display)

**Throwing things into KiCad**

![<# alt text #>](screenshots/Screenshot%202026-06-17%20at%2011.34.26%E2%80%AFAM.png "Screenshot")

**eink research**

![<# alt text #>](screenshots/Screenshot%202026-06-17%20at%2011.38.52%E2%80%AFAM.png "Screenshot")

### 2:10pm - more KiCad + research (2 hours)

finding footprints to put into the schematic. I'm thinking of using the seeed studio ePaper Driver Board and just adding headers to it to make my life simple. I just need to add a footprint to use in KiCad for it.

I'm proabably just gonna use a generic connector and modify it a bit to match the pins.

**Custom generic connector**

![<# alt text #>](screenshots/Screenshot%202026-06-17%20at%202.30.27%E2%80%AFPM.png "Screenshot")

**finished wiring driver board**

![<# alt text #>](screenshots/Screenshot%202026-06-17%20at%203.14.59%E2%80%AFPM.png "Screenshot")

**finished wiring through-hole neopixel - gonna start with one for now and add more if they fit**

![<# alt text #>](screenshots/Screenshot%202026-06-17%20at%203.16.21%E2%80%AFPM.png "Screenshot")

**final schematic (for now at least)**

![<# alt text #>](screenshots/Screenshot%202026-06-17%20at%203.22.27%E2%80%AFPM.png "Screenshot")

nvm, that one was not final...I had to tweak my custom driver board connector and break it into two connectors so I have more control when positioning the holes on the pcb

annddd it turns out I also forgot to think about any resistors and capactiors I might need. Apparently (according to google - yes google...do you really think I already know what I'm doing?) its a good idea to include them for the neopixel

**hopefully the final schematic**

![<# alt text #>](screenshots/Screenshot%202026-06-17%20at%203.59.23%E2%80%AFPM.png "Screenshot")

### 4:45pm - pcb layout (20 mins)

working on laying out the components on the pcb editor

**the layout so far**

![<# alt text #>](screenshots/Screenshot%202026-06-17%20at%204.58.42%E2%80%AFPM.png "Screenshot")

### 5:05pm - importing 3d models (10 mins)

working on getting and importing 3d models for the rendering

## June 18 2026

### 1:10pm - importing 3d models + pcb design (2 hours, 20 mins)

continuing to work on getting 3d models so I can see how things will fit before wiring

**adding custom driver 3d model on existing header 3d models**

![<# alt text #>](screenshots/Screenshot%202026-06-18%20at%201.16.11%E2%80%AFPM.png "Screenshot")

now I'm trying to figure out why one of my driver headers doesn't have any connections in the pcb panel

turns out the issue was becuase I renumbered the pins, I just had to revert them and they were fine

**3d model so far**

![<# alt text #>](screenshots/Screenshot%202026-06-18%20at%202.51.50%E2%80%AFPM.png "Screenshot")

**more progress! I still need to figure out how to fit in the lipo battery and eink display. they're not soldered to the board, but they're plugged into the driver**

![<# alt text #>](screenshots/Screenshot%202026-06-18%20at%203.05.29%E2%80%AFPM.png "Screenshot")

**I think I finally figured out an ideal layout to fit everything, so now its time to start wiring**

![<# alt text #>](screenshots/Screenshot%202026-06-18%20at%203.16.53%E2%80%AFPM.png "Screenshot")

**starting to wire**

![<# alt text #>](screenshots/Screenshot%202026-06-18%20at%203.25.13%E2%80%AFPM.png "Screenshot")

after a little bit of wiring, I realized that there was something wrong with the 5V connections on the led...they weren't even connected to the microcontroller!

### 4:50pm - wiring pcb (45 mins)

after asking for a sanity check on my schematic, I decided to work on the case while I waited

well, turns out I didn't even need that capacitor...google was misleading.

**this is how the schematic looks after making those small fixes**

![<# alt text #>](screenshots/Screenshot%202026-06-18%20at%205.17.27%E2%80%AFPM.png "Screenshot")

**the final wired pcb! (hopefully)**

![<# alt text #>](screenshots/Screenshot%202026-06-18%20at%205.25.49%E2%80%AFPM.png "Screenshot")

### 5:45pm - modeling case (30 mins)

now is the part where I struggle to model a case in fusion360 ToT

**getting the base rectangle in for the case**

![<# alt text #>](screenshots/Screenshot%202026-06-18%20at%206.02.17%E2%80%AFPM.png "Screenshot")

## June 19 2026

### 7:45am - the final stretch

I got up early this morning to finish modeling the case and finish all the things I need to do to submit (like putting together the BOM and throwing all the files into the repo)

**the case is almost done! I just need to add a keyring**

![<# alt text #>](screenshots/Screenshot%202026-06-19%20at%208.09.14%E2%80%AFAM.png "Screenshot")

**the case is done! (at least, until I get the PCB and potentially decide to make changes)**

![<# alt text #>](screenshots/Screenshot%202026-06-19%20at%208.15.23%E2%80%AFAM.png "Screenshot")

now to shop for parts and put everything in the GitHub repo