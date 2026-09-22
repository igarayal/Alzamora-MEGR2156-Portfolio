# A5 – Bracket Design

## Objective
For this assignment, I designed a bracket to support a horizontal load applied by a polyester strap. I used a design load of 650 lbf with a safety factor of 4. The bracket was separated into five features: the retention pin (A), connecting gusset (B), T-beam span (C), flange (D), and web (E).

Each feature was analyzed for both strength and stiffness using a maximum allowable deflection of 0.005 in. The two results were then compared to determine which requirement governed the final dimensions.

## Analyze
I selected Aluminum 6061-T6 with a yield strength of 35,000 psi and a modulus of elasticity of 10 × 10⁶ psi. Using a safety factor of 4 gave an allowable stress of 8,750 psi.

I selected aluminum because it provides enough strength for the required load while remaining lightweight and easy to manufacture. I assumed the bracket was loaded symmetrically, shear deflection was negligible, and direct shear failure would not occur as stated in the assignment.

## Decide
After comparing the stress and stiffness calculations, stress governed all five features. I rounded each required dimension upward to a practical size for the final CAD model.

The final dimensions were:

Feature A: (d_A = 0.9375) in.
Feature B: (t_B = 0.09375) in., (w_B = 0.9375) in.
Feature C: (h_C = 0.6875) in.
Feature D: (t_D = 0.625) in.
Feature E: (s_E = 0.3125) in.

Feature C was the closest comparison between stress and stiffness. Stress required approximately 0.668 in., while stiffness required approximately 0.593 in., making the two results about 13% apart.

## Communicate
I documented the stress and stiffness analysis for all five features and created two multiview sketches showing the dimensions determined from each method. The final CAD model was created using the governing stress-based dimensions.

INSERT CAD IMAGE

CAD FILE DOWNLOAD LINK: INSERT

Multiview Sketches
Stress Analysis Sketch

INSERT

Stiffness Analysis Sketch

INSERT

Lessons Learned
Governing Failure Mode

Stress governed the final dimension for every feature. Feature C was the closest comparison, with stress requiring 0.668 in. and stiffness requiring 0.593 in. This showed that a small change in span length or loading could cause stiffness to become the governing requirement.

Error Propagation

The reaction from Feature A is carried through the remaining features. Because of this, an incorrect force or moment calculated early in the analysis could affect every feature that follows. I checked equilibrium at each stage to make sure the 650 lbf load was transferred correctly.

Assumption Sensitivity

One important assumption was using 6061-T6 aluminum. Changing to steel would not greatly change the stress-based dimensions because the yield strengths are similar, but the larger modulus of elasticity of steel would reduce the stiffness-based dimensions. Since stress controlled this design, aluminum allowed the bracket to remain lighter while still meeting the requirements.

Mistakes

One important correction during the design process was making sure each feature used the correct structural model and moment arm. Using the wrong beam model or load location would significantly change the resulting dimensions.

I also checked that the safety factor was only applied once through the allowable stress calculation and that all calculations remained in consistent units.

I spent approximately INSERT HOURS completing the calculations, sketches, CAD model, and documentation.

