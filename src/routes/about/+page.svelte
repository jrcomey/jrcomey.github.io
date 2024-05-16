


<!-- 


TO DO:
    - CENTER THE WHOLE PAGE 


-->

<script>
    import About from '../About.svelte';
    import Header from '../Header.svelte';
    import Academics from './Academics.svelte';
    import WorkExperience from './WorkExperience.svelte';
    import PersonalInfo from './PersonalInfo.svelte';
    import WhyAWebsite from './WhyAWebsite.svelte';
    import Skills from './Skills.svelte';

    /** @type {import('./$types').PageData} */
    export let data;
    let profile_pic = "src/assets/profile.JPG";
</script>

<Header/>

<About/>

<PersonalInfo/>

<Academics/>

<WorkExperience/>

<Skills/>

<WhyAWebsite/>



<style>

    .box-1 {
        display: grid;
        grid-template-columns: 1fr;
        grid-template-rows: 1fr 1fr;
    }

    .about-box {
        display: flex;
        justify-content: space-evenly;
        flex-direction: column;
        justify-content: space-evenly;
    }

    
    section {
        position: relative;
        display: flex;
        align-items: center;
    }
    
    .about-container {
        display: grid;
        grid-template-columns: 2fr 4fr;
        align-items: center;
    }
    
    .about {
        display: grid;
        flex-direction: row;
        grid-template-columns: 2fr 4fr;
        align-items: flex-start;
        padding: 5vh 5vw;
        justify-content: space-between;
        overflow: hidden;
    }

    section img {
        width: 10%;
        object-fit: scale-down;
        border-radius: 5%;
        /* padding: 5%; */
    }

    .about img {
        width: 100%;
        object-fit: scale-down;
        border-radius: 5%;
        /* padding: 5%; */
    }
    .about div {
        padding: 5vw;
        align-content: center;

    }
    .about h1 {
        text-decoration: underline;
    }


</style>


<!-- <section>
    <div class="about">
        <div class="about-box">
            <img src={profile_pic} alt="Profile Picture">
        </div>

        

        <div class="about-box">
            <h1>ABOUT ME</h1>
            <p> 
                My name is Jack Comey, and I'm a Guidance, Navigation, and Controls Engineer working in the space domain. I graduated from UC Davis in 2021, with a double Bachelor's degree in Aerospace Science and Engineering, and Mechanical Engineering. 
            </p>
            <p>
                I used the Covid-19 pandemic as an opportunity to improve my academic work and made the Dean's list three times during lockdown. I used the extra time available to take my work to the next level, and my team won the NASA ARMD Aeronautics competition as a part of the result of that.
                Since graduating, I've been at Lockheed Martin Space in Sunnyvale, working on precision motor controls for launch vehicle attitude control systems.
            </p>
            
            <p>
                In 2019, I lead an aircraft design team that competed in SAE Aero Design West, a heavy-lift aircraft design competition that competed last May against teams from a wide variety of nations. 
                Being a part of this team has provided invaluable hands-on design and leadership experience that doesn't typically come from a classroom setting. 
                Unlike many of our competitors, our team has a modest budget and limited personnel, and we've had to find creative ways to overcome our challenges. 
                As a result, I’ve had experience fulfilling ambitious engineering goals in short design cycles, using limited resources and innovative designs both as a design lead, and as an administrative lead for my team.
            </p>

            <p>
                I have years of experience with MATLAB and Python, especially with close-to-the-wire controls design and testing. I've delivered flight code to customers,
                I'm adept with multiple programming languages, such as Matlab, C, and Python, and I have strong communication and interpersonal skills.

            </p>
        </div>


    </div>
</section> -->


<!-- <div class="about-container">
    <div class="about">
        <div class="about-box">
            <img src={profile_pic} alt="Profile Picture">
        </div>
        <div>
            <h1>ABOUT ME</h1>
            <p> 
                My name is Jack Comey, and I'm a Guidance, Navigation, and Controls Engineer working in the space domain. I graduated from UC Davis in 2021, with a double Bachelor's degree in Aerospace Science and Engineering, and Mechanical Engineering. 
            </p>
            <p>
                I used the Covid-19 pandemic as an opportunity to improve my academic work and made the Dean's list three times during lockdown. I used the extra time available to take my work to the next level, and my team won the NASA ARMD Aeronautics competition as a part of the result of that.
                Since graduating, I've been at Lockheed Martin Space in Sunnyvale, working on precision motor controls for launch vehicle attitude control systems.
            </p>
            
            <p>
                In 2019, I lead an aircraft design team that competed in SAE Aero Design West, a heavy-lift aircraft design competition that competed last May against teams from a wide variety of nations. 
                Being a part of this team has provided invaluable hands-on design and leadership experience that doesn't typically come from a classroom setting. 
                Unlike many of our competitors, our team has a modest budget and limited personnel, and we've had to find creative ways to overcome our challenges. 
                As a result, I’ve had experience fulfilling ambitious engineering goals in short design cycles, using limited resources and innovative designs both as a design lead, and as an administrative lead for my team.
            </p>

            <p>
                I have years of experience with MATLAB and Python, especially with close-to-the-wire controls design and testing. I've delivered flight code to customers,
                I'm adept with multiple programming languages, such as Matlab, C, and Python, and I have strong communication and interpersonal skills.

            </p>
        </div>
    
    </div>
</div> -->




