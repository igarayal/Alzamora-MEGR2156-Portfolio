# A2 – Truss Stress Analysis
# Truss Design with Basic Stresses

## Project Overview

For this assignment, I designed a lightweight planar truss while following the given geometric, loading, and material constraints. The purpose of this project was to better understand how applied loads create internal forces and stresses within a structure and how those forces affect the dimensions required for a safe design. I started by creating a simple truss geometry, then determined the external and internal forces, calculated the required cross-sectional areas of the members and pins, and used these calculations to develop the final CAD model using Creo Parametric.

---

## Design Constraints

For my design, I selected an applied load of **P = 25 kN**, which is within the required range of 20–30 kN. The given dimensions were **a = 0.4 m** and **b = 0.3 m**, with a pin support located at point A and a roller support located at point B. The truss members are made from A500 steel and are required to have identical cross-sectional areas and geometry, while the connecting pins are made from hardened tool steel.

The main design constraints I used were:

- Applied load: **P = 25 kN**
- Horizontal dimension: **a = 0.4 m**
- Vertical dimension: **b = 0.3 m**
- Point A: **Pin support**
- Point B: **Roller support**
- Truss material: **A500 steel**
- Member safety factor: **3.5**
- Pin material: **Hardened tool steel**
- Pin yield shear strength: **170 ksi**
- Pin density: **0.278 lb/in³**
- Pin safety factor: **4**
- Pin connections: **Single shear**
- All truss members have the same cross-sectional area
- All pins are identical

<img width="530" height="570" alt="Screenshot 2026-09-04 023933"/>


.png work)
## Initial Truss Design

First, I decided what I wanted my overall truss geometry to look like. I chose a relatively simple and symmetric design because it provided a straightforward load path while making the method of joints easier to apply and verify. I divided the bottom of the truss into three sections that are each **0.4 m long** and used the required height of **0.3 m**.

The coordinates I used for the joints were:
png here
- A = (0, 0) m
- E = (0.4, 0) m
- F = (0.8, 0) m
- B = (1.2, 0) m
- C = (0.4, 0.3) m
- D = (0.8, 0.3) m

The diagonal members have a horizontal distance of 0.4 m and a vertical distance of 0.3 m. I used the Pythagorean theorem to calculate their length.
png here

I also determined the sine and cosine of the diagonal angle because these values would be needed to separate the member forces into horizontal and vertical components.

png here

These values were then used throughout the method-of-joints calculations.

**[INSERT INITIAL TRUSS SKETCH HERE]**

---

## Free Body Diagrams

Before solving for the internal forces, I created a free body diagram for each joint in the truss. I initially assumed that all unknown member forces were in tension, so the force arrows were drawn pointing away from each joint. This gave me a consistent sign convention where a positive calculated force represented tension and a negative calculated force represented compression.

I also included the external 25 kN loads at joints C and D and the support reactions at A and B. Creating each free body diagram separately helped me identify which equilibrium equations could be used at each joint. These diagrams were then used directly with the method of joints to calculate the internal forces.

**[INSERT FREE BODY DIAGRAM IMAGE HERE]**

---

## Finding the External Reaction Forces

Next, I determined the external reaction forces at the pin support A and roller support B due to the two applied loads. Since A is a pin support, it can provide both a horizontal reaction, **Ax**, and a vertical reaction, **Ay**. The roller at B provides the vertical reaction **By**.

Because there are no external horizontal loads:

png here

Finding these reactions first was necessary because they become known external forces when applying the method of joints.

png here

## Finding the Internal Member Forces

After finding the support reactions, I used the **method of joints** to determine the internal force carried by each truss member. I started at joints with no more than two unknown member forces and applied horizontal and vertical equilibrium. The forces were first solved symbolically in terms of P and then evaluated numerically using **P = 25 kN**.

### Joint A
png here

Therefore, AE is in **tension**.

---

### Joint C

I then moved to joint C, where the 25 kN external load is applied. Since FAC was already known from joint A, the remaining unknown member forces could be found using horizontal and vertical equilibrium. This allowed me to determine the forces in members CD and CE.

png here

This means CE is a **zero-force member** under the selected loading condition.

### Joint E

Next, I analyzed joint E. Since CE was found to be a zero-force member, vertical equilibrium showed that ED was also a zero-force member for this loading condition. Horizontal equilibrium was then used to determine the force in EF.

png here

Therefore, EF is in **tension**.

