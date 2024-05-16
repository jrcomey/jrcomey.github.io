<script>

    let profile_pic = "src/assets/profile.JPG";
    let fern_pic = "src/assets/photography/fern_closeup.jpg";

</script>


<section>
    <div class="shaded-background">
        <div class="description">
            <h1>Academics</h1>
            <p>I graduated from University of California, Davis, in 2021, with a dual Bachelor's degree in Aerospace Science and Engineering, and Mechanical Engineering. I thoroughly enjoyed my time there, and I made many friends there that I will keep for life.</p>
            <p>My first taste of the full aircraft design cycle was as part of UC Davis's Aerobrick team, a heavy lift aircraft design team that competed each year in SAE's Aero Design West. In my first year, I had joined the team too late in the cycle to participate in the design, but the next year I was selected to lead the team (as part of a group of three), and proposed a elliptical wing aircraft, but the competition that year was cancelled due to the COVID-19 pandemic.</p>
            <p>The pandemic also ruined my chances for an internship that summer, as most companies withdrew postings and most positions became remote. I decided to make my own luck and gave myself an assignment, making a <a href="projects/UAVSim">6DOF multirotor simulator</a> to teach myself more about engineering software design. I was able to have the project reviewed after completion by TAs and professors, and put the resulting software into practice the next year.</p>
            <p>The challenge for our undergraduate capstone design team was to create an urban air mobility aircraft (UAM) for transport in and around one of several major metropolitan areas in the continental United States. The challenge itself was written by the NASA Aeronautics Research Mission Directorate, based out of the NASA facility in Langley, Virginia, and our team was allowed the option of submitting our design to the competition after completion. We decided on Chicago as our target location, as we thought a midwestern winter made for a more challenging environment (and therefore a more interesting project). Our end result was <a>the ATP-XW Blizzard, a two-ton, hydrogen-powered multirotor helicopter</a> with a high passenger throughput and significant temperature tolerance.</p>
        </div>
        <div class="image-reel">
            <img src={fern_pic} alt="Profile Picture"/>
            <h3><i>Hawaiian Fern</i></h3> 
            <p>May 2<sup>nd</sup>, 2023</p>
        </div>
    </div>
</section>
<style>

    section {
        background-image: url("./src/assets/photography/cooks_bay.jpg");
        align-content: center;
        background-size: cover;
        position: relative;
    }
    
    .shaded-background {
        background-color: #0f1112CC;
        /* display: flex; */
        /* flex-direction: row; */
        padding: 5%;
        border-radius: 2%;
        display: grid;
        /* grid-row: 1; */
        grid-template-columns: 4fr 3fr;
        /* padding: 5%; */
        align-content: left;
      }
    
    .image-reel {
        /* border: 5%; */
        margin: 5%;
        align-content: center;
    }
    
    .description {
        margin: 5%;
    }
    
    .image-reel img {
            width: 100%;
            object-fit: cover;
            aspect-ratio: 1;
            border-radius: 5%;
            /* padding: 5%; */
        }
    
    </style>