<script>
    /** @type {import('./$types').PageData} */
    export let data;
</script>

<p>I developed a multicopter dynamics package to aid in the development of Unmanned Aerial Vehicles (UAV/UAS). It allows for rapid prototyping of UAVs of any size, shape, or configuration, through easily configured settings, and returns predictions of vehicle dynamics under a variety of conditions.</p>

<p>I began developing this Python package after I encountered difficulties gaining access to aircraft testing facilities on campus while captain of my aircraft design team. While initially intended to serve as a replacement for flight testing, the scope of the project increased to serve as a rapid prototyping environment for Unmanned Aerial Vehicles (UAVs).</p>

<p>While the original objectives of the package were completed, it is continually being developed as part of the Urban Air Mobility Project, which you can read more about here.</p>

<p>The package itself is easy to use, and well-optimized. Any arbitrary multicopter UAV, of any number of motors, configuration, layout, or orientation, can be simulated. The user need only define directional effects of each motor on the local body of the aircraft. </p>

<p>The simulation uses a custom 6 degree of freedom (DOF) state space physics and control model. At each time step, the current attitude and position are fed into the simulated flight controller, along with a waypoint position. The difference between the two states is rotated into local body coordinates, and the flight computer determines raw signal output to the motor signals. </p>

<p>Each motor can be customized, with unique time response parameters and thrust curves. Using this data, local body forces on the aircraft are calculated, and the new state vector is used to update the position and attitude of the aircraft in the physics model.</p>

<p>The end result is a highly optimized flight simulator, which enables the user to rapidly test UAV multicopter aircraft, or optimize onboard controls, reducing cost and improving designs. If you are interested in seeing the model explained in detail, the report is on the left of the page.</p>

<p>While all base features of the simulation package are complete, development on the simulator will continue in the coming months. My senior design project (which will have its own page after sufficient progress) is a multicopter Urban Air Mobility (UAM) aircraft, and this simulator provides a perfect testing environment.</p>

<p>Expected updates to the package will include a shift to the more-accurate RK4 algorithm, wind and drag simulation, and a fuel consumption tracker.</p>

<p>The package can be found on my Github page.</p>