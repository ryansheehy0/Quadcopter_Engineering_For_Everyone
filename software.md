# Software
- Overview of a simple flight controller

- Use graph to explain integrals and reiman sum.
	- x-axis: time
	- y-axis: velocity
	- Used to get position
	- Computers use reiman sums not integrals
- Give example of code for velocity

```
function currentTime()
function currentVelocity()

main
	prevTime = currentTime()
	position

	while
		deltaTime = currentTime() - prevTime
		prevTime = currentTime()

		position += currentVelocity * deltaTime
```

- This is known as dead reckoning. This was originally used with boards.
	- Problem. Errors accumulate so you have to corret for those erros with an outside source, like stars in the night sky.
- Introduce the IMU with gyro to get the angle and then accelerometer and magnometer to correct for errors.
	- Explain acro mode vs stablized mode
	- Instead of linear distance it's used to find orientation around an axis.
- Explain full loop of drone
	- Calcualte delta time
	- Get info from IMU
	- Estimate angl of the drone
	- Get controller input
	- Feed into PIDs
	- Motor mixing
- Explain PIDs and how each variabl controls the shap of the graph
- Explain flight controllers vs flight computers

## PIDs
- Explain feedback loops with the example of the temp in a shower.
- When there's a delay in the measurement, then there's osculations.
- PIDs are there to explain this.

- You could just wait for the delay to end.