---

### Joint B

I then analyzed joint B. The known vertical reaction at this joint was **By = 25 kN**, which allowed me to solve for the forces in members DB and FB.

png here

### Joint F

Finally, I analyzed joint F. The horizontal forces from members EF and FB are equal in magnitude and opposite in direction. This leaves DF as the only possible vertical force at the joint.

png here

DF is a **zero-force member** under this loading condition.

---

## Internal Force Results

After completing the method-of-joints calculations, I organized the results into a table so I could compare the magnitude and condition of each member.
png here of table

The largest internal force occurs in members **AC and DB**, which both experience **41.67 kN of compression**. Because every truss member is required to have the same cross-sectional geometry, I used this maximum internal force to size all of the members. This ensures that even the most heavily loaded member satisfies the required safety factor.

---

# Cross-Sectional Area and Weight of Truss Members

## Member Cross-Sectional Area

Next, I calculated the minimum cross-sectional area required for the truss members. The members are made from A500 steel, and I used a yield strength of **46 ksi**, which is approximately **317.16 MPa**. I used the largest internal force and the required safety factor of **3.5** so that the identical cross-section would be sufficient for every member in the truss.

### Knowns

Maximum internal force:

png here

I will use the same selected cross-sectional geometry for every truss member as required by the assignment.

---

## Approximate Truss Weight

After determining the required cross-sectional area, I estimated the weight of the truss before creating the CAD model. I first added the lengths of all of the members to determine the total amount of A500 steel used in the analytical model. I then multiplied the total length by the minimum cross-sectional area to calculate volume and used the density of steel to calculate mass and weight.

png here

This hand-calculated value gives me a prediction that I can later compare with the mass properties from my CAD model.

---

# Connecting Pin Design

## Critical Pin and Single-Shear Analysis

Next, I determined the required size of the connecting pins. The assignment specifies hardened tool steel with a yield shear strength of **170 ksi**, a density of **0.278 lb/in³**, and a safety factor of **4**. I designed the connection as a **single-shear connection** as required and used the largest support reaction of **25 kN** as the expected shear force.

The pin free body diagram shows the applied shear force acting across one shear plane. This is important because a single-shear connection has only one resisting shear area. I used this loading condition to calculate the minimum area and diameter required for each identical pin.

**[INSERT CRITICAL PIN FREE BODY DIAGRAM HERE]**

png here

The actual pin diameter used in CAD must be greater than or equal to this value. I will round upward when selecting a practical pin diameter so that the final design does not fall below the calculated minimum.

---

## Approximate Combined Weight of the Pins

After determining the required pin area, I estimated the combined weight of the connecting pins. The pin weight depends on the final pin length, so I used the actual pin length selected during CAD modeling in the final calculation. The volume of each cylindrical pin is determined from its cross-sectional area and length, and the specified density can then be used to determine its weight.

png here

This value was then included when comparing my analytical weight prediction with the final CAD model.

---

# CAD Modeling

## Creating the Truss Model

The next step was to transfer the dimensions determined from my calculations into CAD. I modeled the truss, excluding the pins, as one part as required by the assignment. I maintained the selected cross-sectional area throughout each member and at the intersections around the pin joints so that the CAD geometry represented the assumptions used in my calculations.

I used the same 0.4 m horizontal spacing and 0.3 m vertical height established during the initial design. I also made sure that the cross-sectional geometry selected for the members had an area greater than or equal to the calculated minimum of **459.8 mm²**. This allowed the physical dimensions in the CAD model to satisfy the safety factor used in my analytical design.

**[INSERT CAD TRUSS SCREENSHOT HERE]**

---

## Creating the Pins

Next, I modeled the connecting pins as separate cylindrical components. The minimum calculated pin diameter was **10.42 mm**, so I selected a practical diameter that was equal to or larger than this value. I also selected a pin length that allowed the pin to pass completely through the connection without adding unnecessary material.

The final dimensions I selected were: png

I used the same dimensions for every pin because the assignment requires the connecting pins to be identical.

**[INSERT CAD PIN SCREENSHOT HERE]**

---

## Final CAD Model

After creating the truss and pins, I completed the final model using the calculated geometry and dimensions. I checked the pin locations, member intersections, and overall dimensions to make sure that the CAD model remained consistent with the free body diagrams and hand calculations. This step was important because changing the geometry during CAD modeling would also change the member forces calculated earlier.

