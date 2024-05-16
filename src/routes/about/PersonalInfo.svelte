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
            <h1>A Little More Background</h1>
            <p>I grew up in California's southern Bay Area.</p>
            <p>I've always had a passion for spaceflight. Like many engineers, I grew up watching the Space Shuttle launches, and always wanted to work on spacecraft like that. It had always seemed like a pipe dream, but the longer I worked, the more practical of an option it became. I've now graduated with two B.S.'s in engineering, and started my career over two years ago with Lockheed Martin Space.</p>
            <p>In my free time, I like to hike in many of the fantastic national and state parks the California has to offer, often as part of a nature photography trip. You may see some of my work scattered around the background of this website, and if you see something that you'd like to visit yourself, please don't hesitate to reach out.</p>
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