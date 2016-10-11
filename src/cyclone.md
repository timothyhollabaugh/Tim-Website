# Cylcone PCB Mill
---

[!Picture of Cyclone](img/cyclone.jpg)

I have been making circuit boards using the toner transfer and etching acid method since I was a kid, and I had always despised it. The process was long, messy, and error prone. Since I had gotten my [3d printer](printer.md), I had always wanted to add a Dremel to mill the copper off a circuit board. I acually tried this, and it seemed to work, but I did not have any real bits to use. After this initial sucess, I decided to build a dedicated machine for pcb milling. I did some searching, and found the [Cyclone PCB Factory](https://github.com/CarlosGS/Cyclone-PCB-Factory) on GitHub. It used a Dremel for the spindle, and most of the frame was 3d printed.

The one thing I did not like about it was that it could only hold one size PCB in the clamps. I fixed this issue in [my fork](https://github.com/chickenchuck040/Cyclone-PCB-Factory) that adds a 3d printed workbed with holes every 20mm. There is an inset for a nut at the bottom of each hole, and I tapped them all to M3. That allows the screwing down of smaller clamps to hold smaller boards, or screwing the boards directly to be bed.

After coinvincing my dad to order the parts, the assembly went relativly quickly. The only issue I had was getting the frame square, for which I modified some of the parts to have slots for screws to make alignment easier. I also decided to make my own control board to run the opensource CNC firmware [grbl](https://github.com/grbl/grbl). It is made to run on an Arduino UNO, but I did not have any UNOs around. However, I did happen to have some atmega328s around, the microprocessor that the UNO uses. I decided to make my own control PCB using the toner transfer method, integrating the atmega, stepper controllers, and voltage regulator on one board. I first made the circuit on a breadboard, to ensure that everthing would work as it should.

[!Image of the breadboard](img/cyclone-breadboard.jpg)

After some issues with blowing stepper drivers (They don't like to be powered with not stepper attached!), I went ahead and made the control PCB. After etching it, I decided that the mill was working well enough on the breadboard to drill all the holes in the board. Lining up the already etched board with the workbed was a pain, but in the end, it worked. It was the first real milling that it had done, and it worked great. I put all the components in the board, and there were no issues. After mounting it, the next step was to try some acual isolation milling.

[!Image of the control board](img/cyclone-control.jpg)

After some initial calibration to figure out the milling depth and width, I was ready to try my first board. It was a breakout for the Raspberry Pi on my 3d printer, to replace a perfboard that I have made earlier. All it had to do was combine power, some GPIOs, USB and audio into a 9 pin serial connector to interface with the printer. My setup before had worked, but it was a bit fluky, and needed to be replaced. The board was good for a test, as it was small, and there was nothing particularly difficult. I used 1mm traces to ensure that even if the Dremel cut too wide, it would still work. it turned out to work just fine, and is now serving its duty on the printer.

[!Image of the first PCB](img/cyclone-firstpcb.jpg) 
