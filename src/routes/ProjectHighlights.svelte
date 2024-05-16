<script>

</script>

<section class="dark centered">
    <h1>Project Highlights</h1>
    
    <div class="big-project-title-page">

        <div class="project-image-backdrop-white">
            <img src="src/assets/BlockDiagTransparent4.png" class="big-project-image-title-page" alt="MULTIROTOR GUST REDUCTION SYSTEM">
        </div>
        <div class="big-project-description">
            <h1>Multirotor Gust Reduction System</h1>
            <h3>Weather Tolerant Controls Scheme for High Wind Environments</h3>
            <p>
                As part of my undergraduate design project, I worked with my team to develop a system for the Blizzard eVTOL UAM aircraft to withstand both significant gusts and other wind fields common to the Chicago area. I developed a fully fledged Guidance, Navigation, and Control system (GNC), using multiple controllers, to operate the aircraft during flight. I developed optimal controllers using a Linear Quadratic Regulator (LQR) from a linearized model, and demonstrated the controller using my UAV simulation. I performed dozens of simulation tests to verify flight performance under windy conditions.
            </p>
            <p>
                To read more about it, <a href="/projects/grs">click here</a>.
            </p>
        </div>
    </div>

    <div class="big-project-title-page">
        <div class="project-image-backdrop-white">
            <img src="src/assets/blizz.png" class="big-project-image-title-page" alt="ATP-XW BLIZZARD: WEATHER TOLERANT URBAN AIR MOBILITY CONCEPT">
        </div>
        
        <div class="big-project-description">
            <h1>ATP-XW Blizzard</h1>
            <h3>Weather Tolerant Urban Air Mobility Concept</h3>
            <p>
                As part of a team of 5, my team and I are developing a weather tolerant, hydrogen powered Urban Air Mobility (UAM) vehicle, designed for operation in Chicago's cold-weather environment. I developed a fully functional Guidance, Navigation, and Control (GNC) system to enable autonomous flight for the aircraft. I also developed significant parts of the propulsion train for the aircraft, developing propellers using Blade Element Momentum (BEM) theory. I also created a flight model for the aircraft and proved the viability of the control method using a Monte Carlo simulation. I additionally designed the propeller for the aircraft, and performed center of mass calculations.
            </p>
            <p>
                To read more about it, <a href="/projects/blizzard">click here</a>.
            </p>
        </div>
    </div>


</section>

<style>
    
    .big-project-title-page {
        display: grid;
        grid-template-columns: 1fr 2fr;
        background-color: #22272b;
        margin-top: 1%;
        margin-bottom: 1%;
        padding: 5% 5%;
        align-items: center;
    }

    .big-project-image-title-page {
        flex: 1;
        width: 100%;
        aspect-ratio: 16/9;
        object-fit: scale-down;
    }

    .big-project-description {
        display: flex;
        flex-direction: column;
        padding: 0% 10%; /* Adjust the padding as needed */
        align-content: flex-start;
    }

    .big-project-title-page h1 {
        font-variant: small-caps;
        font-size: 2.0em;
    }

    .big-project-title-page h3 {
        font-style: italic;
        font-variant: small-caps;
    }

    .project-image-backdrop-white {
        background-color: #FFFFFFCC;
        display: flex;
        padding: 0%;
        border-radius: 5%;
        height: 100%;
        width: 100%;
    }

    
</style>