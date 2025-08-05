# MechaGrip: Log

| Builder | Chandan                    |
|---------|-----------------------------|
| Project | MechaGrip - Robotic Arm     |
| Total Hours | 21.5 hours                 |

---

## MechaGrip 
### July 10th finding the best motor for my roboarm
So, I spent the early hours of July 10th completely immersed in servo and stepper motor charts. I won't lie, it was a lot. I looked at more than 30 different sources, including YouTube videos, Reddit threads, very niche forums, and a lot of datasheets that were honestly way too complicated. At that point, I was pretty much on a mission.After hours of looking at specs and going down random internet rabbit holes, I finally decided on the motors I wanted to use. The one I chose can handle about 9.4 kg/cm of torque, which is more than enough for what I'm making right now. But this whole thing did take a lot of work, which was surprising. It seems like a small choice on paper, but it took me all morning to figure it out through trial and error and brain fog. I might change the motor setup later, but for now, this works great. Putting a picture of the motor below for context.

time spent: 3 hours

| Image | Description |
|-------|-------------|
| <img width="858" height="700" alt="Screenshot 2025-07-19 172028" src="https://github.com/user-attachments/assets/73d27a61-aa55-4db9-bd4d-110594410c07" /> | MG996R Servo Motors i finally settled on. Decent torque, clean threads, good vibe. |

---

### July 11th designing the disc and checking compatibilty  
So, July 11th was a total mess.  I began making the disc for the motors, which is basically the part that connects the robot's chassis to the motor shaft.  It should have been easy, but it wasn't.  Fusion 360 chose to be dramatic.  My constraints kept messing up, the geometry wouldn't line up, and everything just seemed wrong.
I got so mad after an hour of trying to fix it that I just deleted everything and started over.  To be honest, it was for the best.  I was finally getting somewhere. until I somehow deleted the STEP file for the disc model by mistake.  Also, I had emptied the recycle bin earlier, which was smart of me.
I briefly believed I had lost everything. However, it turned out that I had already imported it into Fusion, so I wasn't totally lost. That little heart attack was still unpleasant. For such a basic component, the disc required a surprisingly high amount of work, but since it serves as the actual basis for the bot's movement, it had to be sturdy.

Time spent: 2 hours

| Image | Description |
|-------|-------------|
| <img width="913" height="311" alt="Screenshot 2025-07-19 172128" src="https://github.com/user-attachments/assets/29d06812-b7d7-405b-9453-657620930761" /> | That disc finally aligned with the shaft. Minor win, major relief. |

---

### July 12th Base 
I began working on the robot's base, which I assumed would be a cool component, early on July 12. It was much more annoying than I had anticipated. I continued experimenting with various shapes, including squares, triangles, and even an odd polygon, but none of them really blended in with the bot's overall design. Each shape either looked totally out of place or interfered with the wheel positioning. I had a "duh" moment after several unsuccessful attempts and a lot of intense screen staring. I now know why the circular base is the original and most likely the best option.The design simply... functions. It provides nice symmetry, fluid movement, and doesn't struggle with CAD like other designs do. So, yes, I went classic instead of using all the strange shapes. It is now prepared for a proper render after I cleaned it up and added my mounting points.
Although it may have taken longer than anticipated, I'm quite pleased with the final base.


Time spent: 2.5 hours

| Image | Description |
|-------|-------------|
| <img width="873" height="729" alt="Screenshot 2025-07-19 172345" src="https://github.com/user-attachments/assets/f0220d44-a904-4f76-b753-fdef0eabd94e" /> | MechaGrip’s base  six-sided, balanced. |

---

### July 13th Desighned the gripper
On July 13th, I woke up and immediately started working on the robotic arm's gripper. The objective was fairly simple: I only needed something sturdy enough to support a few boards or my solder parts, nothing too fancy. I just wanted something that works; I wasn't going for industrial precision or anything.
Since flat is boring, I decided on a zigzag design and added one of the servos to make it more dynamic. Unexpectedly, this was most likely the simplest aspect of building the entire robot. Yes, it took a while, but only because I overdid the details, making sure it was neat, balanced, and not a hastily drawn-out afterthought.
But in a functional sense? It's flawless. It doesn't slip, grabs what it needs to, and it looks kind of cool. I'm genuinely pleased with how this section turned out.

time spent: 3 hours

| Image | Description |
|-------|-------------|
| <img width="1171" height="940" alt="Screenshot 2025-07-19 172533" src="https://github.com/user-attachments/assets/b7577e61-5f1c-4d8c-84d3-ab9aeccafa0f" /> | The claw. The grip. The grabber. Might open cans or crush dreams. |

---

### July 14th made the elbow bends
Okay, so July 14th was the day for elbow bends. It kept clipping into the other arm like two hostile toddlers vying for space while I was working on the joints, you know, the flexible portion of the robot arm. Despite the mess, I was able to fix it more quickly than anticipated. Constraints turned out to be the true villain. The motion was totally messed up when I tried to add a fillet on a side that already had two or more constraints. The elbows were clean and worked like butter after I finally figured it out, though it took some time.

What I discovered:
How to utilize the fillet tool effectively without destroying the entire model

time spent: 2 hours

---

### July 15th Shoulder building
I started working on the shoulders of the robot arm, and I was amazed at how slim it was.   Like a skinny, undernourished action figure.   I didn't want a robot that was meant to be tough to have that vibe.used the traditional trial-and-error method to try a number of measurements until it stopped looking like garbage. Nothing felt right for a long time. But I kept tweaking it until it looked respectable. As though it could hold things without shattering.


  Without being unduly intricate, it was thickened and given a crisper shape.   Much better than what I started with.

Time spent: 3 hours

| Image | Description |
|-------|-------------|
| <img width="448" height="697" alt="Screenshot 2025-07-19 172724" src="https://github.com/user-attachments/assets/a99214c3-581e-4491-a039-49ca47c0b93b" /> | Shoulders carry a lot  and this one’s ready. Hollow, lightweight, strong. |

---

### July 16th made the bom and attached render pics  
I worked mostly on the robotic arm's Bill of Materials (BOM) today. In order to prevent needless purchases, I began by examining my current electronics inventory. Although it took some time, this contributed to the overall cost savings.To keep the build within my means, I also took the time to source parts and compare costs. The final list cost about $100, which is a lot less than most similar robotic arm builds.In addition, I worked on rendering the robot's current model. The render looks good and shows the development thus far.

time spent: 2.5 hrs

| Image | Description |
|-------|-------------|
| <img width="626" height="1065" alt="Screenshot 2025-07-19 173041" src="https://github.com/user-attachments/assets/bff52ffd-d78b-4408-8a36-811785ed079c" /> | Final render of MechaGrip  before the real cuts begin. Time to build. |

---

### July 17th made the firmware of the robot
Today, I began writing the firmware for the robotic arm. The objective was to implement basic servo motor control using the Arduino Servo.h library.
I set up a simple sketch to control multiple servos, check their angles, and guarantee smooth motion. At first, jitter and unresponsive servos were minor issues that were fixed by carefully allocating PWM pins and modifying the delay values.

time spent: 1.5 hours

---

