# Hardware
- Drones need to do two main things.
- First, they need to apply a force against gravity to stay in the air.
- And second, they need to be able to move around.

- In order to counteract gravity, all you really need is one propeller.
- But the problem with that is that as the motor spins, it pushes against the body of the drone, causing the body to spin in the opposite direction.

[Image of one prop]()
	Maybe do video instead.

- In order to counteract this spin, helicopters have a tail with another prop sideways to apply a counter force.
- They also use this to spin around its vertical axis.

[Image of helicopter]()
	Video of this.

- Helicopters move around using a relatively complex mechanical mechanism called a swashplate.
- The swashplate changes the pitch of th rotor blades depending on where they're in their rotation.

- This allows the helicopter to produce more lift on one side of the rotor disk, allowing it to tilt and move forward, backwards, or side to side.

Show video of swashplate and helicopter moving.

- But if this same mechanism were scaled down to a drone, it would be very fragile and prone to breaking.
- Instead, drones usually use 4 independent motors, changing the speed of individual motors to change direction.

Show video of drone powering for pitch and roll control.

- This removes the mechanical complexity of the swashplate in exchange for more software complexity.
- Using four motors is only possible if you can quickly stop and start the motors.
* Using four motors works because electric motors can rapidly change their speed.

- This is easier when the props are smaller and using electric power, instead of larger and decile power.
* This is easier with smaller propellers and electric motors than with larger propellers and combustion engines.

- This is why helicopters don't also use four motors.

* This is one reason helicopters don't typically use four independent rotors.

- That and the inefficiencies four seprate drive trains cause, is the reaosn helicopers don't typically use 4 independent rotos.

* The inefficiencies of using four separate drivetrains are another reason helicopters don't typically use four independent rotors.

- Drones don't have a sideways propeller to rotate around their vertical axis, so they do something else.
- When diagonal motors are powered, the motors push on the body of the drone in the same direction, allowing the drone to spin in place.

Show video of yaw control.

- The reason drones have four motors is because it's the minimum number of motors needed to efficiently stay in the air and move around, without needing any complicated mechanical parts.