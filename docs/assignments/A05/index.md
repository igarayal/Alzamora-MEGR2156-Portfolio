# A5 – Motor Mount

## Objective
The objective of this project was to design a motor mount for a 24 V DC gear motor that attaches the motor to rigid wall A and supports a 300 N force applied to the motor shaft. This design uses a curved transition between the motor-supporting section and the wall-mounting section rather than a sharp 90° corner.

The mount must be designed using a safety factor of 3 and must maintain a maximum allowable deflection of 0.30 mm at the free end. The weight of the motor is neglected. The final goal was to create a practical, manufacturable, and parametric CAD model with SolidWorks that satisfies the required stress and deflection limits while incorporating the curved geometry.

## Analyze
I first reviewed the project requirements, Appendix A, and Appendix B to determine the loading conditions, motor dimensions, and required design constraints. Appendix A provided the motor dimensions, including the Ø28 mm gearbox, Ø27.7 mm motor body, Ø6 mm shaft, Ø22 mm mounting-hole pattern, and four M3 mounting holes.

The primary difference between this design and the original L-shaped motor mount is the curved transition between the two main structural sections. The overall loading conditions remain the same, but the curve changes how the horizontal and vertical sections connect.

For the hand calculations, the mount was simplified into equivalent beam sections so that standard beam equations could still be used to estimate stress and deflection. The curved portion was then incorporated into the CAD geometry.

The project allowed ABS, PETG, or PLA. I compared the available materials and selected PLA because it provides sufficient stiffness and strength for the calculated loading conditions while also being easy to manufacture using 3D printing.

The material properties used for the calculations were:

E = 3500 MPa

Sy = 48 MPa

Using the required safety factor of 3:

σ_allow = 48 / 3

σ_allow = 16 MPa

Therefore, the design was required to remain below an allowable bending stress of 16 MPa.
I researched existing motor-mount designs to better understand common mounting geometries and methods of increasing stiffness. The designs included L-shaped brackets, motor mounting plates, and brackets using curved or reinforced transitions between structural members.

This research showed that a curved transition could be incorporated between the horizontal and vertical sections while maintaining the same basic function as a traditional L-shaped bracket.

Links to existing motor mounts:

https://www.pololu.com/product/1084

https://www.pololu.com/product/1995/resources

Feature 1 represents the portion of the mount that extends outward from rigid wall A and supports the motor. For the hand calculations, this section was approximated as a cantilever beam.

Although the final CAD geometry contains a curve, the straight cantilever approximation provides a simplified and conservative method for sizing the main structural section.

The rectangular beam equations were used to determine the required thickness based on both bending stress and deflection. Because the required thickness based on deflection was greater than the thickness based on stress, deflection controlled the design. The calculated stress is below the allowable stress of 16 MPa, and the calculated deflection is below the maximum allowable deflection of 0.30 mm.
<img width="500" height="500" alt="Screenshot 2026-09-16 144130" src="https://github.com/user-attachments/assets/bfeb40bf-d542-458d-9700-a5847ea1d773" />
<img width="500" height="500" alt="Screenshot 2026-09-16 144138" src="https://github.com/user-attachments/assets/c94d15e0-8e53-475f-bbe2-b6b7de0820dc" />
<img width="500" height="500" alt="Screenshot 2026-09-16 144158" src="https://github.com/user-attachments/assets/6aab5315-86e3-4604-a34e-17514ec31e28" />


## Decide


## Communicate

