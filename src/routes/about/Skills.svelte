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
            <h1>What I Can Offer You</h1>
            <p>I am first and foremost a controls engineer. While my experience is mostly in 6DOF control for both <a href="">aircraft</a> and <a href="">spacecraft</a>, and in <a href="">precision motor control</a>, these skills are applicable to a wide variety of industries.</p>
            <p>Need sensor fusion techniques to position your smartphone or headset design? Spatial positioning and controls for industrial robotics? Each one uses similar techniques, using skills that I've demonstrated here on my site. They include <a href="">Kalman filters for sensor fusion and navigation</a>, <a href="">Laplacian time-domain modeling for accurate dynamics</a>, <a href="">classical controls in the discrete and continuous domains</a>, and <a href="">more complex system controls such as Linear Quadratic Regulators</a>.</p>
            <p>I'm proficient in a wide variety of programming languages, and can also pick up new ones quickly as needed. I've primarily used MATLAB and Simulink in industry, but you'll see my personal projects include languages such as C, C++, Python, Rust, and more.</p>
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

        b {
        color: #00C1D4;
        font-variant: bold;
    }
</style>