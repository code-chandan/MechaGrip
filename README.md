# MechaGrip

MechaGrip is a 4-axis robotic arm that’s kinda like if a CNC machine, a 3D printer, and a drunk claw machine had a kid except this one actually works. It’s made for light pick-and-place tasks, gesture control experiments, or just for flexing on your desk next to your keyboard. It runs on a basic Arduino setup but doesn’t feel basic at all. The servos aren’t those $2 ones that jitter like they’re having a seizure   we went with beefy MG996Rs and a proper control board. It moves smoothly, holds position like a champ, and doesn’t scream (too loudly) when you power it up.

It’s built from a mix of laser-cut acrylic and 3D printed parts no CNC required. Just print, bolt, wire, upload, and flex.

<img width="365" height="509" alt="image" src="https://github.com/user-attachments/assets/430a393c-23b0-4402-b01a-bebf1a17a502" />


---

## What it can do

- Controlled via joystick or sliders, or you can go full nerd and make it run from Python or serial commands
- Decent strength it won’t lift bricks but a screwdriver or can of Red Bull? Easy.
- Compact enough to sit on a table without feeling like it’s invading your space
- Fully open source so you can mod the hell out of it

---

## Build Details

The arm has 4 degrees of freedom (base, shoulder, elbow, gripper) and is powered by 4x MG996R high-torque metal gear servos. The body is mostly acrylic plates and some 3D printed joints. We used a PCA9685 servo driver so your Arduino doesn’t get cooked by current draw.

Wiring is simple, most of the mess is cable management. We zip-tied ours. You can be classier if you want.

---

## Bill of Materials (BOM)

| Item                      | Qty | Unit Price | Total  | Link                                                 |
|---------------------------|-----|------------|--------|------------------------------------------------------|
| MG996R Servo Motors       | 4   | $8.00      | $32.00 | [Amazon](https://www.amazon.in/Robocraze-MG996R-TowerPro-Servo-Motor/dp/B08F7678YH?source=ps-sl-shoppingads-lpcontext&ref_=fplfs&smid=A1B5UBSQH24ZDS&th=1)
| PCA9685 Servo Driver      | 1   | $14.95      | $14.95  | [Adafruit](https://www.adafruit.com/product/815)     |
| Arduino UNO R3           | 1   | $25.00     | $25.00 | [Robocraze](https://robocraze.com/products/official-arduino-nano-matter-with-headers?variant=47315643498720&country=IN&currency=INR&utm_medium=product_sync&utm_source=google&utm_content=sag_organic&utm_campaign=sag_organic&utm_source=google&utm_medium=cpc&utm_campaign=BL+%7C+Pmax+%7C+Feed+Only+%7C+Arduino+%26+Compatible+%7C+12%2F06&utm_source=googleads&utm_medium=ppc&utm_campaign=21377571572&utm_content=_&utm_term=&campaignid=21377571572&adgroupid=&campaign=21377571572&gad_source=1&gad_campaignid=21381661351&gbraid=0AAAAADgHQvZjgTBitAxxubPiI02yWKT0_&gclid=Cj0KCQjwhO3DBhDkARIsANxrhTpXrLs1esHQ1z7r-NAyG1RpxpDxpgtMRdddGJnQG8DH2xughz5pxskaAkW_EALw_wcB) |
| M3 Nuts & Bolts Assorted  | 1   | $5         | $5 | [Amazon](https://robu.in/product/pro-range-120pcs-m3-hexagon-copper-pillar-screw-kit/?gad_source=1&gad_campaignid=20387462343&gbraid=0AAAAADvLFWdyq8-oO6LCqonOg3rZc1pmc&gclid=Cj0KCQjwhO3DBhDkARIsANxrhTp1n4thZauUkX5pc6z7l_rgFNzQCKDRJ47aisyZkDi2tdvtR-lEYAkaAnlOEALw_wcB)       |
| SG90 Servo (Gripper)      | 1   | $4.00      | $4.00  | [Amazon](https://www.amazon.com/dp/B07CZ3T31B)       |
| 5V 3A Power Supply        | 1   | $10.00     | $10.00 | [Amazon](https://adapterkart.com/products/hi-lite-essentials-20v-3a-power-adapter-for-sony-speaker-adapter-ac-yjs060k-sa-100-speakers?variant=48295051559233&country=IN&currency=INR&utm_medium=product_sync&utm_source=google&utm_content=sag_organic&utm_campaign=sag_organic&srsltid=AfmBOopj0BzrYoYaCSoQJ4VEHTL8OQ2UsU74alinmBjFCs7bzR92bIV84Mk)       |
| Jumper Wires (Male-Female)| 1   | $5.74      | $5.74  | [Amazon](https://www.amazon.in/Serplex%C2%AE-Breadboard-Connections-Assortment-Prototyping/dp/B0DR8W4N3Y/ref=asc_df_B0DR8W4N3Y?mcid=434ae378de723e7b82aeddce22667654&tag=googleshopdes-21&linkCode=df0&hvadid=709963085936&hvpos=&hvnetw=g&hvrand=7833136022907648132&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9062044&hvtargid=pla-2391433251529&psc=1&gad_source=1) |


**Total Cost**: **$100.69 USD**

Give or take a few dollars for shipping, tax 
---

## Code and Firmware

Just basic Arduino code with `Servo.h` and the PCA9685 library. Upload and run. You can control the arm using joystick input, sliders, or from Python/serial if you like writing scripts instead of turning knobs.

You’ll find the code inside `/firmware`.

---

## Wiring

- MG996R Servos → PCA9685 outputs (channels 0–3)
- PCA9685 → VCC (5V), GND, SDA/SCL → Arduino A4/A5
- Power supply → PCA9685 power rail (don’t power servos from Arduino, it will cry)

---
## gallery 

<img width="448" height="697" alt="Screenshot 2025-07-19 172724" src="https://github.com/user-attachments/assets/dea2a4e8-7a8a-48a7-8ef6-13b0c92cf5e5" />
<img width="1171" height="940" alt="Screenshot 2025-07-19 172533" src="https://github.com/user-attachments/assets/f56900b7-5636-4692-a278-94da0081aa00" />
<img width="873" height="729" alt="Screenshot 2025-07-19 172345" src="https://github.com/user-attachments/assets/b318820b-8897-4cff-ada8-d4f0120f62f5" />
<img width="913" height="311" alt="Screenshot 2025-07-19 172128" src="https://github.com/user-attachments/assets/b6e212bf-9b1d-4547-afa1-d46f18bd9a96" />
<img width="858" height="700" alt="Screenshot 2025-07-19 172028" src="https://github.com/user-attachments/assets/c2bf9e1e-b802-4ef2-9e4f-030a7c85d109" />
<img width="423" height="951" alt="Screenshot 2025-07-19 193125" src="https://github.com/user-attachments/assets/f8853129-c265-469e-8e7d-945be35f0751" />
<img width="626" height="1065" alt="Screenshot 2025-07-19 173041" src="https://github.com/user-attachments/assets/dc158ba3-40e0-4e45-85f8-c5ceffdb364d" />

---

## License

MIT. Basically, do whatever you want with it. Build it, sell it, remix it into something weird. Just don’t sue us if it punches you.

