# A10 – Lead Screw Translating System

## Objective
Our goal was to design a benchtop tensile tester that uses two leadscrews to apply up to 2 kN to a specimen. The crosshead must move at 1–50 mm/min, deflect no more than 0.100 mm under load, and operate mechanically. We used a design factor of 4 when sizing the load-bearing components.

## Analyze
### Leadscrew Diameter, Speed, and Torque ([George])

We assumed the specimen was centered, so each leadscrew carries 1,000 N of the 2,000 N load. We selected two 18 in long, 3/8–12 right-hand precision Acme leadscrews made from 1018 steel. Using the catalog lead of 0.083 in/rev, the screws need to turn at approximately **0.474–23.72 rpm** to meet the crosshead speed range. Our preliminary raising torque was **8.76 lbf·in per screw**, before bearing and drivetrain losses.

During our calculation review, we found that the original axial sizing applied the factor of safety twice. We can apply the factor to the service load or divide the material strength by it. The screw’s actual root diameter and material strength still need to be confirmed for the final strength check.

### Nut and Flange ([George])

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
### Concept Selection ([Team])

We used a Pugh matrix to compare three ways to drive the two leadscrews together. The roller chain was the baseline. A `+` means better than the baseline, `0` means comparable, and `−` means worse.

| Selection criterion | Roller chain (baseline) | Timing belt | Cross-shaft with bevel gears |
| --- | :---: | :---: | :---: |
| Synchronizes both leadscrews at a 1:1 ratio | 0 | 0 | 0 |
| Can meet the 1–50 mm/min target with suitable crank gearing | 0 | 0 | 0 |
| Smooth motion at low speed | 0 | + | + |
| Ease of assembly and alignment | 0 | 0 | − |
| Low routine maintenance | 0 | + | − |
| **Net score** | **0** | **+2** | **−1** |

The timing belt scored highest because it provides smooth low-speed motion and requires no chain lubrication. A toothed belt and two equal-size pulleys would turn the screws at the same rate, allowing both sides of the crosshead to advance together. The crosshead places the screw centers 152.40 mm apart, with the specimen grip centered between them.

Our Pugh matrix compared a roller chain, a timing belt, and a cross-shaft with bevel gears as ways to synchronize the two leadscrews. We evaluated each option based on synchronization, ability to meet the crosshead speed range, smoothness at low speed, ease of assembly and alignment, and maintenance. We selected the timing-belt drive because it earned the highest score (+2), with advantages in low-speed smoothness and routine maintenance.

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

[Download the Crosshead Drawing](https://github.com/igarayal/Alzamora-MEGR2156-Portfolio/blob/main/docs/assignments/A10/A10-Crossheadfinal.SLDDRW)
[Download the Crosshead Part](https://github.com/igarayal/Alzamora-MEGR2156-Portfolio/blob/main/docs/assignments/A10/A10-Crossheadfinal.SLDDRW)

### Tabulating Costs ([Eva Stewart])

| Item Number | Quantity | Name             | Cost/Item | Cost    | Purchase Link |
|:-----------:|:--------:|------------------|:---------:|:-------:|---------------|
| 1           | 2        | ⅜”-12 Leadscrew  | $17.04    | $34.08  | [Leadscrew](https://www.mcmaster.com/99030A992/) |
| 2           | 2        | ⅜”-12 Nut        | $32.18    | $64.36  | [Nut](https://www.mcmaster.com/95072A108/) |
| 3           | 2        | 9/16”-18 Flange  | $37.06    | $74.12  | [Flange](https://www.mcmaster.com/95082A641/) |
| 4           | 4        | 2' Frame         | $38.12    | $152.48 | [Frame](https://www.mcmaster.com/4658N31-4658N33/) |
| | | **Verified subtotal** | | **$325.04** | |


### Lessons Learned ([Isabella])

We learned that the screw, nut, and flange each determine a different part of the design. The screw lead sets the rotational speed, the nut threads transfer the axial force, and the flange bolt circle sets the crosshead hole pattern. We also learned that stiffness can determine the plate thickness even when the bending stress is well below the allowable stress. In our design, the deflection check required **15.07 mm**, compared with **10.08 mm** for bending strength.

**Time spent** - 5 hours
