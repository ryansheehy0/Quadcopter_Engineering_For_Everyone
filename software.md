# Software
- Overview of a simple flight controller


- Graph to explain integrals
	- x axis is time and y axis is velocity.
	- Get position
- Micro-controllers have small increments.
- Give example of simple code
- Instead of linear distance it's used to find orientation around an axis.
- 


- Explain integrals and reiman sum
	- Computers us riman sum
- Implement that in code with velocity exampl
- Explain dead recknoning with boats and have to corrct for errors from an outside source
- Introduce the IMU with gyro to get angle and then acc and magnometer to correct for errors.
	- Explain acro mode vs stabalized mode
- Explain full loop of drone
	- Calcualte delta time
	- Get info from IMU
	- Estimate angl of the drone
	- Get controller input
	- Feed into PIDs
	- Motor mixing
- Explain PIDs and how each variabl controls the shap of the graph
- Explain flight controllers vs flight computers
- Building is much harder. 90% safe, but last 10% with props is dangerous.

## PIDs
- Explain feedback loops with the example of the temp in a shower.
- When there's a delay in the measurement, then there's osculations.
- PIDs are there to explain this.

- You could just wait for the delay to end.