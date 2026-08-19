# Hardware
- Drones need to do two main things.
- First, they need to apply a force against gravity to stay in the air.
- And second, they need to be able to move around.

- In order to counteract gravity, all you really need is one propeller.
- But the problem with that is that as the motor spins, it pushes against the body of the drone, causing the body to spin in the opposite direction.
- In order to counteract this spin, helicopters have a tail with another prop sideways to apply a counter force.
- They also use this to spin around its vertical axis.

[Why tail rotors video](https://youtu.be/XQiz6a8x9rE?si=XJz3Bgg-VM3PTzvx)

- Helicopters move around using a relatively complex mechanical mechanism called a swashplate.
- The swashplate changes the pitch of the rotor blades depending on where they're in their rotation.
- This allows the helicopter to produce more lift on one side of the rotor disk, allowing it to tilt and move forward, backwards, or side to side.

[Swashplate video](https://youtu.be/MLY-Y-CbbU8?si=1GFkkNKcItUlNdFt)

- But if this same mechanism were scaled down to a drone, it would be very fragile and prone to breaking.
- Instead, drones usually use 4 independent motors, changing the speed of individual motors to change direction.
- This removes the mechanical complexity of the swashplate in exchange for more software complexity.

- Since drones don't have a sideways prop to rotate around their vertical axis, they do something else.
- When diagonal motors are powered, the motors push on the body of the drone in the same direction, allowing the drone to spin in place.

[Video explaining how a drone moves](https://youtu.be/iQAPkN7OWus?si=7apKPRasRD44KZAU)

- The reason drones have four motors is because it's the minimum number of motors needed to efficiently stay in the air and move around without needing complicated mechanical parts.
- The reason helicopters don't do the same is because four large motors and their power electronics would add significant weight, while a single engine and mechanical transmission are more efficient when scaled up.