# Journal: Ahsen and Pranav

## 26 November 2024
**Level 2 Foundation**

![Constume](/journal_assets/costume_skirt.jpg)

With the help of the Equipment center, we went to the costume shop to look for gown/skirts and accessories for Mrs.Peacock. We found two skirts that coincientally worked well together. One was white and plain while the other was a light pink, layered and see through. When put over the other, their colors and texture complimented eachother so we decided to use both. This will cover the legs of the lvl 2 foundation.

![Fortify body](/journal_assets/fortify_body.jpg)

We laser cut the layers of Mrs.Peacock's body one by one. The maximum dimension the laser cutter could handle was 80cmx50cm, so we cut as big as we could. For the central layer we cut two identical pieces that we stuck together for greater structure integrity. This is the piece that would support all the other layers and it would be the only layer mounted to the lvl 2 foundations (using 6 L brackets to spread out the pressure on the base of the cardboard) so it needed to be reliably strong. We also inserted several wooden skweres into the cardboard to fortify it along its weaker axis. The last thing we want is for it to bend under the weight of the other layers it would support. Furthermore, we did not have any more cardboard to laser cut a piece as big as the central layer, so we moved as cautiously as we could.

![join body](/journal_assets/hot_glue_body.jpg)

We drilled 3 holes through all the body layers and 2 holes through the face layers, and pushed wooden skewers through them. Next we hot glued all the pieces in place to maintain the illusion of a 3D peacock body. 

![Tail fabric](/journal_assets/hot_glue_body_2.jpg)

We also cut and stapled the fabrics we procured onto the tail. The more time consuming part of this step was deciding on the fabrics we wanted. We also asked many classmates and students in the IM lab for their thoughts on how the tail should look. The above picture is the design we settled on.


![Constume](/journal_assets/costume_skirt.jpg)

With the help of the Equipment center, we went to the costume shop to look for gown/skirts and accessories for Mrs.Peacock. We found two skirts that coincientally worked well together. One was white and plain while the other was a light pink, layered and see through. When put over the other, their colors and texture complimented eachother so we decided to use both. This will cover the legs of the lvl 2 foundation.

## 19 November 2024
**Level 2 Foundation**

![Fabrics](/journal_assets/fabric.jpg)

We also were able to procure fabrics from the Textile studio with the help of Tucker. We looked for designs, colors, and textures that would complement Mrs. Peacocks body and tail. As she is a loud and prideful character, we opted for loud, vibrant colors to be an extension of her personality.


![mount tail](/journal_assets/mount_tail.jpg)

Next we mounted our the tail components and Arduino Mega to the the lvl 2 foundation. We also tested the tail mechanism to find the appropriate angles for the servos to 'open' and 'close' the tail.

## 12 November 2024
**Body Designing and Level 2 Foundation**

![Body design](/journal_assets/design_body.jpg)

We created layers for the peacock body on illustrator. By describing type of peacock profile we were looking for to co-pilot LLM, we were able to get an image drawing we could work with. We then imported this into illustrator and converted it into vector. We then polished it to fit what we had in mind of Mrs.peacock and for practicality (like a longer neck and flat base to ease its mounting to the foundation). Once we had a central piece we were ready with, we then worked on the progressively smaller pieces that would give Mrs.peacock a 3D body when spaced horizontally next to each other. We also incorporated feather and wing details to the outermost layers. Once we were happy with the design, we laser cut the central layer to see how it looks on the newly built lvl 2 foundation.

![lvl 2 foundation](/journal_assets/foundation&prototype.jpg)

This weekend we worked on creating a second foundation for Mrs.Peacock. This is where we envision Mrs.peacock's body and tail will be mounted to. Since the dimensions of the body we will design is limited to the maximum size the laser cutter can hold, we must construct the foundation height somewhat proportionally. The foundation is help up and attached to 2 wooden rods using two L brackets for each of the 2 rods, both at the base and the top. If it is not stable, we may consider adding another leg.



## 5 November 2024
**Peacock Tail Iteration 2**

![two rod for tail](/journal_assets/two_tail.jpg)
We duplicated what we did last weekend to create the second rod for the other half of the tail. We now have the two moving components of the tail. Our next step would be to create a mount a central beam along with these two moving rods set the backbone of the tail.

![Solder shield](/journal_assets/solder_shield.jpg)
We also soldered the shield for the Arduino Mega as instructed in class and github. Moving forward, we hope to test our peacock tail code once we plug it into the newly recieved mega.

## 29 October 2024
**Peacock Tail Iteration 1**

![Attach servo](/journal_assets/tail_sketch1.jpeg)
First sketched out how we would build Mrs.Peacock's tail. Its structure was held up with three wooden beams. One beem would be drilled into the foundation behind the robot to hold the tail up. The other two beams would be held by two servors planted on either sides of the central beam. The three beams would be dressed in fabric of peacock colors. When triggered, the two servons would turn in opposite directions, moving the beams with them, thereby opening up Mrs.Peacock's 'tail'. This constitutes the main tail mechanism.


![Attach servo](/journal_assets/25kg_servo.jpeg)
Next we attached the servo to the Arduino Uno. We only possessed one 25kg servo at this time. We tried to match the same color scheme with wires.
After, we coded the expected movement into the arduino. This required mapping the range, as well as setting the min and max angle.


```

// Code for the left servo

#include <Servo.h>

Servo Servo1;

int servoPin = 9;
int commandGiven = 0;

void setup() {

  Servo1.attach(servoPin);
}

void loop() {
  // The resting angle (hiding behind the robot)
  int angle = 96; //tested precise angle

  // Code to be updated as we progress with the functionality
  commandGiven = 1; //this will be changed, as of now it's being hardcoded for testing purposes
  if (commandGiven == 1) {
    angle = 30;
  }

  // Mapping the angle we want (because the servo has a wider angle than a usual servo)
  int mappedAngle = map(angle, 0, 270, 0, 180);

  // Write the mapped angle to the servo
  Servo1.write(mappedAngle);

  delay(1000); // Add a delay for stability
}

```



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












