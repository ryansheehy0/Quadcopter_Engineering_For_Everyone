# Electronics
- The electronics for a drone are very similar to the electronics used in other robots.
- First is the battery.
- Depending on the size of the drone, these batteries typically range from 2S to 12S, which represents the number of cells connected in series and determines the voltage.
- Most drones use lithium polymer batteries, with a nominal voltage of around 3.7V per cell.
- Meaning a 4S battery has a nominal voltage of around 14.8V.

[4s Battery](./4s_battery.png)

- The battery is connected to all four motors through something called an electronic speed controller, or ESC for short.
- You can think of these as electronic switches that control how much power is delivered to each motor when given a command.

[ESC](./esc.png)

- In order for the brain of the drone, called the flight controller, to get power, the voltage needs to be stepped down to 5V.
- This can be done a number of ways, but the most common is with a buck converter.

[Buck converter](./buck_converter.png)

- The flight controller needs to know the current angle of the drone and the commands from the user.
- The drone's angle is determined using a sensor called an Inertial Measurement Unit, or IMU for short.
- The user's commands are gotten from the receiver, which receives radio signals from the user's controller.
- These two inputs are fed into the flight controller which calculates how much power each motors needs and sends those commands to the ESCs.

[IMU](./imu.png)
[Flight Controller](./flight_controller.png)
[Receiver and Controller](./receiver_and_controller.png)

- This is the full overview of the electronics.

[Electronics overview](./electrical_diagram.png)