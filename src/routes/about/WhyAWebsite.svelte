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
            <h1>Why A Website?</h1>

            <p><i>If an image is worth a thousand words, an interactive website with images and animations is worth millions.</i></p>
            <hr>
            <p>The longer answer is that there are two primary lines of thinking that lead to the same conclusion:</p>
            <ul>
                <li>People who are not themselves engineers, but work with them on a regular basis often complain about a lack of communications skills in the discipline. This is not always true, but true often enough to be warranted. Any engineer who is able to not only <i>design</i> well, but can also <i>present</i> well (whether to an internal audience, customers, or investors) sets themselves far apart from other candidates. Think of it as a force multiplier for good design.</li>
                <li>The internet is inseperable from modern life and modern communication. The modern western economy has largely left behind printed documents for webpages not merely because it is more cost-effective, but because they are <b>significantly better for communicating ideas with greater capabilities than a paper document could allow.</b> A simple visual demonstration, through animation or images, will inform and engage the reader far better than simple text can permit.</li>
            </ul>
            <p><i>Of course, should you prefer a well-formatted resume, <a>you can find mine here.</a></i></p>
            <hr>
            <p>If you are intrigued by what you've seen here, <a href="/contact">please don't hesitate to reach out.</a></p>
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