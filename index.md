---
layout: default
---

This is a developer blog detailing engineering projects by Jack Comey.

All work is my own, unless stated otherwise.

For highlights of my work, please [click here](./another-page.html).

# Latest Project Updates

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Update 1: Physics simulation

I'm very pleased to report that the basic physics model for the simulation is now complete. 


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
