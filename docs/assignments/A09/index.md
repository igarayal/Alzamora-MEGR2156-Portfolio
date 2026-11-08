# A9 – Pulleys

## Objective
The objective of this assignment was to design a belt-driven pulley system capable of transferring rotational power between two parallel shafts while maintaining a minimum factor of safety of 3.

For my design, I selected two 3-inch diameter aluminum pulleys with a center-to-center distance of 5 inches, an operating speed of 1500 rpm, and an initial static belt tension of 5 lbf.

I applied principles of belt friction, normal stress, torsional shear stress, bearing pressure, and structural mechanics to determine the required component dimensions. I also developed a 3D CAD model to visualize the pulley system and its supporting components.

## Analyze
### Part 1: Belt Selection and Analysis

I started by identifying the knowns and unknowns and creating a free-body diagram (FBD) of the pulley system. I used the belt friction equation to calculate the tight-side and loose-side tensions, assuming a coefficient of friction of 0.30 and a wrap angle of 180 degrees.

I then applied the normal stress equation and the polyurethane rubber yield strength of 471 psi to determine the minimum belt cross-sectional area and diameter.

#### Belt Analysis Results

| Parameter | Calculated Value |
|---|---|
| Pulley diameter | 3 in |
| Center-to-center distance | 5 in |
| Static belt tension | 5 lbf |
| Tight-side tension | 7.196 lbf |
| Loose-side tension | 2.804 lbf |
| Maximum transmitted torque | 6.588 lbf·in |
| Minimum cross-sectional area | 0.0458 in² |
| Minimum belt diameter | 0.242 in |
| Selected belt diameter | 0.250 in |
| Tensile factor of safety | 3.21 |

Based on these calculations, I selected a 1/4-inch diameter polyurethane round belt from McMaster-Carr.

The calculated nominal belt pitch-path length was approximately 19.425 inches. I initially considered selecting a belt based only on its geometric circumference, but realized that installation strain was also necessary to generate sufficient static pretension.

To account for this, I evaluated a shorter 19-inch circumference belt. The selected diameter satisfies the preliminary tensile-strength requirement, although the actual installation tension and slip resistance would require further verification.

#### Handwritten Calculations

![Belt Calculations](images/belt-calculations.jpg)

*Figure 1: Belt friction, tension, minimum cross-sectional area, and diameter calculations.*

![Belt FBD](images/belt-fbd.jpg)

*Figure 2: Free-body diagram showing the forces acting on the belt and pulleys.*

### Part 2: Shaft Design

For the shaft design, I selected 1060 hardened steel and calculated the minimum diameter required to transmit torque without exceeding the allowable torsional shear stress.

I began by developing a shaft FBD showing the applied torque, belt forces, and bearing reactions. I then used the torsion equation for a solid circular shaft and the maximum-shear-stress criterion to determine the required shaft diameter.

#### Shaft Analysis Results

| Parameter | Calculated Value |
|---|---|
| Shaft material | 1060 hardened steel |
| Maximum transmitted torque | 6.588 lbf·in |
| Assumed yield strength | 44,700 psi |
| Allowable shear stress | 7,450 psi |
| Minimum shaft diameter | 0.165 in |
| Selected shaft diameter | 0.250 in |
| Torsional shear stress | 2,147 psi |
| Torsional factor of safety | 10.41 |

I selected a standard 1/4-inch diameter shaft because it exceeds the calculated minimum diameter and provides additional torsional strength.

The selected shaft meets the minimum factor of safety under pure torsion. However, a complete shaft analysis would also need to consider bending stresses, bearing reactions, and combined loading.

#### Handwritten Calculations

![Shaft Calculations](images/shaft-calculations.jpg)

*Figure 3: Shaft torque, minimum diameter, and torsional shear stress calculations.*

![Shaft FBD](images/shaft-fbd.jpg)

*Figure 4: Free-body diagram showing the applied torque and shaft support reactions.*

### Part 3: Journal Bearing Design

Next, I evaluated journal bearings to support the rotating shafts while maintaining proper alignment and minimizing friction.

Using an assumed radial bearing load of 5 lbf, a shaft diameter of 0.250 inches, and a bearing length of 0.500 inches, I calculated the projected bearing area, bearing pressure, surface velocity, and pressure-velocity (PV) rating.

#### Journal Bearing Analysis Results

| Parameter | Calculated Value |
|---|---|
| Shaft diameter | 0.250 in |
| Bearing length | 0.500 in |
| Rotational speed | 1500 rpm |
| Assumed radial load | 5 lbf |
| Projected bearing area | 0.125 in² |
| Bearing pressure | 40 psi |
| Surface velocity | 98.17 ft/min |
| PV rating | 3,927 psi·ft/min |

Based on these results, I selected oil-impregnated sintered bronze as the preliminary bearing material because of its self-lubricating properties and suitability for rotating-shaft applications.

The calculated pressure and PV rating would need to be compared with the allowable operating limits in Machinery's Handbook to verify the material selection.

#### Handwritten Calculations

![Bearing Calculations](images/bearing-calculations.jpg)

*Figure 5: Journal bearing pressure, surface velocity, and PV calculations.*

![Bearing FBD](images/bearing-fbd.jpg)

*Figure 6: Free-body diagram showing the radial bearing load and support reaction.*

### Part 4: Frame Design and Structural Analysis

For the support frame, I selected 6061-T6 aluminum because of its strength-to-weight ratio, corrosion resistance, and machinability.

I designed a rounded rectangular frame with two bearing openings separated by 5 inches to maintain the required center-to-center distance between the shafts.

