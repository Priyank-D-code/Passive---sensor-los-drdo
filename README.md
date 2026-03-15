# Passive Sensor LOS Triangulation Simulator

**Research implementation from ITR-DRDO internship, Summer 2025**

Interactive 3D visualisation of a novel clustering algorithm for passive sensor measurement association, developed during a research internship at Central Data Processing (CDP), Integrated Test Range (ITR), DRDO, Chandipur, Balasore.

## What this demonstrates

- **Pairwise LOS triangulation** - each pair of passive sensors triangulates a target position using azimuth/elevation measurements in ECEF coordinates
- **Geometric cluster validation** - validity conditions using angle-noise uncertainty bounds (σ multiplier)
- **Intensity-based filtering** - only clusters with high spatial intersection density proceed to association cost evaluation
- **Real-time performance** - algorithm achieves 99.97% FCA at 0.10s CPU time vs 2.80s baseline (So-D + Seq(2-D))

## Algorithm performance (from research report)

| Sensors | Our Method (CPU) | So-D+Seq(2-D) | FCA |
|---------|-----------------|----------------|-----|
| 4       | 0.10s           | 2.80s          | 99.97% |
| 7       | 0.25s           | 9.90s          | 99.95% |
| 10      | 0.41s           | 20.2s          | 99.91% |

## How to run

Open `index.html` in any modern browser. No server or dependencies required.

Or deploy instantly to GitHub Pages - push to a repo and enable Pages.

## Controls

- **Drag** to rotate the 3D scene
- **Scroll** to zoom
- **Step Through** to see each algorithm phase (sensors -> targets -> LOS rays -> triangulations -> clusters -> estimates)
- **Run Simulation** for full result

## Research context

- **Institution:** Central Data Processing (CDP), ITR-DRDO, Chandipur, Balasore
- **Period:** 15 May - 14 June 2025
- **Supervised by:** Sanjay Kumar Sahani (Scientist-G, Group Director), Y.P. Mohanty (Scientist-B)
- **Authors:** Priyank Dhandhania (KIIT), Shiv Sankar Sahoo (SUIIT), Shiv Sundara Sahoo (SUIIT), Swetajali Sahu (VITAM)

## Stack

Pure JavaScript . Three.js (r128) . No build step required
