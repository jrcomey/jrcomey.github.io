<script>
    let black = "#0f1112";
    let bluegrey = "#181c1f";
    let darkgrey = "#22272b";
    let white = "#FFFFFF";


</script>

<section id="misc-projects" class = "dark centered">
    <h1>Project Gallery</h1>
    
    
    <div class="project-grid">

        <div class="project">
            <a href="/projects/DATACOM"><img src="./src/assets/moon_pic.jpg" alt="UAVSim Plot"></a>
            <a href="/projects/DATACOM"><h2>DATACOM</h2></a>
            <a href="/projects/DATACOM"><h3>Multipurpose Simulation Visualization Engine</h3></a>
            <a href="/projects/DATACOM"><p>A custom graphics engine using OpenGL for easier visualization of 6DOF simulations</p></a>
        </div>

        <div class="project">
            <a href="/projects/KalmanFilter"><img src="./src/assets/moon_pic.jpg" alt="Kalman Filter"></a>
            <a href="/projects/KalmanFilter"><h2>Kalman Filter Demonstration</h2></a>
            <a href="/projects/KalmanFilter"><h3>Statistical Methods for Navigation</h3></a>
            <a href="/projects/KalmanFilter"><p>A C++ demonstration of a common navigation technique</p></a>
        </div>

        <div class="project">
            <a href="/projects/ThreeBodyProblem"><img src="./src/assets/moon_pic.jpg" alt="Three Body Problem"></a>
            <a href="/projects/ThreeBodyProblem"><h2>The Three Body Problem</h2></a>
            <a href="/projects/ThreeBodyProblem"><h3>A classic dynamics problem</h3></a>
            <a href="/projects/ThreeBodyProblem"><p>A C++ demonstration using a well-known dynamics model.</p></a>
        </div>

        <div class="project">
            <a href="/projects/UAVsim"><img src="./src/assets/newplot.png" alt="UAVSim Plot"></a>
            <a href="/projects/UAVsim"><h2>UAVSim</h2></a>
            <a href="/projects/UAVsim"><h3>Rotorcraft Dynamics Simulation Package</h3></a>
            <a href="/projects/UAVsim"><p>A package intended to reduce testing costs in vehicle development, and to provide a testing environment if one is unavailable.</p></a>
        </div>

        <div class="project">
            <a href="/projects/clementine"><img src="./src/assets/poster_req_review.png" alt="Clementine"></a>
            <a href="/projects/clementine"><h2>Clementine</h2></a>
            <a href="/projects/clementine"><h3>Space Systems Engineering</h3></a>
            <a href="/projects/clementine"><p>As part of a team of 5, I was tasked with reverse-engineering the 1993 Clementine lunar flyby probe in order to modify the spacecraft to prevent an ADCS error that caused mission failure.</p></a>    
        </div>


        <div class="project">
            <a href="/projects/aerobrick"><img src="./src/assets/mozziepic.png" alt="Aerobrick"></a>
            <a href="/projects/aerobrick"><h2>Aerobrick</h2></a>
            <a href="/projects/aerobrick"><h3>Fixed-wing Aircraft Design</h3></a>
            <a href="/projects/aerobrick"><p>I was Team Captain of a heavy-lift aircraft design team that competed in SAE Aero Design West's Regular division. </p></a>
        </div>


        <div class="project">
            <a href="/projects/launchsim"><img src="./src/assets/Undeformed.png" alt="Deformed Satellite"></a>
            <a href="/projects/launchsim"><h2>Launch Simulation</h2></a>
            <a href="/projects/launchsim"><h3>Satellite Inertial Loading and Thermal Analysis</h3></a>
            <a href="/projects/launchsim"><p>Analysis of satellite superstructure experiencing inertial loading during launch, and thermal loading during operation</p></a>
        </div>


        <div class="project">
            <a href="/projects/flat-plate-drag"><img src="./src/assets/Prob1bResults1.png" alt="Reynolds Flow Pic"></a>
            <a href="/projects/flat-plate-drag"><h2>Flat Plate Drag</h2></a>
            <a href="/projects/flat-plate-drag"><h3>CFD & Fluid Flow Analysis</h3></a>
            <a href="/projects/flat-plate-drag"><p>Two-dimensional analysis of subsonic fluid flow over a flat plate using numerical methods</p></a>
        </div>


        <div class="project">
            <a href="/projects/waveprop"><img src="./src/assets/Prob1b.png" alt=""></a>
            <a href="/projects/waveprop"><h2>Wave Propagation Analysis</h2></a>
            <a href="/projects/waveprop"><h3>2D Discrete Differential Equation Solutions</h3></a>
            <a href="/projects/waveprop"><p>A three-dimensional study of wave propagation and subsonic/supersonic airflow</p></a>
        </div>


        <div class="project">
            <a href="/projects/basins"><img src="./src/assets/basinsofattraction.png" alt="Project 4"></a>
            <a href="/projects/basins"><h2>Basins of Attraction</h2></a>
            <div></div>
            <a href="/projects/basins"><h3>Iterative Convergence Study</h3></a>
            <a href="/projects/basins"><p>Fractal convergence study for system using imaginary numbers</p></a>
        </div>

        <div class="project">
            <a href="/projects/supersonic"><img src="./src/assets/Prob2bResults.png" alt="Project 3"></a>
            <a href="/projects/supersonic"><h3>Supersonic Flow</h3></a>
            <a href="/projects/supersonic"><p>Two-dimensional analysis of supersonic flow over a symmetric biconvex airfoil</p></a>
        </div>

    </div>

    <!-- <div id="image-track" data-mouse-down-at="0">
        <img class="image" src="./src/assets/windy_hill_forest_1.jpg" alt="Project 3">
        <img class="image" src="./src/assets/windy_hill_forest_1.jpg" alt="Project 3">
        <img class="image" src="./src/assets/windy_hill_forest_1.jpg" alt="Project 3">
        <img class="image" src="./src/assets/windy_hill_forest_1.jpg" alt="Project 3">
        <img class="image" src="./src/assets/windy_hill_forest_1.jpg" alt="Project 3">
        <img class="image" src="./src/assets/windy_hill_forest_1.jpg" alt="Project 3">
        <img class="image" src="./src/assets/windy_hill_forest_1.jpg" alt="Project 3">
    </div> -->


        
</section>

<style>
    
.project-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr); /* Adjust the number of columns as needed */
  grid-gap: 20px;
}

.project:hover {
    scale: 1.02;
}

.project:hover img {
    opacity: 100%;
}

.project {
    display: flex;
    justify-content: flex-start;
    flex-direction: column;
    text-align: center;
    margin-bottom: 30px;
    background-color: #22272b;
    border-radius: 1%;
}

.project img {
  aspect-ratio: 1 / 1;
  border-radius: 5px;
  width: 100%;
  opacity: 80%;
  object-fit: cover;
  /* height: 50%; */
}

.project a {
    color: #FFFFFF;
    text-decoration: none;
}

.project a:hover {
    /* text-decoration: underline; */
}

.project p {
  padding: 5%;
}

.project h3 {
    /* font-family: 'Helvetica', sans-serif; */
    font-style: italic;
}

section {
    background-color: #0f1112;
}

</style>