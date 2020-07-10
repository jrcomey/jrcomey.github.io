---
layout: default
---

This is a developer blog detailing engineering projects by Jack Comey.

All work is my own, unless stated otherwise.

For highlights of my work, please [click here](./another-page.html).

# Latest Project Updates

These are my latest updates regarding my simulation project. 
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

**Show freefall picture here**

A quick test with no motor input shows that the aircraft falls towards the earth at an accelerating rate, and reaches a predicted position of Z=-44.15m
after three seconds. The next question is if thrust from the motors will stop the aircraft from falling. I wrote a placeholder control loop to increase thrust if the aircraft had negative velocity, and to decrease thrust if the velocity was positive, with the hope that it would reach a point where it would hover.

**Show hover pic here**
A successful, if not a very fast responding, demonstration of gravitational and motor forces shows that the translational force and kinematics models are functional.

The rotational model presented more difficulties. I ended up using a deconstructed version of Euler's equations, with an additional function to prevent Euler angles from exceeding bounds. The testing method was similar, and one motor was fixed at maximum power, and then the simulation was run.

**Show spiral pic here**

Predictably, the aircraft flips over at an accelerating rate, and begins to spiral. After implementing basic feedback systems for both pitch and roll, these are the results:
**Show rotational feedback pictures here**

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
* 	X+Y velocity kill control
*	Full 3D velocity kill control
*	Stabilization into velocity kill function
* 	Seperation of phyiscs calculations and velocity/stabilization program. (Control software loaded onto flight computer)
*	3D pathfinding algorithim to find shortst possible route in 3D space from point A to point B, with maximum acceleration limits.




> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
