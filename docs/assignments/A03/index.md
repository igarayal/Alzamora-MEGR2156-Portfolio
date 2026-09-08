# A3 – [Topic]

## Objective
The objective of this assignment was to design an aluminum bar that could support a direct tensile load without exceeding the maximum allowable axial deflection of 0.009 inches. I used the axial deflection equation along with parametric modeling in SolidWorks to determine the dimensions of the bar. After creating the model, I used Finite Element Analysis (FEA) to check the displacement and stress produced by the same applied load. The purpose of the assignment was to better understand how force, material properties, and geometry all work together to affect the stiffness and strength of a part.

## Analyze
I started by looking at the relationship between the applied force, cross-sectional area, bar length, Young’s Modulus, and axial deflection. The direct tension equation



was used to determine the required length of the bar based on the selected dimensions and material properties. For my design, I used an applied tensile load of 400 lbf and a Young’s Modulus of (10 \times 10^6) psi.

After completing the hand calculations, I created the bar in SolidWorks using parametric equations. I assigned variables to the important dimensions and properties so that the length of the bar would update automatically whenever one of the design values changed. This made it easier to connect the engineering calculations directly to the CAD model instead of entering every dimension manually.

Once the model was complete, I performed a Finite Element Analysis using the same 400-lbf tensile load and the same aluminum material properties. One end of the bar was constrained while the tensile force was applied to the opposite end. The simulation produced both a displacement plot and a von Mises stress plot, which allowed me to compare the numerical FEA results with the results from the hand calculations.

## Decide
After comparing the calculations and simulation results, I determined that the selected dimensions satisfied the requirements of the assignment. The analytical design was based on a maximum axial deflection of 0.009 inches, and I compared the FEA displacement result to this value to determine how closely the simulation matched the hand calculation.

I also compared the maximum von Mises stress from the FEA with the specified aluminum yield strength of 40 ksi. From this comparison, I was able to calculate the factor of safety and determine whether the bar would remain below the yield strength under the applied load.

For a straight bar with a constant cross section and a simple tensile load, I expected the analytical and FEA deflection results to be very similar. The geometry does not contain major changes in shape or stress concentrations, so the assumptions used in the axial deflection equation closely match the conditions used in the simulation. Any small difference between the two results could come from the mesh, boundary conditions, or the exact material properties entered into SolidWorks.

For this design, I would use the hand calculation as a quick prediction and the FEA result as a final verification of the model. The displacement plot shows how much the bar moves while under the applied tensile force, while the von Mises stress plot shows how the stress is distributed throughout the bar.

I also considered what would happen if a pin hole were added near the left side of the bar. Using a stress concentration factor for a hole in a flat bar under tension, I estimated the increase in local stress around the hole. Even with the increased peak stress caused by the hole, the estimated stress remained below the 40 ksi yield strength of the aluminum. The resulting factor of safety also remained greater than one, meaning the modified bar would still satisfy the strength requirement.


## Communicate
Throughout the assignment, I documented my calculations, CAD model, SolidWorks equations, simulation setup, displacement results, and von Mises stress results. I included screenshots at different stages of the process to show how the design developed from the original calculations into the completed model and FEA.

One of the main things I learned from this assignment was how useful parametric modeling can be during the design process. Instead of manually recalculating and changing dimensions every time one variable changes, equations can be used to automatically update the model. This makes it much easier to explore different design conditions and understand how each parameter affects the final geometry.

I also learned how FEA can be used alongside hand calculations. The analytical equations provide a quick way to predict how a simple part should behave, while FEA provides a visual way to examine displacement and stress throughout the model. Using both methods helped me better understand the connection between engineering calculations, CAD modeling, and simulation.

One challenge during the assignment was making sure the parameters, units, material properties, loads, and fixtures were consistent between the hand calculations and the FEA model. Small differences in these inputs could cause the simulation results to differ from the expected analytical values.

In total, I spent approximately 3 hours completing the calculations, creating the parametric SolidWorks model, running the FEA, reviewing the results, and documenting the assignment.
