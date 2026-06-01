# Bench Test Plan

## Purpose

Verify that the tabletop demonstrator can estimate target error, command constrained servo motion, and log useful data without creating a flight-capable or hazardous system.

## Test Environment

- Stationary tabletop setup
- Low-voltage bench power
- Servo motion mechanically limited
- Clear workspace around moving parts
- Manual power disconnect available

## Initial Tests

1. Sensor frame capture
   - Confirm image or thermal frame acquisition.
   - Save representative frames for documentation.

2. Target error estimation
   - Place target at known positions in the frame.
   - Record estimated x/y error.
   - Compare against expected direction and relative magnitude.

3. Servo neutral and limits
   - Command neutral position.
   - Sweep within conservative limits.
   - Confirm no binding, cable snagging, or overheating.

4. Open-loop command logging
   - Send scripted commands.
   - Log command, timestamp, and measured/estimated response.

5. Closed-loop bench tracking
   - Enable low-gain control.
   - Move target slowly within the controlled bench area.
   - Record target error and servo command.

## Pass Criteria

- Tracking output is stable enough for control experiments.
- Servo motion remains within mechanical and software limits.
- Logs contain enough information to reproduce plots.
- No unsafe motion, overheating, or uncontrolled behavior occurs.

