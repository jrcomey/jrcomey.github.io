---
layout: default
---

This is a developer blog detailing engineering projects by Jack Comey.

All work is my own, unless stated otherwise.

For highlights of my work, please [click here](./another-page.html).

Images to come soon!

# Latest Project Updates

These are my latest updates regarding my simulation project. 

## Update 3: PID Positional and Attitude control
_12 JUL 2020_

While velocity control is a good start, the type of system control that you'd want for an autonomous vehicle would be a positional control (e.g. give it an altitude, and it stays steady at that altitude). For that to happen, it was necessary to switch from a velocity based PID control to a position based PID. In practical effects, this just meant a change to the D term as a function of velocity rather than position, as well as the addition of a few feed forward terms. Below is an example of the new behaviour of the system:

**Image here**

Next comes attitude control. Using the same system, with slightly different constants, its possible to control pitch and roll simulataneously. PID loops for both are seperate, and signal changes to each motor are summed to the current motor signal matrix rather than setting the new signal themselves. This allows them to use the setpoint value for hovering and then modify attitude behaviour as slight differences to each motor from that baseline value. By doing so, both the altitude control and attitude correction funcitons can run simultaneously, with little effect on the other. The first attempt at this is seen below:

**Image here**

Note that the positional hover takes priority over attitude control, and that attitude control only has room to function after the UAV begins to stabilize at its setpoint altitude. Not only does this prevent attitude control until basic conditions have been met, but prevents the aircraft from self-righting if in an inverted position. The fix to this is to simply call the signal sanity check function at the end of the hover function, to ensure that the signal value that the attitude control functions are being summed with are not beyond the physical bounds of the signal wire itself. This allows the attitude control functions full input at all times, completely fixing the bug. The results of the new system are below.

**Image here**

## Update 2: PID Velocity control
_10 JUL 2020_

I wanted to begin PID testing with the translational system as a basic hover function, controlling vertical velocity as the output in the control loop, and motor signal input as the input. Unfortunately, I hadn't had time today to draw up a control systems model for desired behaviour, but the important part for today was to program the actual control loop itself, and worry about desired output behaviour once the system was in place. It's a standard PID loop, nothing particularly special, and I don't think the system itself warrants much explanation.

So far, so good. The simulation seems to be able to achieve a zero velocity condition using the PID loop. The primary issue was unit conversion between velocity and motor signal. My solution to this was to use two constants for each term, one for signal width (defined as the difference between the maximum motor input signal, and the accompanying minimum) and the other for the individual term constant. This is functional for velocity, but early attempts with a setpoint position rather than setpoint velocity yielded an unstable underdamped system. This will require more in-depth analysis, but not until similar control loops for attitude control have been developed.



## Update 1: Physics simulation
_9 JUL 2020_

I'm very pleased to report that the basic physics model for the simulation is now complete. As this is my first post regarding the development process,
this may be a little feature heavy. Bear with me, here.

I'm using a quadcopter model as my test aircraft, but the physics model and other math are applicable to all other formats.

When the aircraft is initialized, all components are defined in a local frame of reference, with its center at the UAV's centre of mass.
All force and torque generation and addition are then done in this localized frame of reference, and then the
combined net force and torque vectors are transformed into a global frame of reference. 
From there, external forces on the aircraft are summed (e.g. gravity)
and then kinematics calculations are performed for a small time interval **dt** for both translational and rotational movement. 

![UAV in freefall](Pictures/VerticalFall.png)

A quick test with no motor input shows that the aircraft falls towards the earth at an accelerating rate, and reaches a predicted position of Z=-44.15m
after three seconds. The next question is if thrust from the motors will stop the aircraft from falling. I wrote a placeholder control loop to increase thrust if the aircraft had negative velocity, and to decrease thrust if the velocity was positive, with the hope that it would reach a point where it would hover.

**Show hover pic here**

A successful, if not a very fast responding, demonstration of gravitational and motor forces shows that the translational force and kinematics models are functional.

The rotational model presented more difficulties. I ended up using a deconstructed version of Euler's equations, with an additional function to prevent Euler angles from exceeding bounds. The testing method was similar, and one motor was fixed at maximum power, and then the simulation was run.

![UAV in uncontrolled spin](Pictures/Uncontrolled spin.png)

Predictably, the aircraft flips over at an accelerating rate, and begins to spiral. After implementing basic feedback systems for both pitch and roll, these are the results:

![UAV with underdamped, unstable attitude control](Pictures/StabilizerPlaceholder.png)

The implemented control system is underdamped and unstable, but is, after all, a placeholder. The next step of the project is to replace this placeholder with a PID controller.

# Project Descriptions

## UAV Simulator Project Description

I've been working on this for a few weeks now, and I was encouraged to keep a development blog and document my process.
 The best place to start, I believe, would be a description of what it is exactly that I'm doing, and how I plan to go about it.

The project itself is a comprehensive UAV simulator (**U**nmanned **A**rial **V**ehicle) designed to be used as an easy testing platform for UAV systems.
While I'm currently developing for multicopter formats (quadcopters, hexacopters etc.), 
I plan on expanding the system for a much larger variety of aircraft in the future.

**Description of overall process here**

The program itself uses a parent class containing general purpose functions and calculations for any generic UAV system. If calculations are 
reliant on specific geometry of the UAV, then those functions are contained in that drone's object class (as a child class of the generic UAV)
This structure allows for easy modelling of wildly different UAV types, with minor edits to the initialization of a new child class, and edits to 
geometry-specific functions.
#### Planned Feature List

*	~~Body, Earth, and Stability transformation matrices for changing vector space~~
*	~~Translational motor thrust modelling~~
*	~~Torque modelling from motor thrust~~
*	Gyroscopic procession modelling for each motor
*	~~Sum of translational motor forces~~
*	~~Sum of motor torques~~
*	~~Model inertia matrix~~
*	~~Hover Capability~~
*	Stabilization loop for pitch
*	Stabilization loop for roll
*	Stabilization loop for yaw
*	Above three function together
*	X velocity kill control
*	X+Y velocity kill control
*	Full 3D velocity kill control
*	Stabilization into velocity kill function
*	Seperation of phyiscs calculations and velocity/stabilization program. (Control software loaded onto flight computer)
*	3D pathfinding algorithim to find shortst possible route in 3D space from point A to point B, with maximum acceleration limits.
