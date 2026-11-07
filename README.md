# Delta + T3 pick cell

Browser digital twin of a pick, inspect and palletize cell: a delta robot picks parts from a conveyor into a shared buffer nest, and an Epson T3-401S SCARA inspects each part over a camera and places it on a pallet or in a reject bin.

**Live:** https://sergiudanstan.github.io/delta-t3-cell/

- Delta inverse kinematics (3 arms, parallelogram lower links) and T3 SCARA kinematics with joint limits
- Scheduled program with a mutex on the shared buffer nest
- Robot-to-robot clearance checked over the whole cycle
- Program mode (timeline, step list, timing, joints, report, CSV) and manual jog mode

Single `index.html`, three.js loaded from a CDN. Open it directly or serve the folder.
