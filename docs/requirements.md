# Requirements

## Objective

Build a safe, non-flying tabletop demonstrator that estimates target error from a visible or thermal sensor and commands servos on a constrained gimbal or control-surface rig.

## Functional Requirements

- Detect or track a controlled bench target in a camera or thermal sensor frame.
- Estimate horizontal and vertical target error relative to the frame center.
- Command servo positions from the estimated error using a documented control law.
- Log timestamped target error, command output, and servo position during tests.
- Provide a manual disable or power-off procedure during bench operation.

## Non-Functional Requirements

- Operate only as a stationary tabletop demonstrator.
- Keep moving parts guarded, low-energy, and easy to disconnect.
- Use repeatable bench tests with documented setup conditions.
- Make results understandable through plots, photos, and concise reports.

## Out of Scope

- Flight hardware
- Propulsion
- Weaponization
- Guidance-to-impact behavior
- Operational deployment guidance

