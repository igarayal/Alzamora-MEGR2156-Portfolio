# A6 – Bracket Drawing

## Objective

For this assignment, I took the bracket from A5 and developed it into a parametric SolidWorks model and a fully dimensioned engineering drawing using third-angle projection. The main goal was to connect the important bracket dimensions to the strength and stiffness relationships from the previous assignment instead of entering only fixed values. I also applied tolerances to the three sliding-fit interfaces where the bracket fits over the rigid T-beam.

## Analyze

I organized the bracket around a set of SolidWorks global variables so that the main dimensions could be controlled from the same design inputs used in A5.

The main design values used were:

- Load: 650 lbf
- Safety Factor: 4
- Yield Strength: 35,000 psi
- Modulus of Elasticity: 10,000,000 psi
- Maximum Deflection: 0.005 in
- Allowable Stress: 8,750 psi

I also carried over the final A5 dimensions for Features A through E.

[INSERT EQUATIONS / GLOBAL VARIABLES SCREENSHOT]

## Parametric Model And Sketches

[INSERT FULL BRACKET MODEL SCREENSHOT]

### C - Block

Feature C forms the main upper body of the bracket and contains the geometry that interfaces with the rigid T-beam.

The main span length was set to 4.00 in, and the final height used from the A5 stress analysis was 0.6875 in.

The analytical stress calculation gave a required value of approximately 0.668 in, so I rounded the final CAD dimension upward to 0.6875 in.

[INSERT C - BLOCK SCREENSHOT]

### T-Slot

The T-slot provides the sliding interface between the bracket and the rigid T-beam.

The pocket dimensions were controlled separately because these surfaces directly affect assembly. I treated the three T-beam contact dimensions as functional mating surfaces and applied tighter tolerances to them in the engineering drawing.

[INSERT T-SLOT SCREENSHOT]

### B - Gusset

Feature B is the connecting gusset between the main body and the lower section of the bracket.

The final dimensions from A5 were:

- Gusset thickness, t_B = 0.09375 in
- Gusset width, w_B = 0.9375 in

The gusset was included to transfer load between the upper block and the lower bracket features while limiting deformation.

[INSERT B - GUSSET SCREENSHOT]

### A - Pin

Feature A is the lower pin that supports the strap load.

The final pin diameter from the A5 strength analysis was:

d_A = 0.9375 in

The pin dimension was controlled by the bending-stress requirement and was rounded upward from the calculated value to a practical final dimension.

[INSERT A - PIN SCREENSHOT]

### D - Flange

Feature D forms the flange located between the web and the lower pin area.

The final flange height used in the CAD model was:

h_D = 0.625 in

This value was selected from the governing strength analysis completed in A5.

[INSERT D - FLANGE SCREENSHOT]

### E - Web

Feature E is the center web that transfers the load from the lower features into the upper bracket body.

The final web thickness was:

s_E = 0.3125 in

This dimension was controlled by the governing strength requirement from A5.

[INSERT E - WEB SCREENSHOT]

## Decide

After entering the A5 dimensions and equations into SolidWorks, I checked the model to make sure the calculated dimensions also satisfied the physical fit requirements of the bracket.

One important issue was that a dimension can satisfy the stress equation but still be too small for the mating T-beam. Because of this, the final dimensions had to satisfy both the structural requirement and the geometry needed for assembly.

I also selected tolerances based on the function of each feature instead of applying the tightest tolerance everywhere.

## Tolerance Class Per Dimension

The three T-beam pocket dimensions received explicit tolerances because they are functional mating surfaces.

These dimensions directly control the sliding fit between the bracket and the rigid T-beam. Too little clearance could prevent assembly, while too much clearance could allow excessive movement.

The drawing uses the required general tolerance block:

- X.X ± .02
- X.XX ± .01
- X.XXX ± .005

For a critical sliding-fit dimension, I used the tighter X.XXX ± .005 tolerance class.

For non-critical dimensions such as overall lengths or features that do not directly mate with another part, I allowed the general tolerance block to control the tolerance.

Using the tightest tolerance on every dimension would unnecessarily increase machining difficulty and inspection requirements without improving the function of the bracket.

## Communicate

I created the final engineering drawing directly from the SolidWorks model.

The drawing includes the necessary dimensions, the three sliding-fit tolerances, the general tolerance block, and a third-angle multiview layout.

The main purpose of the drawing was to clearly communicate which dimensions are critical to the bracket's function and which dimensions can use the general manufacturing tolerances.

## Drawing

The drawing was arranged using third-angle projection.

The Top view was placed above the Front view, and the Right-side view was placed to the right of the Front view.

I used projected views so that the views remained aligned with one another instead of manually positioning independent views.

[INSERT COMPLETE ENGINEERING DRAWING SCREENSHOT]

### Top View

The Top view shows the 4.00 in overall span and the layout of the upper T-beam interface.

### Front View

The Front view shows the main load path through the block, web, flange, and pin.

### Right View

The Right view shows the depth of the bracket and the three T-beam interface dimensions used for the sliding fit.

## Lessons Learned

### Mistakes and Corrections

One of the main lessons from this assignment was that the calculated strength requirement is not the only factor that controls the geometry.

For Feature C, the stress calculation produced a required height of approximately 0.668 in, while the final CAD dimension was rounded upward to 0.6875 in. I also had to make sure that the T-beam interface still physically fit inside the surrounding bracket geometry.

Another important lesson was the difference between a normal dimension and a parametric dimension. By entering the design values as global variables and equations, I could keep the analytical relationships connected to the CAD model instead of relying only on manually entered dimensions.

I also learned that tolerances should be assigned based on function. The three sliding-fit surfaces require tighter control because they directly affect assembly, while non-critical dimensions can use the general tolerance block.

### Equation-Driven Dimension

I used the Feature C bending-stress equation as the analytical relationship for the parametric portion of the model.

The bending moment was defined as:

M_C = (F × L_C) / 4

Using:

- F = 650 lbf
- L_C = 4.00 in

gave:

M_C = 650 lbf·in

The Feature C height was calculated from:

h_C = sqrt(6M_C / (b_C × sigma_allow))

Using an allowable stress of 8,750 psi gave a required height of approximately 0.668 in.

The final CAD dimension was rounded upward to:

h_C = 0.6875 in

I entered the design variables and calculation into the SolidWorks Equation Manager so that the relationship was documented directly in the CAD model.

## Time It Took

It took me approximately 6 hours to complete the parametric model, drawing, tolerancing, revisions, and documentation.

## CAD File

[Bracket.zip](INSERT-YOUR-GITHUB-BRACKET-ZIP-LINK-HERE)
