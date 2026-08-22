# Software
Let's say you have a graph of velocity.  
The X-axis is time, and the Y-axis is velocity.  
In calculus, you learned that you can find the position by taking the integral, which is the area under the curve.  
This area can be approximated by taking a bunch of thin rectangles and adding their areas together, called the Riemann sum.  
This approximation becomes more accurate as you use more rectangles.  

[Video animation of integrals](https://youtu.be/2qxrA-AfPq4?si=HPq4mXxtApntXE1X)

The flight controller does something similar, but instead of infinitely small rectangles, it uses very small time intervals, on the order of microseconds.  
Here's an example of pseudocode, which is used to explain concepts but isn't real code.  
If you don't understand code, just know that each line is its own instruction, and the instructions are executed from top to bottom, one line at a time.  

```
function getCurrentTime()
function getCurrentVelocity()

start of code
	prevTime = getCurrentTime()
	position = 0

	loop
		deltaTime = getCurrentTime() - prevTime
		prevTime = getCurrentTime()

		position = position + (getCurrentVelocity() * deltaTime)
```

This pseudocode will keep track of the robot's current position in one dimension.  
This is known as dead reckoning, which was originally used to keep track of the position of boats.  
For example, if you know your boat's current position on a map, how fast you're traveling, how long you've traveled, and your direction, you can keep track of your boat's current position.  

[Video explaining dead reckoning](https://youtu.be/Byf8T3mrnOM?si=0xAgoaIgmcPy4XyA)

The problem with dead reckoning is that errors accumulate over time.  
As time passes, the estimate of your position becomes less and less accurate.  
In order for this to be precise, you need to periodically reset your position using an outside reference, such as the stars in the night sky.  

[Video explaining how stars can be used for navigation](https://youtu.be/p7QbwG2_aM4?si=N60d-0Xef5XByPYQ)

For a drone, the same concepts apply.  
Instead of measuring velocity, the drone measures angular velocity from the gyroscope in the IMU (Inertial Measurement Unit).  
This angular velocity is added up, like in the pseudocode example, to estimate the current angular position of the drone.  
But the problem is that errors accumulate, so the estimate needs to be corrected using an outside reference.  
In this case, that outside reference is the direction of Earth's gravity, measured using the accelerometer in the IMU.  
With some trigonometry, you can determine the drone's current angle and correct for the gyroscope's accumulated error.  
But the accelerometer is very sensitive to bumps and vibrations, so it can't replace the gyroscope, just correct the errors.  

[Video explaining how IMU works](https://youtu.be/XH5rW4EhKIc?si=s4O85nO03ElpT0YC)

These are the main steps required in the flight controller's main loop:  
1. Calculate the delta time and set the previous time, as shown in the previous pseudocode.  
2. Get data from the IMU sensor.  
3. Estimate the drone's current angle using the deltaTime and gyroscope data, with a slight correction from the accelerometer.  
4. Get the user's input from the receiver.  
5. Use the drone's current angle and the user's inputs in a specific algorithm called a PID controller to determine how much to move the drone along all three axes.  
6. Translate how much the drone needs to move into how much power to give each motor, a process called motor mixing.  
This loop happens roughly every 250 microseconds, allowing the drone to react to the user's commands in real time while staying balanced in the air.  

<!-- If you're interested, you can learn more about the specific algorithms [here](link to advanced software).   -->