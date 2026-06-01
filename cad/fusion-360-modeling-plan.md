# Fusion 360 Modeling Plan

This guide is for building the first tabletop CAD version of the EO/thermal tracking demonstrator. The goal is not to make a beautiful final assembly on day one. The goal is to create a simple, dimensioned, modifiable model that proves the rig can be mounted, moved, limited, and documented safely.

## Recommended First CAD Architecture

Start with a single-axis servo control-surface demonstrator before modeling a full pan/tilt gimbal.

Why:

- Fewer parts to model
- Easier to 3D print or fabricate
- Easier to test safely
- Still demonstrates aerospace-relevant control surfaces, servo linkage, CAD, and test planning

The first assembly should include:

- Base plate
- Vertical servo mount
- Servo body placeholder
- Servo horn placeholder
- Small control fin
- Mechanical travel stops
- Camera/sensor mounting block

## Suggested Starter Dimensions

These are placeholders. Update them after choosing the actual servo and camera.

| Part | Starting Dimension |
| --- | --- |
| Base plate | 180 mm x 120 mm x 6 mm |
| Servo body placeholder | 40 mm x 20 mm x 38 mm |
| Servo shaft height | 30 mm above base |
| Fin | 70 mm span x 40 mm chord x 3 mm thick |
| Sensor block | 35 mm x 35 mm x 20 mm |
| Mounting holes | M3 clearance, 3.2 mm diameter |

## Fusion 360 Setup

1. Open Fusion 360.
2. Create a new design.
3. Save it as `eo_tracking_demonstrator_v1`.
4. Set units to millimeters:
   - Browser panel
   - Document Settings
   - Units
   - Change Active Units to `mm`

## Step 1: Create Parameters

Use parameters so you can change dimensions later without rebuilding the model.

In Fusion:

1. Go to `Modify > Change Parameters`.
2. Add these user parameters:

| Name | Expression |
| --- | --- |
| base_length | 180 mm |
| base_width | 120 mm |
| base_thickness | 6 mm |
| servo_length | 40 mm |
| servo_width | 20 mm |
| servo_height | 38 mm |
| fin_span | 70 mm |
| fin_chord | 40 mm |
| fin_thickness | 3 mm |
| sensor_block | 35 mm |

## Step 2: Model the Base Plate

1. Create a new component named `Base Plate`.
2. Start a sketch on the XY plane.
3. Draw a center rectangle.
4. Set dimensions:
   - `base_length`
   - `base_width`
5. Finish sketch.
6. Extrude upward by `base_thickness`.
7. Add four mounting holes near the corners:
   - Diameter: 3.2 mm
   - Keep at least 10 mm from edges

## Step 3: Model the Servo Placeholder

1. Create a new component named `Servo Placeholder`.
2. Sketch a rectangle on the base top plane.
3. Dimension it:
   - `servo_length`
   - `servo_width`
4. Place it near the center of the base.
5. Extrude by `servo_height`.
6. Add a small cylinder on one face or top surface to represent the output shaft.
7. Rename the shaft feature clearly.

This does not need to match the final servo perfectly yet. It is a space claim.

## Step 4: Model the Fin

1. Create a new component named `Control Fin`.
2. Sketch a simple rectangle or tapered airfoil-like plate.
3. Start with:
   - Span: `fin_span`
   - Chord: `fin_chord`
4. Extrude by `fin_thickness`.
5. Add a center hole or hub feature where the servo horn will connect.

Keep the fin small and light for bench testing.

## Step 5: Add Mechanical Stops

1. Create two small blocks near the expected fin travel limits.
2. Place them so the fin cannot rotate far enough to hit wires, the sensor, or the base.
3. Use a conservative travel estimate first:
   - approximately +/- 30 degrees

Document these stops in screenshots. They are useful portfolio evidence because they show safety-minded design.

## Step 6: Add the Sensor Mount Block

1. Create a new component named `Sensor Mount`.
2. Place it at the front of the base plate.
3. Start with a simple block:
   - 35 mm x 35 mm x 20 mm
4. Add mounting holes later after choosing the camera or thermal sensor.

## Step 7: Create the First Assembly Screenshot

Create at least three images:

1. Isometric full assembly
2. Top view showing base layout
3. Side view showing servo and fin clearance

Save screenshots or renders into:

```text
images/
```

## What to Export

For the repo:

- Screenshot or render: `images/cad_v1_isometric.png`
- Fusion archive: `cad/eo_tracking_demonstrator_v1.f3d`
- Optional STEP export: `cad/eo_tracking_demonstrator_v1.step`

## First CAD Definition of Done

The first CAD version is complete when:

- Base plate exists with basic mounting holes.
- Servo placeholder exists and is dimensioned.
- Fin/control surface exists.
- Mechanical stops exist.
- Sensor mount placeholder exists.
- At least one CAD screenshot is saved.
- README or report can show the assembly and explain the design.

