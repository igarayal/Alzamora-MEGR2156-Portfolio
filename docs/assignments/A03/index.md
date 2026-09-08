# A3 –  Parametric and FEA

## Objective
The objective of this assignment was to design an aluminum bar that could support a direct tensile load without exceeding the maximum axial deflection of 0.009 inches. For my design, I selected an applied load of 300 lbf and used aluminum as the material. I used hand calculations and parametric modeling in SolidWorks to determine the dimensions of the bar. After creating the model, I performed Finite Element Analysis (FEA) using the same loading conditions to check the displacement and stress. The main purpose of this assignment was to understand how load, material properties, and geometry affect the stiffness and strength of a part.

## Analyze
I began by looking at the relationship between the applied load, cross-sectional area, length, Young’s Modulus, and axial deflection. I selected a tensile load of 300 lbf and used the direct tension equation to determine the required dimensions of my bar while staying within the maximum allowable deflection of 0.009 inches. My calculations also helped me determine the values that I needed to enter into SolidWorks for the parametric model.

<img width="500" height="500" alt="IMG_0410" src="https://github.com/user-attachments/assets/8d6fbfb9-a74f-4e69-b81e-e0fb97e17180" />

After completing my calculations, I created the bar in SolidWorks. I set up parameters for the important design values and connected them using equations so that the dimensions of the model were based on the calculations rather than being entered independently. This allowed the length of the bar to automatically update if one of the design parameters was changed.

Once the parametric model was complete, I set up the FEA using the same material properties, geometry, and 300-lbf tensile load. I fixed one end of the bar and applied the tensile force to the opposite end. After creating the mesh and running the simulation, SolidWorks generated a displacement map and a von Mises stress map that I could use to evaluate the performance of my design.

## Decide
<img width="500" height="500" alt="Screenshot 2026-09-08 075433" src="https://github.com/user-attachments/assets/d0d96bb0-c8e3-4600-8b24-8461debe243e" />

<img width="500" height="500" alt="Screenshot 2026-09-08 074814" src="https://github.com/user-attachments/assets/9382717c-2856-4e0d-a0da-f2e1d6f947e4" />


Based on my calculations and FEA results, I determined whether the bar satisfied the requirements of the assignment. My hand calculation was based on a maximum axial deflection of 0.009 inches, and I compared this value with the displacement obtained from SolidWorks. My FEA displacement was [INSERT FEA DISPLACEMENT] inches, resulting in a percent difference of [INSERT PERCENT DIFFERENCE]%.

I expected the analytical and FEA results to be fairly close because the original bar has a constant cross section and is loaded directly in tension. There are no major changes in geometry that would create a stress concentration. Any small difference between the results could come from the mesh, boundary conditions, or differences in the material properties used by SolidWorks.

The displacement map showed how the bar moved under the 300-lbf load, with the largest displacement occurring toward the loaded end. The von Mises stress map showed how stress was distributed throughout the bar. The maximum stress from my FEA was [INSERT FEA STRESS], which was below the aluminum yield strength of 40 ksi. This gave the bar a factor of safety of [INSERT FACTOR OF SAFETY], showing that the design met the strength requirement.

For this design, the hand calculation was useful for predicting how the bar should behave before running the simulation. I would use the FEA as a final verification because it takes into account the actual CAD geometry, material, load, and boundary conditions used in the model.

I also considered what would happen if a substantial pin hole were added to the left side of the bar. The hole would create a stress concentration and increase the local stress in that area. I used a stress concentration factor based on the size of the hole compared with the width of the bar and used it to estimate the maximum stress. My calculations showed that the increased stress was still below the 40 ksi yield strength of aluminum. The factor of safety remained above one, so the bar would still pass the strength requirement even with the pin hole.
Pin Hole Analysis

I also looked at what would happen if a fairly substantial pin hole were added near the left side of the bar. A hole would create a stress concentration and cause the stress around that area to become higher than the nominal stress in the rest of the bar.

I used a stress concentration factor for a hole in a flat bar under tension and used the nominal stress from my FEA to estimate the increased stress around the hole. My hand calculations for the pin-hole analysis are shown below.

<img width="500" height="500" alt="IMG_0411" src="https://github.com/user-attachments/assets/dbc29372-2cf7-43b4-9503-1fce6a3647bd" />

## Communicate
I documented my design process by including my calculations, SolidWorks model, parametric setup, and FEA results. The first calculation image shows how I determined the dimensions needed for my design, while the second calculation image shows my stress concentration and factor-of-safety analysis for the hypothetical pin hole. I also included screenshots from SolidWorks to show the development of the model and the results of the simulation.

One of the main things I learned from this assignment was how parametric modeling can make the design process more efficient. Instead of manually changing dimensions whenever a design value changes, SolidWorks can use equations to automatically update the geometry. This helped me understand how changing the load, dimensions, or material properties can affect the overall design.

I also learned how FEA can be used to verify results that were first predicted through hand calculations. The calculations gave me an idea of what I should expect, while the FEA allowed me to visualize the displacement and stress throughout the bar. Comparing the two methods helped me better understand the connection between engineering calculations, CAD modeling, and simulation.

One challenge I had during this assignment was making sure that the values used in SolidWorks matched the values from my hand calculations. The load, dimensions, material properties, and boundary conditions needed to be consistent so that the comparison between the two methods was accurate.

Overall, this assignment gave me a better understanding of how analytical calculations, parametric modeling, and FEA can be used together to design and evaluate a part.

I spent approximately 4 hours completing this assignment.

CAD File

SolidWorks CAD File Download: [INSERT LINK]
