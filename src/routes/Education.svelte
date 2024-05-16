<script>
    let gear_pic = "src/assets/gear2.svg";
    let gear_alt = "Gear pic";
    let rocket_pic = "src/assets/rocket.svg";
    let rocket_alt = "Rocket Pic";
</script>


<div class="spacer  centered"></div>
  <section class="education">
    <h1>Education</h1>
    <div class="education-box">
      <img width=40% src={gear_pic} alt={gear_alt}/>
      <img width=40% src={rocket_pic} alt={rocket_alt}/>
        <p>B.S. Aerospace Science and Engineering</p>
        <p>B.S. Mechanical Engineering</p>
        <p>University of California, Davis</p>
        <p>University of California, Davis</p>
    </div>
  </section>


<style>
  .spacer {
    aspect-ratio: 960/300;
    width: 100%;
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
}

.layer1 {
  background-image: url('./assets/layer1.svg');
}

.centered {
  align-items: center;
}

.education-box{
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 3fr 1fr 1fr;
  place-items: center;
}

</style>