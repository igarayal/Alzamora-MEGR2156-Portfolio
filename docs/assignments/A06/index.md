# A6 – Bracket

## Objective
For this assignment, I took the bracket I designed in the previous strength and stiffness assignment and developed it into a parametric SolidWorks model and a fully dimensioned, third-angle engineering drawing. The goal was to make the important dimensions respond to the engineering relationships that control the design instead of entering unrelated fixed values. I also focused on properly dimensioning and tolerancing the three sliding-fit interfaces where the bracket receives the rigid T-beam.

## Analyze
I began by reviewing the bracket geometry from the previous assignment and separating the dimensions that were controlled by strength or stiffness from the dimensions that were controlled by the mating T-beam geometry. I then organized the important values as SolidWorks parameters/global variables so that changes to the design inputs could update the corresponding model dimensions.
The biggest advantage of setting the model up this way is that the bracket can be modified without repeating the entire sizing process by hand. If a controlling variable changes, the related features can regenerate from the equations already built into the model.
[INSERT SCREENSHOT OF EQUATIONS / GLOBAL VARIABLES TABLE]
Parametric Model and Sketches
[INSERT SCREENSHOT OF COMPLETE PARAMETRIC MODEL]
Main Bracket Body
I first created the main body of the bracket because it establishes the overall size and provides the reference geometry for the other features. The surrounding dimensions were then tied to this geometry so that the model would remain consistent when parameters changed.
[INSERT MAIN BODY / BASE SKETCH SCREENSHOT]
T-Beam Interface
The T-beam interface was one of the most important sections of the model because it contains the three sliding-fit surfaces specified in the assignment. These dimensions could not be determined from strength alone because they also had to physically fit around the updated rigid T-beam geometry.
I sized the openings from the mating geometry and included the required clearance instead of treating the gap dimensions as arbitrary values.
[INSERT T-BEAM / SLOT SKETCH SCREENSHOT]
Upper Retaining Feature
The upper retaining portion of the bracket helps capture the rigid T-shaped member and keeps the bracket located during use. Because it is connected to the sliding interface, its dimensions were tied to the surrounding T-beam geometry instead of being modeled independently.
[INSERT UPPER FEATURE SCREENSHOT]
Center Web
The web transfers load between the upper interface and the lower portion of the bracket. I kept this feature connected parametrically to the main body so that changes in the surrounding bracket dimensions would not require the web to be rebuilt manually.
[INSERT WEB SKETCH SCREENSHOT]
Lower Load-Carrying Feature
The lower portion of the bracket provides the load-transfer area for the strap and connects the applied load to the rest of the bracket. This feature was modeled using the dimensions developed from the previous design analysis and the physical space required for the strap.
[INSERT LOWER FEATURE / STRAP INTERFACE SCREENSHOT]
Equation-Driven Dimension
One of the main requirements of this assignment was to drive at least one dimension directly from the analytical design relationship rather than calculating a number separately and typing that result into SolidWorks.
I used the strength/stiffness relationship from the previous assignment to control one of the structural dimensions of the bracket. I entered the design variables as SolidWorks global variables and connected the resulting dimension through an equation in the model.
[INSERT SCREENSHOT OF THE SOLIDWORKS EQUATION]
Because this dimension was equation-driven, a change to the controlling input changed the model dimension through the SolidWorks relation rather than requiring me to manually recalculate and replace the dimension.

## Decide
With the equations in place, I checked each calculated dimension against the physical fit requirements of the bracket. A dimension that satisfies a strength or stiffness equation can still be too small for the mating geometry, so the final values had to satisfy both structural performance and assembly.
I also selected tolerances based on function rather than using the tightest tolerance everywhere.
Tolerance Class Per Dimension
The three T-beam gap dimensions received tighter tolerances because they are functional mating surfaces. Their dimensions directly affect whether the bracket can slide over the rigid T-beam without binding or excessive looseness.
For a critical mating dimension shown to three decimal places, I used the X.XXX ± .005 in tolerance class. For a non-critical dimension that does not control assembly, I used the looser X.X ± .02 in tolerance class.
Holding every feature to ±.005 in would unnecessarily increase manufacturing difficulty and inspection requirements without improving the performance of non-critical features.
The general tolerance block on the drawing is:
- X.X ± .02 in
- X.XX ± .01 in
- X.XXX ± .005 in

## Communicate
I created the final engineering drawing from the same parametric model and used third-angle projection. The Top view is above the Front view and the Right-side view is positioned to the right of the Front view. The drawing includes the dimensions needed to manufacture the bracket, the three sliding-fit tolerances, and the required general tolerance block.

Drawing
[INSERT IMAGE 7 — COMPLETE ENGINEERING DRAWING]

Lessons Learned
Mistakes and Corrections
One thing I learned was that a structurally acceptable dimension does not automatically guarantee that the mating geometry will fit. I had to compare the calculated dimensions with the minimum dimensions required by the rigid T-beam before finalizing the model.

I also learned the difference between simply entering dimensions and creating a truly parametric model. Connecting the important dimensions to global variables and equations allows the model to respond to design changes instead of requiring manual edits.
The drawing portion reinforced why tolerances should be selected based on function. The sliding-fit interfaces require tighter control because variation affects assembly, while non-critical dimensions can rely on the general tolerance block.

I used the analytical relationship from my previous strength/stiffness analysis to control a structural bracket dimension directly inside SolidWorks. The controlling values were entered as global variables and linked to the model through an equation rather than typing in a hand-calculated result.

When a controlling input changes, the linked dimension updates through the equation and the features that reference it regenerate with the model. This reduces manual rework and keeps the CAD model connected to the engineering analysis.

It took me approximately 6 hours to complete the parametric model, drawing, tolerancing, revisions, and documentation.

Download Final Bracket CAD File
MEGR2156_FINAL_Synced_Bracket.step.SLDPRT
