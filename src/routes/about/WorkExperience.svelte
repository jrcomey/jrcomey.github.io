<script>

    let profile_pic = "src/assets/profile.JPG";
    let moon_pic = "src/assets/moon_pic.jpg";

</script>

<section>
    <div class="shaded-background">
        <div class="image-reel">
            <img src={moon_pic} alt="Profile Picture"/>
            <h3><i>The Moon and Mars</i></h3> 
            <p>January 30<sup>th</sup>, 2023</p>
        </div>
        <div class="description">
            <h1>Work Experience</h1>
            <p><i>Please note that I am explicitly vague to respect my employer's proprietary information. This website is intended to showcase work that is either wholly or partly (in the case of university projects) my own.</i></p>
            <p>I joined Lockheed Martin Space in 2021, shortly after graduating college, and have been working at the Sunnyvale facility since then. I'm currently with Lockheed's <b>C</b>ommon <b>C</b>ontrols and <b>A</b>vionics group (CCA), an in-house general-purpose electronics and control team. </p>
            <p></p>
        </div>
        
    </div>
</section>

<style>

    section {
        background-image: url("./src/assets/moon_pic.jpg");
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
        grid-template-columns: 3fr 4fr;
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