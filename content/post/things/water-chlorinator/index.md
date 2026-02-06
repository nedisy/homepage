---
title: Water Chlorinator
description: Implementing water chlorination at home
slug: water-chlorinator
date: 2024-07-20 22:32:14+07:00
lastmod: 2026-02-06 09:57:37+07:00
image: pasted-image-20260206103743.jpg
categories:
- things
tags:
- ideas
- contraptions
- inventions
---

Water chlorinator is a system that deliver correct dose of chlorine into water source. The correct chlorination dose is determined by chlorination graph. The graph consist of chlorine added vs chlorine residues in water. To measure chlorine residual experiment is conducted on various chlorine addition to several cuvette/mini tube. Pool chlorine meter is then used to label free chlorine concentration with dye. In order to get consistent chlorine reading, every tube that will be read by camera is photographed in the state of control, with no dye. Then the photo is taken again with the dye. The pixel value then analyzed to get percent of each wavelengths (RGB) that is absorbed or transmitted. It will be twice, first with deionized water to get reference reading of free chlorine concentration, the second use water to be analyzed to get chlorination graph.
# Experimental Design
## Apparatus
- Cuvette/tube
- Pipette
- Phone
- White Blank Screen
- Computer
- Weighting Scale
## Reagent
- Deionized Water
- Water to be analyzed (already been cleaned with water clarifier experiment)
- Chlorine dye (Ortholidine)
## Steps
1. Create 0.01% active chlorine stock solution from bleach (Bayclin)
2. Prepare five cuvette/tubes
3. Fill the tubes with deionized water according to prescribed amount in the table below
4. Take a photo of the tubes
5. Add chlorine stock solution to the tube with the prescribed amount
6. Add a drop of the dye for each tube
7. Take a photo again
8. Process the absorption data

| Parameter              | Tube 1 | Tube 2 | Tube 3 | Tube 4 | Tube 5 | Note           |
| ---------------------- | ------ | ------ | ------ | ------ | ------ | -------------- |
| Chlorine added (ppm)   | 2      | 4      | 6      | 8      | 10     | Reference      |
| Deionized water (gram) | 1.96   | 1.92   | 1.88   | 1.84   | 1.8    | To be added    |
| Chlorine stock (gram)  | 0.04   | 0.08   | 0.12   | 0.16   | 0.2    | To be added    |
| Red Absorption         |        |        |        |        |        | to be measured |
| Green Absorption       |        |        |        |        |        | to be measured |
| Blue Absorption        |        |        |        |        |        | to be measured |
9. Plot graph for each channel's absorption vs chlorine added.
10. Use the graph with the strongest correlation.
11. Do it all over for the water to be analyzed

| Parameter                   | Tube 1 | Tube 2 | Tube 3 | Tube 4 | Tube 5 | Note           |
| --------------------------- | ------ | ------ | ------ | ------ | ------ | -------------- |
| Chlorine added (ppm)        | 2      | 4      | 6      | 8      | 10     | Reference      |
| Water to be analyzed (gram) | 1.96   | 1.92   | 1.88   | 1.84   | 1.8    | To be added    |
| Chlorine stock (gram)       | 0.04   | 0.08   | 0.12   | 0.16   | 0.2    | To be added    |
| Best correlated Absorption  |        |        |        |        |        | to be measured |

9. Plot graph for the chosen channel.

If no significant increase in chlorine concentration observed, do it again and start by chlorine added 12 ppm, if still nothing observed, do again for 22 and so on.
