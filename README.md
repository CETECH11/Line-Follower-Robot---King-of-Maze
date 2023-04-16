# Line-Follower-Robot---King-of-Maze

LFR stands for Line Following Robot. The line it follows could be white, black, any other color, or even transparent. All that matters is, the robot must follow the line.

Even though it sounds simple, it is a struggle for most of the 1st Year Engineering students. It is a struggle to understand, then implement, then analyze the errors, and make corrections accordingly. After a couple of days, most likely a week, an LFR is finally ready to be run on a line.

Line Following Robots are pretty basic and have readily-available instructions on building them on the Internet. Keeping the usual LFR aside, the one we shall be building is different. Why is that?
1. It has a purpose.
2. It is pretty smart.

![alt text](https://hackster.imgix.net/uploads/attachments/1562635/image_qAg6ebbhe1.png?auto=compress%2Cformat&w=740&h=555&fit=max)

In other words, this LFR is an "IoT-based SmartPID tunedMaze Solver". It can be put anywhere in the maze, and let the robot do a dry run. While performing the dry run, it maps the whole maze and waits for the user to provide a destination. During the speed run, on providing a destination, the LFR reaches the spot through the shortest path available.

To make sure the shortest distance also moves faster in long straight paths, we require a moto speed control system. Along with that, we need a PID control system to find the fastest safe seed way to cover the distance in a short time.
A control system is a system, which provides the desired response by controlling the output. There are two major types - Open & Closed Loop system
Open loop systems are regular predefined inputs that provide output depending on the Input provided.
But the Closed loop system is a feedback-driven system, where the new output depends on the previous output, and whether it matches the defined set point after removing the error in a new value.

![alt text](https://hackster.imgix.net/uploads/attachments/1562682/image_eD9PSoUxgq.png?auto=compress%2Cformat&w=740&h=555&fit=max)

PID controller maintains the output such that there is zero error between the process variable and setpoint/ desired output by closed-loop operations. We use error removal on 3 different levels -

1. Proportional - It gives an output that is proportional to current error e (t). It compares the desired or set point with the actual value or feedback process value. The resulting error is multiplied with a proportional constant to get the output. If the error value is zero, then this controller output is zero.

2. Integral - Due to the limitation of the p-controller where there always exists an offset between the process variable and setpoint, the I-controller is needed, which provides the necessary action to eliminate the steady-state error. It integrates the error over a period of time until the error value reaches zero.Integral control decreases its output when a negative error takes place. It limits the speed of response and affects the stability of the system. The speed of the response is increased by decreasing integral gain.

3. Derivative - The I-controller doesn’t have the capability to predict the future behavior of error. So it reacts normally once the setpoint is changed. D-controller overcomes this problem by anticipating the future behavior of the error. Its output depends on the rate of change of error with respect to time, multiplied by the derivative constant. It gives the kick start for the output thereby increasing system response. It improves the stability of the system by compensating for phase lag caused by the I-controller. Increasing the derivative gain increases the speed of response.

![alt text](https://hackster.imgix.net/uploads/attachments/1544797/pcbway_55Vl7NMRFG.JPG?auto=compress%2Cformat&w=740&h=555&fit=max)

You must check out [PCBWAY](https://www.pcbway.com/) for ordering PCBs online for cheap!

You get 10 good-quality PCBs manufactured and shipped to your doorstep for cheap. You will also get a discount on shipping on your first order. Upload your Gerber files onto PCBWAY to get them manufactured with good quality and quick turnaround time. [PCBWay](https://www.pcbway.com/) now could provide a complete product solution, from design to enclosure production. Check out their online Gerber viewer function. With reward points, you can get free stuff from their gift shop.
