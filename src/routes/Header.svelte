<script>
    export let title = "JRC Portfolio Website"
</script>

<header class="bg-blue-500 text-white p-4">
    <!-- <h1 class="text-3xl font-semibold">{title}</h1> -->
    <!-- <nav class="mt-4 flex">
        <ul class="flex space-x-4">
            <li><a href="#" class="hover:text-blue-700">Home</a></li>
            <li><a href="#" class="hover:text-blue-700">Blog</a></li>
            <li><a href="#" class="hover:text-blue-700">About</a></li>            
            <li><a href="#" class="hover:text-blue-700">Hire Me</a></li>
        </ul>
    </nav> -->

    <!-- <h4>Portfolio | Jack Comey</h4> -->
            <nav>
                <ul>
                  <li><a href="/">Home</a></li>
                  <li><a href="/about">About</a></li>
                  <li><a href="/projects">Projects</a></li>
                  <!-- <li><a href="/blog" class="dropdown-toggle">Blog</a></li> -->
                  <li><a href="https://github.com/jrcomey">GitHub</a></li>
                  <li><a href="/contact">Contact</a></li>
                </ul>
              </nav>

</header>

<style>

header {
    background-color: #0f111296;
    /* background-image: url(windy_hill_forest_1.jpg); */
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-size: cover;
    color: #fff;
    padding: 0 5vw;
    top: 0;
    left: 0;
    width: 100%;
    position: fixed;
    z-index: 100;
}
/* 
header h1 {
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.7);
  } */

main section:first-child {
    margin-top: 10%;
}

nav ul {
    z-index: 1;
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin-right: 10px;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
}

.dropdown {
    position: relative;
    z-index: 1;
}

.dropdown-list {
    display: none;
    position: absolute;
    top: 100%;
    left: 0;
    background-color: #f5f5f5;
    padding: 0;
    margin: 0;
    list-style: none;
    border: 1px solid #ccc;
    z-index: 1;
  }

.dropdown-list li {
    padding: 10px;
    display: block;
    white-space: nowrap;
  }

.dropdown-list li:hover {
    background-color: #f5f5f5;
    
  }

  .dropdown-toggle:hover + .dropdown-list,
.dropdown-list:hover {
  display: block;
  
}

a:hover {
  text-decoration: underline;
}
</style>

