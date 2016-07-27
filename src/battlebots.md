# Battlebots
---

For [Robostorm](robostorm.md), we do a Lego battlebots competition at the 4-H fair every year. The objective is to push the other robot off the field. Although the battlebots are not required to be Lego, they must be under 3 lbs and must fit within the size limit.

## Java

**Autonomous Battlebot**

![Java Image](img/battlebot.png)

Although every other battlebot is human operated, I decided to be different and make a battlebot that is completely autonomous. It uses the Lego Mindstorms NXT for the brain, however it was not running the default firmware. I had installed the [Lejos](http://www.lejos.org/) firmware, which allowed me to program it in Java. This was an advantage over the default NXT-G language as it was more flexible and was easier to do more complex programming. The battlebot used two ultrasonic distance sensors on the front, one on each side, to detect the opponent and go towards it. It also had touch sensors on each side on the front to detect the edge of the field in order to avoid it. Furthermore, there was a bumper on the back that would cause it to reverse if it was getting pushed from behind. Surprisingly, it managed to get second place in one of the competitions.


## Poke

![Poke Image](img/battlebotside.jpg)

After a couple years of competing with autonomous battlebots, people started figuring out how to defeat them. As a result, I decided to go with a human operated design. Because many battlebots were using a large wedge on the front of their bot, I decided to create an 'anti-wedge' bot. The main principle was to be very long, with the driving wheels in the back. It would then be able to be lifted up on a wedge and still push. This realized itself in the form of a long pole at the front of the bot, that could also be raised up when not needed. Another key aspect of the design was to have most of the weight over the driving wheels for the maximum traction. Unfortunately, this resulted in being able to flip backwards easily. As a result, an arm on the back was added to be able to right the bot when it flipped backwards. It worked pretty good in competitions and proved to be popular among the audience, but it also proved to be a bit slow. Furthermore, I would forget to raise it back up after deploying it. If the bot was flipped while it was already deployed, there was no hope of recovery.
