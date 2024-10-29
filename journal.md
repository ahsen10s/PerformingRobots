# Journal: Ahsen and Pranav

## 29 October 2024
**Peacock Tail Iteration 1**

![Attach servo](/journal_assets/tail_sketch1.jpeg)
First sketched out how we would build Mrs.Peacock's tail. Its structure was held up with three wooden beams. One beem would be drilled into the foundation behind the robot to hold the tail up. The other two beams would be held by two servors planted on either sides of the central beam. The three beams would be dressed in fabric of peacock colors. When triggered, the two servons would turn in opposite directions, moving the beams with them, thereby opening up Mrs.Peacock's 'tail'. This constitutes the main tail mechanism.


![Attach servo](/journal_assets/25kg_servo.jpeg)
Next we attached the servo to the Arduino Uno. We only possessed one 25kg servo at this time. We tried to match the same color scheme with wires.
After, we coded the expected movement into the arduino. This required mapping the range, as well as setting the min and max angle.


`#include <Servo.h>`

`Servo Servo1;`

`int servoPin = 9;`

`int commandGiven = 0;`

`void setup() {`

`  Servo1.attach(servoPin);`

`}`

`void loop() {`

`  // The resting angle (hiding behind the robot)`

`  int angle = 96; //tested precise angle`

`  // Code to be updated as we progress with the functionality`

`  commandGiven = 1; //this will be changed, as of now it's being hardcoded for testing purposes`

`  if (commandGiven == 1) {`

`    angle = 30;`

`  }`

`  // Mapping the angle we want (because the servo has a wider angle than a usual servo)`

`  int mappedAngle = map(angle, 0, 270, 0, 180);`

`  // Write the mapped angle to the servo`

`  Servo1.write(mappedAngle);`

`  delay(1000); // Add a delay for stability`

`}`


![Attach servo](/journal_assets/servo_drilled.jpeg)
Next we drilled a beam of appropriate length onto this servo. We chose wood for its lightness. All it had to support was fabric and its own weight, so wood seemed to be the best material.

**Video:**

[![half_tail](https://img.youtube.com/vi/mMwDYpOA7Ys/0.jpg)](https://youtube.com/shorts/mMwDYpOA7Ys)

## 24 October 2024
**Sketch 2.0 for robot mechanism**
All the details can be found in Pranav's journal [here](https://github.com/sripranav9/PerformingRobots/blob/main/journal.md#24-october-2024)

## 1 October 2024
**Presentation 1 question**

Why are we so obsessed with mimicking human realism with robots? Humans already exist. Would it not be better to explore themes only robots perform? Our obsession with anthropomorphising touches all we do.

**Presentation 2 question**

Toomie said that people's initial response from seeing the ultra realistic robot, was worry and unease. They got more relaxed after spending some time with it. Could it be that they were tense at first from seeing it mimic humans so closely and gradually relaxed after seeing it fail to talk exactly like humans? Are we instinctually afraid of being copied by something not us?


## 26 September 2024
**Continuing building the base of our robot**
All the details can be found in Pranav's journal [here](https://github.com/sripranav9/PerformingRobots/blob/main/journal.md#26-september-2024)


## 22 September 2024

### Robot Foundation
![unnamed](/journal_assets/robot_foundation1.jpeg)
![unnamed](/journal_assets/robot_foundation2.jpeg)
![unnamed](/journal_assets/robot_foundation3.jpeg)

In class, we started building the foundation of our performing robot. Pranav and I went with the standard 2 motorized set-up recommended in class. We first sauldered single-core wires to our two servos to have longer cables to work with. Next, we picked out a wooden foundation to build Mrs.Peacock on, and got to puting our mounts, motors, and wheels together. We drilled the motors on opposing sides of the square foundation, center each of each side. To keep the plaque balanced, we drilled a free-spinning wheel on the adjacent side.

However, we will likely have to redo the free-spinning wheel, since we did not adjust for the added height of the larger motorized wheel. Perhaps we shall drill a small wooden block to the underside of our foundation, which we will then use to drill the free-spinning wheel into.


## 17 September 2024 (edited on 18th)

### Initial Thoughts
For this play, above all else, I want to create a memorable character. One that, by the end of the play, teh audience will leave with a clear. complete picture off. With the play runtime being 20 minutes, each character will get roughly two and a half minutes to speak and establish their character. Given the limitation, as well as the inherent clunkiness of having robot actors, my robot will have to have an extreme personality and voice to grab the audience's attention. While subtle nuances in character development is always appreciated in theatre, our compact play is perhaps not the best venue for that.

### Character
We chose Mrs.Peacock.
“Character description (Open for change) - Mrs. Peacock is the wife of an unidentified Senator. She has been taking bribes for an undisclosed amount of time, though she winds up paying some of that money to Mr. Boddy, who discovered her secret thanks to the cook they share. She murders said cook in two of the versions, and in one, she murders every single person because that’s what vindictive old women who think they’re better than everyone else do.

Quality Of Character: It’s all about the sighs with Mrs. Peacock, as handled by Eileen Brennan. She’s great at expressing disapproval without using real words to do it. She’s of that not rare enough breed who thinks her own sins are completely legitimate but those of others are immoral, offensive and scuzzy. This leads to some pretty defensive comments about her own bribe-taking and some pretty offensive statements and mean-spirited looks about things like homosexuality, prostitution and murder.”
[source](https://www.cinemablend.com/new/Every-Single-Character-Clue-Ordered-By-Greatness-40549.html)

### Sketch
![unnamed](/journal_assets/mrs.peacock_v1.jpeg)












