# EO/Thermal Tracking Demonstrator

Safe tabletop electro-optical/thermal tracking and control-surface demonstrator for aerospace engineering portfolio development.

## Project Scope

This project explores perception, controls, embedded systems, CAD, test procedures, data logging, and safety through a non-flying bench rig. The demonstrator will use visible-camera object tracking or thermal target tracking to estimate x/y target error and drive servos or control surfaces on a constrained tabletop setup.

## System Concept

The rig is a stationary bench demonstrator. A camera or thermal sensor observes a controlled target in the workspace, software estimates the target center error from the image frame center, and a microcontroller or companion computer commands servos on a gimbal or fin-control fixture.

```text
Target -> Camera/Thermal Sensor -> Tracking Pipeline -> x/y Error
      -> Controller -> Servo Driver -> Tabletop Gimbal or Control Surface
      -> Data Log -> Plots and Test Report
```

## Skills Demonstrated

- Computer vision or thermal target sensing
- Coordinate frames and pixel-to-error estimation
- Embedded servo control
- Closed-loop control tuning
- Fusion 360 CAD and mechanical packaging
- Bench testing, data logging, and engineering documentation
- Safety-minded aerospace systems thinking

## Safety Boundary

This repository is limited to a non-flying educational demonstrator. It does not include weaponization, propulsion, guidance-to-impact behavior, or operational deployment guidance.

## Repository Layout

```text
cad/         Fusion 360 exports, drawings, and mechanical notes
docs/        Requirements, architecture, test plans, and reports
firmware/    Microcontroller code for servo control and logging
images/      Photos, CAD renders, diagrams, and result plots
perception/  Tracking pipeline experiments and calibration scripts
safety/      Safety constraints, bench procedures, and risk notes
test-data/   Logged bench-test data and analysis outputs
```

## Planned Milestones

1. Define system requirements and safety constraints.
2. Build initial camera or thermal sensor tracking pipeline.
3. Design tabletop gimbal/control-surface rig in CAD.
4. Implement servo control and data logging.
5. Tune and test closed-loop response on the bench.
6. Document results with plots, photos, CAD renders, and lessons learned.

## Current Status

Project initialized. Requirements, safety notes, and first bench-test plan are being drafted before hardware selection.
