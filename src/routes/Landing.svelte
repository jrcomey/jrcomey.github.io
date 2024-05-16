<script>
    import Typewriter from 'svelte-typewriter';
    import {concurrent, cascade, scramble} from 'svelte-typewriter';
    let background_animation = "src/assets/demo_2.gif"

    let gear_pic = "src/assets/gear2.svg";
    let gear_alt = "Gear pic";
    let rocket_pic = "src/assets/rocket.svg";
    let rocket_alt = "Rocket Pic";

    

    let gifIndex = 1;
    let totalGifs = 3; // Total number of GIFs
</script>

<section class="landing-page" id="landing">

    <img class="landing-background-animation" src={background_animation}/>
    
    <div class="landing-background-gradient-overlay"></div>
    <div class="landing-background-gradient-overlay-bottom"></div>
    <div>
            <h1>Better Landing Tag</h1>
            <h4>Jack Rhys Comey</h4>
            <h4>Guidance, Navigation, and Controls Engineer</h4>
            <h4>Currently at: Lockheed Martin Space</h4>
        
    </div>

    
    <div >
        <p>2021 NASA ARMD University Design Challenge Winner</p>
        <p>B.S. UC Davis: Aerospace Science and Engineering</p>
        <p>B.S. UC Davis: Mechanical Engineering</p>
        <p>2 years of Industry Experience</p>
        <p>Committed to Space Technology Development</p>
    </div>
    <div class="landing-page-icon-grid">
        <img width=40% src={gear_pic} alt={gear_alt}/>
        <img width=40% src={rocket_pic} alt={rocket_alt}/>
        <div class="empty"></div>
        <p>Stat 1</p>
        <p>Stat 2</p>
        <div class="empty"></div>
        
    </div>

    <div class="empty"></div>


</section>

<style>

    .landing-background-animation {
        position: absolute;
        top: 0;
        left: 30%;
        width: 100%;
        height: 100%;
        z-index: -2;
        
    }
    
    .landing-background-gradient-overlay {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: linear-gradient(110deg, rgba(15, 17, 18, 1) 40%, rgba(15, 17, 18, 0.0) 80%, rgba(15, 17, 18, 0.0));
        z-index: -1;
    }

    .landing-background-gradient-overlay-bottom {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: linear-gradient(-5deg, rgba(15, 17, 18, 1), rgba(15, 17, 18, 0.2), 20%, rgba(15, 17, 18, 0) 25%, rgba(15, 17, 18, 0));
        z-index: -1;
    }

    .landing-page {
        display: flex;
        align-items: flex-start;
        min-height: 90vh;
        text-align: left;
        justify-content: space-between;
        /* background: linear-gradient(to left, rgba(32,39,49,0) 80%,
              rgba(32,39,49,1)), url(http://foo.com/image.jpg); */
        color: #ffffff;      
        overflow: hidden;        
        /* font-variant: small-caps; */
    }
    

    .landing-page-icon-grid {
        display: grid;
        grid-template-columns: 1fr 1fr 5fr;
        /* grid-template-rows: fr 1fr; */
        width: 100%;
        text-align: center;
        align-content: left;
        place-items: center;
    }

    .landing-page h1 {
        line-height: 1.5;
        font-family: 'Helvetica', italics;
        font-weight: 700;
        font-variant: small-caps;
        color: #FFFFFF;
    }

    .landing-page h4 {
        line-height: 0%;
        /* font-family: 'Helvetica', monospace; */
        color: #FFFFFF;
    }

    .landing-page p {
        /* font-family: 'Helvetica', monospace; */
        color: #FFFFFF;
    }
   
</style>