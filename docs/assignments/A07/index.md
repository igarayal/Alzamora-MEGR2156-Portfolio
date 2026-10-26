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

<img width="400" height="400" alt="Screenshot 2026-10-26 010326" src="https://github.com/user-attachments/assets/02aa8423-3b44-4d94-89f1-f43e90d4bf07" />

Stress Plot

<img width="400" height="400" alt="Screenshot 2026-10-26 010926" src="https://github.com/user-attachments/assets/3110d949-e289-48fa-bb9b-18b31481cd16" />

Displacement Plot

<img width="400" height="400" alt="Screenshot 2026-10-26 010941" src="https://github.com/user-attachments/assets/894bed49-b6b9-45fe-859f-71ea65fcc5e2" />

Factor of Safety Plot

<img width="400" height="400" alt="Screenshot 2026-10-26 011159" src="https://github.com/user-attachments/assets/6c0aad11-3977-4a05-815e-ff408f528192" />

Design I – Finer Mesh

Mesh
<img width="400" height="400" alt="Screenshot 2026-10-26 012955" src="https://github.com/user-attachments/assets/10c9cf2b-fc7c-41da-95cd-fe9745695f8a" />

Stress Plot

<img width="400" height="400" alt="Screenshot 2026-10-26 013839" src="https://github.com/user-attachments/assets/c1719bf1-4cb4-4029-927c-867613908fe7" />

Displacement Plot

<img width="400" height="400" alt="Screenshot 2026-10-26 013952" src="https://github.com/user-attachments/assets/170caedc-81a9-4252-a82b-3cd74f515c2c" />

Factor of Safety Plot

<img width="400" height="400" alt="Screenshot 2026-10-26 014037" src="https://github.com/user-attachments/assets/23ffaa12-6c11-47fd-ad7f-212c992b6452" />

Design II – Coarse Mesh

Mesh

<img width="400" height="400" alt="Screenshot 2026-10-26 071806" src="https://github.com/user-attachments/assets/ddd3158b-7464-458a-a173-91c84e585cc4" />

Stress Plot

<img width="400" height="400" alt="Screenshot 2026-10-26 071946" src="https://github.com/user-attachments/assets/369a889a-77c0-4a00-875a-9bf85ff6f9d7" />

Displacement Plot

<img width="400" height="400" alt="Screenshot 2026-10-26 071956" src="https://github.com/user-attachments/assets/b81266b7-482d-4909-ae71-f483856f56e8" />

Factor of Safety Plot

<img width="400" height="400" alt="Screenshot 2026-10-26 072152" src="https://github.com/user-attachments/assets/e4fd30f1-fdaa-4c5c-8efa-eac541a1a90f" />

Design II – Finer Mesh

Mesh
<img width="400" height="400" alt="Screenshot 2026-10-26 072637" src="https://github.com/user-attachments/assets/6846d2ed-5772-48fa-b93e-79521cd861c8" />

Stress Plot
<img width="400" height="400" alt="Screenshot 2026-10-26 072714" src="https://github.com/user-attachments/assets/14b4eb55-30aa-4802-897d-5dd46095ad41" />

Displacement Plot
<img width="400" height="400" alt="Screenshot 2026-10-26 072725" src="https://github.com/user-attachments/assets/e23253c7-fbce-4b65-9201-a55bc933eef9" />

Factor of Safety Plot
<img width="400" height="400" alt="Screenshot 2026-10-26 072733" src="https://github.com/user-attachments/assets/52f414bb-c918-466f-ae5d-4b94668d23af" />

Design III – Coarse Mesh

Mesh

<img width="400" height="400" alt="Screenshot 2026-10-26 074248" src="https://github.com/user-attachments/assets/0842ce42-472b-4a78-9634-ca08f3d7601d" />

Stress Plot

<img width="400" height="400" alt="Screenshot 2026-10-26 074300" src="https://github.com/user-attachments/assets/469ef4e0-6131-4bc7-ba5b-65bd417139ef" />

Displacement Plot

<img width="400" height="400" alt="Screenshot 2026-10-26 074308" src="https://github.com/user-attachments/assets/6cc2cb28-dc7c-40e1-9efe-b9a893f0f476" />

Factor of Safety Plot

<img width="400" height="400" alt="Screenshot 2026-10-26 074324" src="https://github.com/user-attachments/assets/9e564afd-c903-4d5f-bf60-ae78f2e7bf6e" />

Design III – Finer Mesh

Mesh

Stress Plot

Displacement Plot

Factor of Safety Plot

## Communicate
One of the biggest things I learned from this assignment was how changing the thickness of the connecting gusset affects the factor of safety. As I increased the gusset thickness throughout my three designs, the factor of safety increased from approximately 2.3 in my original design to 3.8 in my final design. Although I did not reach the target factor of safety of 4, my final design came close without adding more material than necessary.

I also learned how important mesh refinement is when performing FEA. Even though my displacement results were within the required 7% difference, the maximum stress and factor of safety were still around 16%. This showed me that I would need additional mesh refinement to determine whether my results had fully converged.
Overall, I spent approximately 2–3 hours working on the FEA simulations, making changes to my bracket design, and documenting my results for my GitHub portfolio.

