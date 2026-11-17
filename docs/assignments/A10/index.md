# A10 – Lead Screw Translating System

## Objective
Our goal was to design a benchtop tensile tester that uses two leadscrews to apply up to 2 kN to a specimen. The crosshead must move at 1–50 mm/min, deflect no more than 0.100 mm under load, and operate mechanically. We used a design factor of 4 when sizing the load-bearing components.

## Analyze
### Leadscrew Diameter, Speed, and Torque ([Team member])

We assumed the specimen was centered, so each leadscrew carries 1,000 N of the 2,000 N load. We selected two 18 in long, 3/8–12 right-hand precision Acme leadscrews made from 1018 steel. Using the catalog lead of 0.083 in/rev, the screws need to turn at approximately **0.474–23.72 rpm** to meet the crosshead speed range. Our preliminary raising torque was **8.76 lbf·in per screw**, before bearing and drivetrain losses.

During our calculation review, we found that the original axial sizing applied the factor of safety twice. We can apply the factor to the service load or divide the material strength by it. The screw’s actual root diameter and material strength still need to be confirmed for the final strength check.

### Nut and Flange ([Team member])

We paired each leadscrew with a **95072A108 bronze nut** and a **95082A641 steel flange**. The nut’s internal 3/8–12 Acme thread fits the screw. Its external 9/16–18 thread attaches it to the flange. For the 5/8 in nut, our equal-load thread-bending model gives approximately **2.57 ksi at the 1,000 N service load**. The flange’s **1-1/8 in bolt circle** sets the mounting hole pattern on the crosshead.

### Crosshead Strength and Deflection ([Isabella])
<img width="400" height="400" alt="Screenshot 2026-11-16 191838" src="https://github.com/user-attachments/assets/d45a9651-1874-47eb-9cfa-2b8ceacc322a" />
<img width="400" height="400" alt="Screenshot 2026-11-16 191846" src="https://github.com/user-attachments/assets/02f15f53-71eb-4a06-b0bb-b439d9deb649" />
<img width="400" height="400" alt="Screenshot 2026-11-16 191856" src="https://github.com/user-attachments/assets/2cca395a-1887-4d66-9edb-1fef61e9a321" />
<img width="400" height="400" alt="Screenshot 2026-11-16 191905" src="https://github.com/user-attachments/assets/65713ebe-1850-4745-8bac-c973e3abae1f" />
<img width="400" height="400" alt="Screenshot 2026-11-16 191912" src="https://github.com/user-attachments/assets/4d5ce70a-1206-46dc-86b3-6c27f5d3dc15" />

We modeled the crosshead as a simply supported beam. The specimen pulls down with **2,000 N** at the center grip, and each nut and flange supports the plate with an upward reaction of **1,000 N**. We used a **152.40 mm span** between the screw centers and a conservative **75 mm effective width** to account for the screw and mounting holes.

| Design check | Minimum thickness | Result for 20 mm plate |
| --- | ---: | ---: |
| Bending strength | 10.08 mm | 15.24 MPa bending stress and 15.75 bending safety factor |
| Deflection | 15.07 mm | 0.0428 mm center deflection |

## Decide
### Concept Selection ([Team member])

Our Pugh matrix compared **[list the concepts your team evaluated]** using criteria that included **[insert your team's criteria]**. We selected the **dual-leadscrew concept** because **[insert the deciding criterion or result from your matrix]**.

The design follows this decision by placing one screw on each side of the centered specimen. This gives the crosshead two symmetric support points and lets both sides advance together when the screws are synchronized. The bronze nuts and bolt-on steel flanges connect the crosshead to the screws.

We selected a **304.80 × 101.60 × 20.00 mm 6061-T6 aluminum crosshead**. Deflection required more thickness than bending strength, so we used the stiffness calculation to guide the plate thickness. The 20 mm plate gives a predicted beam deflection of 0.0428 mm, below the 0.100 mm limit.

## Communicate
### Crosshead Drawing and CAD ([Isabella])

The crosshead has two **Ø10.50 mm through-holes** for the leadscrews, spaced **152.40 mm** apart. Each screw hole is surrounded by four **Ø6.60 mm mounting holes** on a **Ø28.575 mm bolt circle**. The **Ø13.00 mm center hole** is for the proposed grip adapter. Both steel flanges seat against the underside of the crosshead.

<img width="400" height="400" alt="Screenshot 2026-11-16 193857" src="https://github.com/user-attachments/assets/cc694573-4861-430f-b760-c95507cd9e87" />
<img width="400" height="400" alt="Screenshot 2026-11-16 194343" src="https://github.com/user-attachments/assets/4532b707-6c3b-40e8-9c73-0168b4733a8f" />
<img width="400" height="400" alt="Screenshot 2026-11-16 194444" src="https://github.com/user-attachments/assets/1694a951-624c-4066-a27f-20b00b794870" />
<img width="400" height="400" alt="Screenshot 2026-11-16 194508" src="https://github.com/user-attachments/assets/3dc346df-3711-438c-a2f6-fd298da23ba2" />
<img width="400" height="400" alt="Screenshot 2026-11-16 194910" src="https://github.com/user-attachments/assets/391361d8-1b92-486b-ae49-01073ff74e33" />
<img width="400" height="400" alt="Screenshot 2026-11-16 194925" src="https://github.com/user-attachments/assets/b9d07751-449d-4459-a186-3435a4e35a80" />
<img width="400" height="400" alt="Screenshot 2026-11-16 194951" src="https://github.com/user-attachments/assets/498185ef-9e23-4a22-b97e-2f0cda90851d" />

[Download the Crosshead](https://github.com/igarayal/Alzamora-MEGR2156-Portfolio/blob/main/docs/assignments/A10/A10-Crossheadfinal.SLDDRW)

### Tabulating Costs ([Team member])

| Item | Quantity | Purchased component | Cost per item | Extended cost | Purchase link |
| --- | ---: | --- | ---: | ---: | --- |
| 1 | 2 | 18 in precision Acme leadscrew, 99030A992 | Pending | Pending | [McMaster-Carr](https://www.mcmaster.com/99030A992/) |
| 2 | 2 | 673 bronze Acme nut, 95072A108 | Pending | Pending | [McMaster-Carr](https://www.mcmaster.com/95072A108/) |
| 3 | 2 | 1215 steel flange, 95082A641 | Pending | Pending | [McMaster-Carr](https://www.mcmaster.com/95082A641/) |
| 4 | 4 | 40 × 40 mm aluminum frame stock, 906T77 | $47.92 | $191.68 | [Grainger](https://www.grainger.com/product/80-20-T-Slot-Framing-System-Profiles-906T77) |
| | | **Verified subtotal** | | **$191.68** | |

### Lessons Learned ([Team member])

We learned that the screw, nut, and flange each determine a different part of the design. The screw lead sets the rotational speed, the nut threads transfer the axial force, and the flange bolt circle sets the crosshead hole pattern. We also learned that stiffness can determine the plate thickness even when the bending stress is well below the allowable stress. In our design, the deflection check required **15.07 mm**, compared with **10.08 mm** for bending strength.

**Actual time spent** — 