**[INSERT FINAL CAD MODEL SCREENSHOT HERE]**

---

# Hand Calculations vs. CAD Mass Properties

After completing the model, I used the CAD mass properties tool to determine the predicted mass of the final design. I compared the CAD result with my analytical calculation to determine whether the physical model was consistent with the simplified volume and density calculations. A small difference is expected because the CAD model includes the actual joint geometry, pin holes, and other geometric details that are simplified in the hand calculations.

**[INSERT CAD MASS PROPERTIES SCREENSHOT HERE]**

My hand-calculated truss mass was:
png

The difference between these values can be explained by **[INSERT SPECIFIC REASON BASED ON YOUR CAD MODEL, SUCH AS PIN HOLES, JOINT GEOMETRY, OR THE ACTUAL SELECTED MEMBER AREA BEING LARGER THAN THE THEORETICAL MINIMUM]**.

---

# Mistakes and Design Adjustments

One mistake I identified during the design process involved making sure that my free body diagrams and calculations represented the exact same truss geometry. An earlier version of my design used inconsistent member and joint labels, which meant the calculations could not be directly compared with the drawing. I corrected this by defining all six joints first and then maintaining the same joint and member labels throughout the geometry, free body diagrams, calculations, and CAD model.

Another correction involved the maximum internal member force. I initially considered using the 25 kN applied load as the governing force for member sizing, but the method-of-joints calculations showed that members AC and DB actually experience **41.67 kN** of compression. This demonstrated why the external applied load cannot automatically be assumed to be the largest internal force in the structure.

Correcting the governing force changed the minimum required cross-sectional area of the members. Using the actual maximum internal force resulted in a required minimum area of **459.8 mm²**, which I then carried forward into the CAD design. Keeping a record of this correction helped me understand why the complete structural analysis needs to be finished before final member dimensions are selected.

**[INSERT ANY ADDITIONAL CAD OR DESIGN MISTAKES YOU ACTUALLY EXPERIENCED HERE]**

---

# Engineering Lessons Learned

One of the main things I learned from this project was how strongly truss geometry affects the forces carried by individual members. Even though each applied external load was only **25 kN**, the geometry caused members AC and DB to experience approximately **41.67 kN** of compression. This showed me that the force carried by a member cannot be determined from the external load alone and that the geometry and equilibrium of the complete structure have to be considered.

I also learned how material properties and safety factors translate directly into physical design dimensions. Instead of selecting the size of a member based on appearance, I used the maximum internal force, A500 steel yield strength, and a safety factor of 3.5 to determine the minimum required cross-sectional area. I applied the same process to the connecting pins using shear stress and a safety factor of 4, which gave me a minimum pin diameter of **10.42 mm**.

Another lesson I learned was the importance of maintaining consistency between analytical calculations and CAD. The CAD model is based on the assumptions and dimensions used in the hand calculations, so changing the geometry in CAD without updating the structural analysis would make the comparison invalid. Comparing the CAD mass properties with my hand-calculated weight gave me another way to check whether my model accurately represented the design I analyzed.

---

# Time Spent

The part of the project that required the most time was **[INSERT TASK]** because **[BRIEFLY EXPLAIN WHY]**. Tracking my time also showed me where corrections or revisions added additional work to the design process.

---

# CAD Files

Below I have included a download link containing the completed CAD files for my truss design. The files include the final truss model, connecting pin model, and any additional files required to open or reproduce the completed design.

**[INSERT CAD FILE DOWNLOAD LINK HERE]**

I tested the link from the live portfolio page to make sure that the files can be downloaded and opened independently.

---

# Final Design Summary

The final truss was designed for two **25 kN** applied loads using A500 steel members and hardened tool-steel connecting pins. The structural analysis resulted in a maximum internal member force of **41.67 kN**, which required a theoretical minimum member cross-sectional area of **459.8 mm²** when using a safety factor of 3.5. The single-shear pin analysis resulted in a minimum pin area of **85.32 mm²** and a minimum pin diameter of **10.42 mm** using a safety factor of 4.

The analytical truss mass was approximately **13.36 kg**, before accounting for differences caused by the final CAD geometry and selected standard dimensions. I used the calculated minimum dimensions as design limits when creating the CAD model and then compared the CAD mass properties with my hand calculations. This process allowed me to move from an initial geometric concept to a design supported by equilibrium, stress calculations, safety factors, material properties, and CAD verification.
