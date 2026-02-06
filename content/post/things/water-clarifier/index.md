---
title: Water Clarifier
description: Implementing water clarifier system in home scale
slug: water-clarifier
date: 2024-07-19 00:07:13+07:00
lastmod: 2026-02-06 09:58:26+07:00
image: pasted-image-20260206103743.jpg
categories:
- things
tags:
- ideas
- contraptions
- inventions
---

Water clarifier, or water sedimentation pool is an idea to build small scale water treatment plant. Because the lack of treatment facilities in rural Indonesia, small scale ones need to be build. I propose simple and affordable way to build water clarifier. First, we need to calculate average daily domestic water use of the served community, whether it is one house, multiple ones, or a residential area. In this case, I use my house as the example for calculation.
## Domestic Water Use
Not all water need a treatment. Treatment primarily used for bath, potable water, and drinking. From [IWAP]([Defining domestic water consumption based on personal water use activities | Journal of Water Supply: Research and Technology-Aqua | IWA Publishing (iwaponline.com)](https://iwaponline.com/aqua/article/70/7/1002/83539/Defining-domestic-water-consumption-based-on)), it is expected at lest 100 liters per capita per day. My house shared water with my extended family that usually use 1000 liters per day. That figures translated to 125 liters per capita with 8 occupant. Thus it is safe to assume domestic water use to be 1000 liters per day.
## Sizing
1000 liters per day translates to around 1.2e-5 m3 per second that will be used as flow rate.  The "overflow rate", that is how quickly a basin can handle sedimentation is assumed to be less or equal to 1000 gallon/day/ft2 according to [Water MECC](https://water.mecc.edu/courses/ENV115/sedimentationb.htm). That number translates to around 4e-4 m/s. To calculate the area needed:
$$\begin{align}
A&=\frac{Q_{c}}{O_{r}}\\
Q_{c}&=1.2\cdot10^{-5}\\
O_{r}&=4\cdot10^{-4}\\
A&=0.03\text{ m}^2
\end{align}$$
The area gotten is around 0.03m2, it can be taken for square root to get approximate dimension of sedimentation basin. That is calculated to be around 0.18 m. With that, I choose to make the sedimentation basin from a jerry can with size 30x30 cm that is easy to find and easy to modify.
## Power calculation
The power needed to make this system run is calculated by multiplying head loss of the system and the flow rate. Head loss can be assumed to be mostly gravity loss because the pipe run into water tank above my house. The gravity head loss would be 4 meters, and giving some tolerance we get 6 meters. 6 meters times 1.2e-5 m3/s gives:
$$\begin{align}
P&=\frac{\rho g Q H}{\eta}\\
\rho&=1000\text{ kg/m}^3\\
g&=9.81\text{ m/s}^2\\
Q&=1.2\cdot10^{-4}\text{ m}^3\text{/s}\\
H&=6\text{ m}\\
\eta&=0.8\\
P&=8.829\text{ Watt}
\end{align}$$
[This](https://www.tokopedia.com/variaautosport/pompa-air-celup-r13-mini-dc-12v-kolam-ikan-aquarium-r13-e014b) is an example of available pump with that power or higher.
## Dosing Mechanism
For sedimentation to occur, the water need to be mixed with alum with correct dose. The dose is determined by simple mixing experiment with controlled pH. The correct dose and pH obtained by finding maximum sedimentation speed or "overflow rate". This can be done with milligram weighting device. After the optimum dose and pH is obtained, injection mechanism involving IV drip and venturi suction is set up. The correct dosage is done by adjusting screw flow limiter in the IV line and by measuring the drip interval. It has to be known before the actual flowrate and drip volume to adjust drip interval correctly. The dosing mechanism is also used for NaOH to pull the calcium out of water.
## Experimental Design
To find the exact dosing for specific application of my water supply, experiment is needed.  For alum dosing, the exact amount recommended is to be 30 mg/L and pH of 7.8. For that, preparation is needed. Other are water softening parameter. The amount required is calculated based on measured TDS to be 500 ppm.
### 1 M Alum Stock Solution
A stock solution of alum with concentration of 1 Molar needed to be made before any experiment.
The reagent needed are:
- 342.15 gram of dry Aluminium Sulfate
- Top with water until volume is 1 liter
### 20 mM Ca(OH)<sub>2</sub> Stock Solution
Other than alum, NaOH stock solution is also needed to adjust the pH.
The reagent needed:
- 1.4819 gram of dry Ca(OH)<sub>2</sub>
- Top with water until volume is 1 liter
### Water Softening Experiment
First the optimum dose need to be estimated. Based on [this](https://water.mecc.edu/courses/ENV115/lesson14_2b.htm) article, we can estimate that:
- 10 mg/L CO<sub>2</sub>
- 500 mg/L CaCO<sub>3</sub>
With that we can calculate:
A = $10\cdot1.27=12.7$
B = $500\cdot0.56=280$
C = 0
D = 0
Quicklime Feed (mg/L) = (A+B+C+D) $\cdot$ 1.15 = 337 mg/L
Lime Feed, mg Ca(OH)<sub>2</sub> /L = 337/0.757 = 445.32 mg/L
Lime Feed, L stock /L = 445.32/1481.9 = 0.3 L stock /L

Now we can design experiment with that anchor point:
1. For each mix below, mix according to the design
2. Mix thoroughly with blender or similar apparatus
3. Measure TDS

| Precursor                        | Mix 1 | Mix 2 | Mix 3 | Mix 4 | Mix 5 | Note           |
| -------------------------------- | ----- | ----- | ----- | ----- | ----- | -------------- |
| Raw Water (Liters)               | 1     | 1     | 1     | 1     | 1     | Design         |
| Limewater Stock Solution (Liter) | 0.2   | 0.25  | 0.3   | 0.35  | 0.4   | Design         |
| TDS by Electrical Conductivity   |       |       |       |       |       | To be measured |
| TDS by Boiling                   |       |       |       |       |       | To be measured |

### Flocculation Experiment
After we get the optimum lime dose, we need to play around with it to get both optimum softening potential, and optimum flocculation. Flocculation is the priority because it is the major problem with health and algae issue. Initial alum needed is 30 mg/L (A. Amirtharajah and Kirk M. Mills, 1982). Thus we need stock solution of 30/342150 = 0.0000877 L stock /L. That is equivalent to 87.7 mL stock/m<sup>3</sup>.

Measured stock density (g/mL): $\text{MSD}$ 

| Precursor                        | Mix 1             | Mix 2             | Mix 3             | Mix 4             | Mix 5             | Note           |
| -------------------------------- | ----------------- | ----------------- | ----------------- | ----------------- | ----------------- | -------------- |
| Raw Water (Liters)               | 1                 | 1                 | 1                 | 1                 | 1                 | Design         |
| Alum Stock Solution (gram)       | 0.105$\text{MSD}$ | 0.105$\text{MSD}$ | 0.105$\text{MSD}$ | 0.105$\text{MSD}$ | 0.105$\text{MSD}$ | Design         |
| Limewater Stock Solution (Liter) | 0.2               | 0.25              | 0.3               | 0.35              | 0.4               | Design         |
| Measured pH                      |                   |                   |                   |                   |                   | To be measured |
The ideal pH is 7 - 8. If all mix is suitable, then we can choose the optimum. If no coagulation is observed, double the dose to be:

| Precursor                        | Mix 1            | Mix 2            | Mix 3            | Mix 4            | Mix 5            | Note           |
| -------------------------------- | ---------------- | ---------------- | ---------------- | ---------------- | ---------------- | -------------- |
| Raw Water (Liters)               | 1                | 1                | 1                | 1                | 1                | Design         |
| Alum Stock Solution (gram)       | 0.21$\text{MSD}$ | 0.21$\text{MSD}$ | 0.21$\text{MSD}$ | 0.21$\text{MSD}$ | 0.21$\text{MSD}$ | Design         |
| Limewater Stock Solution (Liter) | 0.2              | 0.25             | 0.3              | 0.35             | 0.4              | Design         |
| Measured pH                      |                  |                  |                  |                  |                  | To be measured |
