# A4 – Motor Mount

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

The stress calculation produced a required thickness of:

h_stress = 11.86 mm

The deflection calculation produced:

h_deflection = 17.50 mm

Once again, deflection controlled the design.

I selected:

h₂ = 18 mm

The resulting calculated values were:

σ = 6.94 MPa

δ = 0.276 mm

The calculated stress remains below the allowable stress of 16 MPa, while the calculated deflection remains below the required maximum of 0.30 mm.



## Decide

Material Selection: PLA was selected because it is suitable for 3D printing and provides the stiffness and strength required for the calculated loading conditions.

Feature 1 Design: The calculations indicated that a minimum thickness of 15.29 mm was required to satisfy the deflection requirement. An 18 mm thickness was selected to provide additional stiffness.

Feature 2 Design: The calculations indicated that a minimum thickness of 17.50 mm was required. An 18 mm thickness was selected to satisfy the requirement.

Curved Transition: A curved transition was incorporated between Feature 1 and Feature 2 instead of using a sharp corner. The curve was accounted for in the CAD geometry while the hand calculations used an equivalent simplified beam model.

Overall Geometry: The primary dimensions of the original design were maintained, including a 40 mm width, approximately 50 mm Feature 1 length, and approximately 50 mm Feature 2 height. The curved transition was incorporated within this overall geometry.

Mounting Features: The design includes four Ø3.4 mm motor clearance holes positioned on a Ø22 mm bolt circle and a Ø7 mm shaft clearance hole.

The resulting design satisfies the calculated stress and deflection requirements while incorporating the curved geometry into a manufacturable motor mount.

The curved motor mount was modeled parametrically in SOLIDWORKS. The primary dimensions were created as editable parameters so that the design could be modified without rebuilding the entire model.

The model includes Feature 1, Feature 2, the curved transition, motor mounting holes, and shaft clearance.

The curved section was created using a controlled radius so that its geometry could also be adjusted parametrically. This allowed the overall shape of the mount to be changed while maintaining the required mounting dimensions.
## Communicate

Through this project, I learned how theoretical beam calculations can be applied to a component that does not have completely straight geometry. The hand calculations provided the required dimensions for the major structural sections, while the CAD model allowed those dimensions to be incorporated into a more practical curved shape.

I also learned that deflection can control a design even when the calculated stresses are well below the allowable material stress. In both structural sections, the deflection requirement resulted in a larger required thickness than the stress requirement.

Another important lesson was understanding how simplified engineering models can be used during the early design process. The actual mount contains a curved transition, but simplifying the geometry into equivalent beam sections made it possible to estimate the required dimensions using standard beam equations.

The curved transition also demonstrated the importance of translating analytical calculations into practical geometry. A real component may contain radii, mounting holes, and other features that are not represented directly in the initial hand calculations.

Overall, this project improved my understanding of the relationship between structural analysis, design constraints, and parametric CAD modeling.

This project took me roughly 6 hours to complete.