#### Frame Dimensions

| Parameter | Selected Value |
|---|---|
| Material | 6061-T6 aluminum |
| Overall length | 7 in |
| Width | 1.5 in |
| Thickness | 0.25 in |
| Shaft center-to-center distance | 5 in |
| Number of bearing openings | 2 |

For the preliminary structural analysis, I assumed an axial compressive load of 10 lbf and calculated the nominal cross-sectional area, average compressive stress, and factor of safety.

#### Frame Analysis Results

| Parameter | Calculated Value |
|---|---|
| Applied compressive load | 10 lbf |
| Cross-sectional area | 0.375 in² |
| Average compressive stress | 26.67 psi |
| Assumed aluminum yield strength | 35,000 psi |
| Direct-stress factor of safety | 1312.5 |

The frame satisfies the minimum factor of safety under the simplified axial compression model. However, additional analysis would be required to evaluate bending stresses, stress concentrations around the bearing openings, and overall structural stability.

#### Handwritten Calculations

![Frame Calculations](images/frame-calculations.jpg)

*Figure 7: Frame cross-sectional area, compressive stress, and safety factor calculations.*

## Decide
Based on my engineering analysis, I selected two 3-inch diameter aluminum pulleys, a 1/4-inch polyurethane round belt, 1/4-inch 1060 hardened steel shafts, oil-impregnated sintered bronze journal bearings, and a 6061-T6 aluminum support frame.

| Component | Selected Design |
|---|---|
| Driving pulley | 3-inch diameter aluminum |
| Driven pulley | 3-inch diameter aluminum |
| Belt | 1/4-inch polyurethane rubber |
| Preliminary belt circumference | 19 in |
| Shafts | 1/4-inch diameter 1060 hardened steel |
| Journal bearings | Oil-impregnated sintered bronze |
| Support frame | 6061-T6 aluminum |
| Frame dimensions | 7 × 1.5 × 0.25 in |
| Center-to-center distance | 5 in |
| Operating speed | 1500 rpm |

I selected standard belt and shaft diameters that exceeded their calculated minimum values to provide additional strength while maintaining practical manufacturing dimensions.

The journal bearing material was selected based on its friction and lubrication properties, while the frame was designed to maintain shaft alignment and the specified center distance.

These components satisfy the preliminary strength calculations, although further analysis would be required to verify belt pretension, bearing specifications, and combined shaft loading.

## Communicate

After completing the calculations, I developed a preliminary 3D CAD model of the pulley system using SolidWorks-compatible STEP geometry.

I started by modeling the aluminum support frame with a rounded rectangular profile and two bearing openings separated by 5 inches.

Next, I modeled the two 3-inch diameter pulleys with circumferential grooves for the polyurethane round belt. Each pulley was designed with a central shaft opening.

I then added the steel shafts and sleeve bearings before positioning the components to represent the complete pulley assembly.

### Step 1: Support Frame

The frame was designed with an overall length of 7 inches, a width of 1.5 inches, and a thickness of 0.25 inches.

The bearing openings were positioned along the longitudinal centerline to maintain the required 5-inch spacing.

![Frame Sketch](images/frame-sketch.png)

*Figure 8: Dimensioned sketch of the aluminum support frame.*

![SolidWorks Frame](images/solidworks-frame.png)

*Figure 9: Isometric CAD model of the aluminum frame.*

### Step 2: Pulley Geometry

Each pulley was modeled with a 3-inch outside diameter and a circumferential groove to accommodate the round belt.

A central bore was included to accommodate the 1/4-inch diameter shaft.

![SolidWorks Pulley](images/solidworks-pulley.png)

*Figure 10: Pulley geometry showing the belt groove and shaft bore.*

### Step 3: Final Assembly

After modeling the individual components, I positioned the pulleys, shafts, bearings, and belt relative to the aluminum frame.

The assembly maintains a 5-inch center distance between the two pulley axes.

![Final Pulley Assembly](images/final-pulley-assembly.png)

*Figure 11: Complete pulley system showing the pulleys, belt, shafts, bearings, and support frame.*

The CAD model represents the preliminary component geometry. Further development would be necessary to finalize bearing fits, shaft retention, belt installation tension, and mounting details.

### Design Challenges and Modifications

One challenge I encountered was determining the appropriate belt circumference. Initially, I focused on matching the calculated geometric belt length, but realized that installation strain was necessary to develop sufficient initial tension.

I also had to distinguish between the theoretical minimum shaft diameter and a practical standard diameter. Although the minimum calculated diameter was approximately 0.165 inches, I selected a 0.250-inch shaft to increase the torsional safety margin.

Another design consideration was maintaining accurate shaft alignment and center spacing within the frame while allowing enough clearance for the rotating components.

Throughout this assignment, I developed a better understanding of how belt friction and the difference between tight-side and loose-side tensions influence torque transmission.

I learned how to apply torsional shear stress equations to determine the minimum shaft diameter and how bearing pressure, surface velocity, and PV ratings affect journal bearing selection.

During the belt selection process, I learned that tensile strength and geometric circumference alone are insufficient to determine belt performance. Installation strain, static pretension, and friction must also be considered to reduce the risk of slipping.

The frame analysis also demonstrated the importance of structural stiffness, load distribution, and shaft alignment.

Overall, this assignment helped me understand how engineering calculations and SolidWorks modeling can be used together to make mechanical design decisions. I spent approximately 6 hours completing the initial calculations, component selection, and documentation. Additional time was spent developing the CAD model.
