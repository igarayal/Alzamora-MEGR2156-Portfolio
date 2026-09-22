# A5 – Bracket Design

## Objective
For this assignment, I designed a bracket to support a horizontal load applied by a polyester strap. I used a design load of 650 lbf with a safety factor of 4. The bracket was separated into five features: the retention pin (A), connecting gusset (B), T-beam span (C), flange (D), and web (E).

Each feature was analyzed for both strength and stiffness using a maximum allowable deflection of 0.005 in. The results were compared to determine which requirement governed the final dimensions.

## Analyze
I selected Aluminum 6061-T6 with a yield strength of 35,000 psi and a modulus of elasticity of 10 × 10⁶ psi. Using a safety factor of 4 gave an allowable stress of:

$$ \sigma_{allow}=8,750\text{ psi} $$

Aluminum was selected because it provides sufficient strength while remaining lightweight and easy to manufacture. I assumed the bracket was loaded symmetrically, shear deflection was negligible, the material remained linearly elastic, and direct shear failure would not occur as stated in the assignment.

## Decide
After comparing the stress and stiffness calculations, stress governed all five features. Each required dimension was rounded upward to a practical size for the final CAD model.

The final dimensions were:

Feature A: \(d_A = 0.9375\) in.
Feature B: \(t_B = 0.09375\) in., \(w_B = 0.9375\) in.
Feature C: \(h_C = 0.6875\) in.
Feature D: \(h_D = 0.625\) in.
Feature E: \(s_E = 0.3125\) in.

Feature C was the closest comparison between stress and stiffness. Stress required approximately 0.668 in., while stiffness required approximately 0.593 in., a difference of about 13%.

## Communicate
I documented the stress and stiffness analysis for all five features and created two multiview sketches showing the dimensions determined by each method. The final CAD model was created using the governing stress-based dimensions.

INSERT CAD IMAGE

https://github.com/igarayal/Alzamora-MEGR2156-Portfolio/blob/main/docs/assignments/A05/A5%20Bracket%20final.SLDPRT

Multiview Sketches
Stress Analysis Sketch

INSERT

Stiffness Analysis Sketch

INSERT

Lessons Learned
Governing Failure Mode

Stress governed the final dimension for every feature. Feature C was the closest comparison, with stress requiring 0.668 in. and stiffness requiring 0.593 in. This showed that a relatively small change in span length or loading could cause stiffness to become the governing requirement.

Error Propagation

The load and reactions determined for earlier features were used to analyze later features. Because of this, an incorrect force, reaction, or moment arm could affect multiple downstream calculations. I checked equilibrium at each stage to make sure the 650 lbf load was transferred consistently through the bracket.

Assumption Sensitivity

One important assumption was the use of 6061-T6 aluminum. Changing to steel would not greatly change the stress-based dimensions because the yield strengths are similar, but steel's higher modulus of elasticity would reduce the dimensions required by stiffness. Since stress governed this design, aluminum allowed the bracket to remain lighter while still satisfying the design requirements.

Mistakes

One important correction during the design process was making sure each feature used the correct structural model, load, and moment arm. For example, I corrected the dimensions used for Features B and D so that the calculations matched the final bracket geometry.

I also checked that the safety factor was applied only once through the allowable stress calculation and kept all calculations in consistent lbf, in., and psi units.

Time Spent

I spent approximately INSERT HOURS completing the calculations, sketches, CAD model, and documentation.

