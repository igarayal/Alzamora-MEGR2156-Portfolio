# A3 –  Parametric and FEA

## Objective
The objective of this assignment was to design an aluminum bar that could support a direct tensile load without exceeding the maximum axial deflection of 0.009 inches. For my design, I selected an applied tensile load of 301 lbf, which satisfies the required load range of greater than 300 lbf and less than 500 lbf. I used aluminum with a Young’s Modulus of approximately \(10 \times 10^6\) psi.

I used hand calculations and parametric modeling in SolidWorks to determine the geometry of the bar. After creating the model, I performed Finite Element Analysis (FEA) using the same loading conditions to evaluate the displacement and von Mises stress. The purpose of this assignment was to understand how load, material properties, and geometry affect the stiffness and strength of a part and to compare analytical calculations with FEA results.

## Analyze
I began by examining the relationship between the applied load, cross-sectional area, length, Young’s Modulus, and axial deflection. I selected a tensile load of 301 lbf and used a maximum allowable axial deflection of 0.009 inches.

The assignment specified a circular cross section, so I modeled the bar with a diameter of 0.500 inches. Using the direct-tension elongation relationship, I determined the required length of the bar based on the selected load, material properties, and cross-sectional area.

My hand calculations are documented on two separate calculation pages. Calculation Page 1 contains the initial design calculations used to determine the geometry of the bar, including the cross-sectional area, axial deflection, required bar length, nominal stress, and initial factor of safety.

[EMBED CALCULATION PAGE 1 HERE]

Based on my calculations, the final bar was designed with a diameter of 0.500 inches and a length of approximately 58.71 inches.

After completing the analytical calculations, I created the bar in SolidWorks using the calculated dimensions and assigned aluminum as the material.

I then created a static FEA study using the same design conditions. One circular end of the bar was fixed, while a 301-lbf tensile force was applied to the opposite circular end. After applying the appropriate boundary conditions, I created a mesh and ran the simulation. SolidWorks was then used to generate displacement and von Mises stress maps.



## Decide
[EMBED SOLIDWORKS MODEL SCREENSHOT HERE]

The completed SolidWorks model represents the cylindrical aluminum bar created using the dimensions determined from my analytical design process.

[EMBED FIXTURE/LOAD SCREENSHOT HERE]

For the FEA, one end of the bar was completely fixed while a 301-lbf tensile force was applied to the opposite end. This represented the direct-tension loading condition used in my calculations.

Displacement Results

[EMBED DISPLACEMENT MAP HERE]

My analytical design was based on a maximum axial deflection of 0.009 inches. The maximum displacement obtained from my SolidWorks FEA was [INSERT FEA DISPLACEMENT] inches, resulting in a percent difference of [INSERT PERCENT DIFFERENCE]% between the analytical and FEA results.

I expected the analytical and FEA displacement results to be relatively close because the original bar has a constant circular cross section and is subjected to simple axial tension. There are no major changes in the original geometry that would create significant stress concentrations. Any small difference between the results could be caused by the mesh, boundary conditions, or slight differences between the material properties assumed in the hand calculations and those assigned in SolidWorks.

The displacement map showed how the bar deformed under the applied tensile load, with the largest displacement occurring toward the loaded end and the smallest displacement occurring at the fixed end.

Von Mises Stress Results

[EMBED VON MISES STRESS MAP HERE]

The von Mises stress map showed the stress distribution throughout the bar. The maximum stress obtained from my FEA was approximately 1.63 ksi, which was well below the specified aluminum yield strength of 40 ksi.

Using the FEA stress and the aluminum yield strength, I determined a factor of safety of approximately 24.5. Because the maximum stress was significantly below the yield strength and the factor of safety was greater than one, the bar satisfied the strength requirement.

The hand calculation was useful for predicting how the bar should behave before performing the simulation. For a uniform bar subjected to direct axial tension, I expected the analytical and FEA results to be relatively similar. I would use the FEA as the final verification of the design because it evaluates the actual CAD geometry, assigned material properties, applied load, mesh, and boundary conditions.

Pin Hole Analysis

The assignment also required consideration of what would happen if a fairly substantial pin hole were added near the left side of the bar. Although the primary bar was modeled with a circular cross section as specified in the assignment description, the pin-hole portion of the assignment specifically asks for the stress concentration factor for a hole in a flat bar under tension. Therefore, I treated the pin-hole portion as a separate simplified stress-concentration analysis.

A pin hole creates a geometric discontinuity that causes the local stress surrounding the hole to become greater than the nominal stress in the rest of the bar.

Calculation Page 2 documents my pin-hole analysis. For this calculation, I used the hole-to-width ratio to determine the appropriate stress concentration factor. I then used the nominal stress from my FEA to estimate the maximum local stress that could occur around the hypothetical hole. Finally, I compared the estimated maximum stress with the 40 ksi aluminum yield strength to determine whether the design would still satisfy the strength requirement.

[EMBED CALCULATION PAGE 2 HERE]

Using a stress concentration factor of approximately 2.17 and a nominal FEA stress of approximately 1.63 ksi, I estimated a maximum stress of approximately 3.54 ksi around the hypothetical pin hole. This resulted in a factor of safety of approximately 11.3.

The estimated maximum stress remained well below the aluminum yield strength of 40 ksi, and the resulting factor of safety remained greater than one. Therefore, based on this simplified stress-concentration analysis, the bar would still satisfy the strength requirement with the hypothetical pin hole.

## Communicate
I documented my work using two pages of handwritten calculations along with screenshots of my SolidWorks model and FEA results. Calculation Page 1 documents the initial axial-deflection design process used to determine the geometry of the bar and evaluate its nominal stress and factor of safety. Calculation Page 2 documents the hypothetical pin-hole analysis, including the stress concentration factor, estimated peak stress, and resulting factor of safety.

I also included screenshots from SolidWorks showing the development of the CAD model, the applied fixture and tensile load, and the results of the simulation. The displacement and von Mises stress maps allowed me to visually evaluate how the bar responded to the applied load.

One of the main things I learned from this assignment was how the variables involved in axial deflection are related. Changing the applied force, cross-sectional area, material stiffness, or length directly affects the amount of deformation experienced by the bar. I also learned how parametric modeling can be used to relate design variables so that changes to one parameter can automatically affect the resulting geometry.

I also learned how FEA can be used to verify results that were first predicted through analytical calculations. The hand calculations provided an expected result, while the FEA allowed me to visualize the displacement and stress distribution throughout the entire model. Comparing the two methods helped me better understand the connection between engineering calculations, CAD modeling, and numerical simulation.

One challenge I encountered during this assignment was interpreting the geometry requirements. The assignment description specified a circular cross section, while later portions referred to width, height, thickness, and a hole in a flat bar. I initially performed calculations using flat-bar dimensions before recognizing that these calculations did not correspond with my cylindrical CAD model. I corrected the main analysis so that the geometry and calculations corresponded with the circular bar used for the FEA. This showed me the importance of keeping the assumptions, geometry, material properties, and loading conditions consistent between analytical calculations and computer simulations.

Another challenge was making sure that the load, dimensions, material properties, and boundary conditions used in SolidWorks were consistent with the values used in my calculations. This was important because inconsistencies between the analytical model and FEA model would make it difficult to accurately compare the results.

Overall, this assignment gave me a better understanding of how analytical calculations, parametric CAD modeling, and FEA can be used together to design and evaluate an engineering component.

Actual time spent: Approximately 4 hours
