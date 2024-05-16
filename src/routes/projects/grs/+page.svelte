<script>
    /** @type {import('./$types').PageData} */
    export let data;
</script>

<p>As part of my undergraduate design project (see below), I worked with my team to develop a system for the Blizzard eVTOL UAM aircraft to withstand both significant gusts and other wind fields common to the Chicago area. I developed a fully fledged Guidance, Navigation, and Control system (GNC), using multiple controllers, to operate the aircraft during flight. I developed optimal controllers using a Linear Quadratic Regulator (LQR) from a linearized model, and demonstrated the controller using my UAV simulation. I have currently performed dozens of tests to verify flight performance under windy conditions.</p>

<p>The GNC system uses two controllers for flight operations, one primary feedback, and an an auxiliary feed-forward controller for use in gust avoidance.</p>

<p>The primary controller is an LQR controller, developed using a linearized state space model of the Blizzard vehicle. The controller was developed using MATLAB, and then implemented in the UAVSim simulation program, which you can bread more about here.</p>

<p>The main vulnerability of the Blizzard aircraft is the relatively slow motor response time. This could be avoided be implementing a variable pitch mechanism, but that would leave the aircraft vulnerable to icing conditions due to increased mechanical complexity. Our team has decided to bypass this by implementing a secondary controller, which preemptively begins aircraft maneuvers at the instant the aircraft is affected by a gust, instead of waiting for the aircraft to tilt before correction. The feedback controller is still under development. </p>

<p>The flight controller was verified using my UAVSim simulation program. Dozens of tests were performed under several different wind conditions, and dozens more are planned. On the left is an image of an aircraft yaw test, under chaotic wind conditions. As you can see, the aircraft is able to maintain attitude (and position, not shown), and can even execute maneuvers under windy conditions. </p>

<p>Performance tests and standards were taken from ADS-33E-PRF, a set of standards for military rotary-wing aircraft, which include a number of tests for maneuvers under windy conditions with clear pass/fail criteria. On the left is a demonstration of a roll impulse response test, one of the tests listed in the standard. The acceptable recovery zone is marked within the black dashed lines. This test shows an older controller under calm winds, and will be repeated under strong winds with the improved controller upon completion of the design.</p>

<style>
    
</style>