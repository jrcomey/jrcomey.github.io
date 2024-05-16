<script>
    /** @type {import('./$types').PageData} */
    export let data;
    import Header from '../../Header.svelte';
</script>

<Header/>

<section class="title-page">

    <div class="gradient-background"></div>
    <h1>THE ATP-XW BLIZZARD</h1>


</section>

<section class="high-level-description">

    <h1>ALL WEATHER TAXI PILOTS EXPERIMENTAL WEATHER AIRCRAFT <i>BLIZZARD</i></h1>

    <p>I designed a fully functional Guidance, Navigation, and Control (GNC) system for the Blizzard, and is capable of both piloted and autonomous control. The control system uses a state-feedback controller with added integrator control to maintain both the position and attitude of the aircraft by varying the rotation speed of the 8 motors which power the aircraft, creating thrust differentials, and therefore a moment about the center. The autonomous capabilities of the aircraft would reduce the operating costs by 35%, lowering ticket price and ultimately allowing the aircraft to carry more passengers. </p>


</section>





<p>The system is currently being redeveloped to be used in gust detection and avoidance. The process is currently in an early stage of development, but will use ultrasonic sensors to detect local weather cells in the areas around the aircraft, predict incoming wind patterns, and preemptively begin maneuvers to reduce the impact of wind gusts on the aircraft.</p>

<p>Using my simulation program, I was able to test the aircraft against a variety of maneuverability tests, as laid out in ADS-33E-PRF, a military standard which contains, among other elements, a list of response tests for rotary-wing aircraft in windy conditions. While not required to certify the Blizzard for its intended use, these standards provide a clear pass/fail test used for other fast-response aircraft in similar conditions. My plan is to repeat these tests once the aerodynamic model is fully completed, for wind conditions, temperatures, and precipitation consistent with Chicago winter weather.</p>

<p>To determine the size of the support struts which held the coaxial motor set in place in the duct, I constructed a carpet plot, a method commonly used in the aerospace field to size sets of independent and dependent variables. The plot varies both the number of struts, and their size, and determined operating point based on beam deflection under maximum loading conditions, and thrust force lost to drag on the motors. Using this plot I was able to appropriately size the motor support struts around an operating point.</p>

<p>I developed a Concept of operations (CONOPs) for the aircraft, defining its mission and flight profile, in accordance with requirements set by the NASA Aeronautics Undergraduate Competition statement, FAR  standards, and our team's own requirements set. This guided my team's development of the Blizzard with regards to sizing and power requirements.</p>

<p>Using my UAVSim flight simulator (which you can read more about here) I developed a flight model for the Blizzard and ran a Monte Carlo simulation by randomizing aircraft position and attitude and allowing the aircraft to return to a neutral position, observing system response. </p>

<p>Results indicated that the aircraft was stable for perturbations under a given magnitude, and in most cases recovered with only a 6 meter loss of altitude. Results initially identified a control error that caused the aircraft destabilized if inverted, and has been fixed. The aircraft is now able to safely recover from any attitude destabilization.</p>

<p>In the current quarter, our team has chosen to focus on a gust detection and avoidance system to navigate local weather patterns between large buildings. I am currently in the process of writing a Model Predictive Control (MPC) GNC control sequence to resist significant gusts. The model will take both the current attitude of the aircraft, and incoming wind gusts to preemptively position the aircraft in order to provide a counter force to the drag resulting from the gust. </p>

<p>I selected a motor for the aircraft based on power and weight requirements to meet requirements set out by the competition statement and further requirements by our team. I then developed a propeller under the motors' given operating characteristics using Blade Element Momentum (BEM) theory using a self-developed Python program. I analyzed the propeller and the aircraft as a whole and determined Hover Efficiency/Figure of Merit for the aircraft.</p>

<p> Among many other things, I designed the propellers and selected motors for the aircraft, but my biggest contribution to the project was a full autopilot system for the aircraft. This system included guidance, navigation, and control components, and aircraft dynamic behavior was verified through the multirotor simulator I had designed the previous summer. To verify our flight controller, I ran Monte Carlo simulations to verify aircraft stability under randomized conditions.</p>
<style>

    section {
        background-size: cover;
        position: relative;
        z-index: -10;
        min-height: 90vh;
        /* align-content: center; */
        display: flex;
        flex-direction: column;
    }
    .title-page {
        align-content: left;
        background-image: url("/src/assets/blizz.png");
        background-size: cover;
        justify-content: end;
        margin-bottom: 0%;
        margin: 0%;
        overflow: hidden;
        /* padding: 0%; */
        /* border: 0%; */
    }
    .gradient-background {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: linear-gradient(to top, rgba(15, 17, 18, 0.9), rgba(15, 17, 18, 0.9), 30%, rgba(15, 17, 18, 0));
        z-index: -1;
    }
    .high-level-description {

    }
</style>