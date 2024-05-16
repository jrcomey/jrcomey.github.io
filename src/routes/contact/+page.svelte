<script>
    /** @type {import('./$types').PageData} */
    import Header from '../Header.svelte';
    export let data;
    let profile_pic = "src/assets/profile.JPG";
    let moon_pic = "src/assets/moon_pic.jpg";
</script>

    <Header/>

    <section>
        <div class="shaded-background">
            <div class="description">
                <h1>Contact Me!</h1>

                <p>If you'd like to reach out, whether it's to discuss some of my work that you've seen here or another topic, please don't hesitate to reach out. I prefer contact through email, at <a href="mailto:jack.rhys.comey@gmail.com">jack.rhys.comey@gmail.com</a>, but you can otherwise contact me through the form on this page.</p>
            </div>
            <div class="image-reel">
                <h2>Contact Form:</h2>
                <form action="https://api.staticforms.xyz/submit" method="post">
                    <input type="text" name="name" placeholder="Your Name">
                    <input type="text" name="email" placeholder="Your Email" />
                    <textarea name="message" placeholder="Your message here"></textarea>
                    <input type="text" name="honeypot" style="display:none">
                    <input type="hidden" name="accessKey" value="aaaaaaaa-bbbb-cccc-dddd-eeee6666kkkk">
                    <input type="hidden" name="subject" value="Contact us from - example.com" />
                    <input type="hidden" name="replyTo" value="@">
                    <input type="hidden" name="redirectTo" value="https://example.com/contact/success">
                    <input type="submit" value="Submit" />
                </form>
            </div>
            
        </div>
    </section>
    
    <!-- Make sure you don't change the form action-->
    

<style>

    section {
        background-image: url("./src/assets/moon_pic.jpg");
        align-content: center;
        background-size: cover;
        position: relative;
        height: 90vh;
    }

    .shaded-background {
        background-color: #0f1112CC;
        /* display: flex; */
        /* flex-direction: row; */
        padding: 5%;
        border-radius: 2%;
        display: grid;
        /* grid-row: 1; */
        grid-template-columns: 5fr 2fr;
        /* padding: 5%; */
        align-content: left;
        height: 100%;
    }

    .image-reel {
        /* border: 5%; */
        margin: 5%;
        align-content: center;
        justify-content: center;
        display: flex;
        flex-direction: column;        
    }

    .description {
        margin: 5%;
    }

    .image-reel form{
        width: 100%;
        object-fit: cover;
        aspect-ratio: 1;
        border-radius: 5%;
        display: flex;
        flex-direction: column;
        height: 100%;
    }

    /* .description h1{
        text-align: center;
    } */

    .contact-me{
        display: flex;
        flex-direction: column;
        justify-content: start;
        min-height: 100vh;
    }

    .contact-me form{
        display: flex;
        flex-direction: column;
    }


</style>