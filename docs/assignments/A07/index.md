# A7 – Bracket FEA

## Objective
For this assignment, I used Finite Element Analysis (FEA) in SolidWorks to improve my previous bracket design from A5 and A6. My goal was to increase the strength and stiffness of the bracket while reducing its weight without changing the assigned Aluminum 6061-T6 material. I completed three design iterations, comparing the stress, displacement, and factor of safety for each design. I also used coarse and finer meshes to evaluate convergence and determine whether the results were within a 7% difference.

## Analyze
For each design, I applied the same loading conditions and fixtures to keep my results consistent. I used Fixed Geometry on the pocket faces where the bracket connects to the rigid T-beam and applied a 650 lbf load to the pin to simulate bending.

I started each simulation with a coarse mesh and recorded the maximum von Mises stress, maximum displacement, and factor of safety. I then refined the mesh and ran the simulation again to compare the results. After completing the three design iterations, I found that only the maximum displacement had a difference of less than 7%. The maximum stress and factor of safety still had differences of approximately 16%, meaning these results had not fully converged.

## Decide
For Design I, I kept the original geometry from A6 unchanged so I could use it as a baseline for my other designs.

For Design II, I increased the connecting gusset thickness from 0.09375 in to 0.125 in and increased its width from 0.9375 in to 1.25 in. I also increased the extruded cut in the pocket to remove more material and reduce the overall weight of the bracket while maintaining its strength.

For Design III, I increased the connecting gusset thickness again to see whether the difference in maximum stress between the coarse and finer meshes would decrease below 7%. I focused mainly on the maximum stress because it was the result that had not come close to converging.

Design I – Coarse Mesh

Mesh

Stress Plot

Displacement Plot

Factor of Safety Plot

Design I – Finer Mesh

Mesh

Stress Plot

Displacement Plot

Factor of Safety Plot

Design II – Coarse Mesh

Mesh

Stress Plot

Displacement Plot

Factor of Safety Plot

Design II – Finer Mesh

Mesh

Stress Plot

Displacement Plot

Factor of Safety Plot

Design III – Coarse Mesh

Mesh

Stress Plot

Displacement Plot

Factor of Safety Plot

Design III – Finer Mesh

Mesh

Stress Plot

Displacement Plot

Factor of Safety Plot

## Communicate
One of the biggest things I learned from this assignment was how changing the thickness of the connecting gusset affects the factor of safety. As I increased the gusset thickness throughout my three designs, the factor of safety increased from approximately 2.3 in my original design to 3.8 in my final design. Although I did not reach the target factor of safety of 4, my final design came close without adding more material than necessary.

I also learned how important mesh refinement is when performing FEA. Even though my displacement results were within the required 7% difference, the maximum stress and factor of safety were still around 16%. This showed me that I would need additional mesh refinement to determine whether my results had fully converged.
Overall, I spent approximately 2–3 hours working on the FEA simulations, making changes to my bracket design, and documenting my results for my GitHub portfolio.

