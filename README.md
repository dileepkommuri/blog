<!DOCTYPE html>
<html lang="en">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Your Professional Blog</title>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/jquery.slick/1.6.0/slick.css" />
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/jquery.slick/1.6.0/slick-theme.css" />
<style>
body {
font-family: 'Arial', sans-serif;
margin: 0;
padding: 0;
background-color: #06080a; /* Dark background color */
color: #ecf0f1; /* Light text color */
scroll-behavior: smooth;
scroll-padding-top: 2rem;
box-sizing: border-box;
}

:root {
--container-color: #573f75; /* Darker container color */
--second-color: #04090cd8; /* Blue accent color */
--text-color: #ecf0f1; /* Light text color */
--bg-color: #08090a; /* Dark background color */
}

::selection {
color: var(--bg-color);
background: var(--second-color);
}

a {
text-decoration: none;
color: #F0F1EC; /* Red link color */
}

li {
list-style: none;
}

img {
width: 100%;
}

section {
padding: 3rem 0 2rem;
}

.container {
max-width: 1068px;
margin: auto;
width: 100%;
background-color: var(--container-color); /* Darker container color */
padding: 20px;
border-radius: 10px; /* Rounded corners for container */
box-shadow: 0 0 10px rgba(8, 8, 8, 0.1);
}

a {
color: #fff;
}

.clearfix::after{
    content: '';
    display: block;
    clear: both;
}

.btn{
    padding: .5rem 1rem;
    background: #54f91dd8;
    color: white;
    border: 1px solid transparent;
    border-radius: .25rem;
}
header {
position: fixed;
top: 0;
left: 0;
width: 100%;
z-index: 200;
}

header.shadow {
background: var(--bg-color);
box-shadow: 0 1px 4px hsla(0, 2%, 10%, 0.1);
transition: .5s;
}

header.shadow .logo {
color: var(--text-color);
}

.nav {
display: flex;
align-items: center;
justify-content: space-between;
padding: 18px 0;
}

.logo {
font-size: 1.5rem;
font-weight: 600;
color: var(--bg-color);
}

.logo span {
color: var(--second-color);
}

.login {
padding: 8px 14px;
text-transform: uppercase;
font-weight: 500;
border-radius: 4px;
background: var(--second-color);
color: var(--bg-color);
}

.login:hover {
background: hsl(198, 93%, 5%);
transition: .5s;
}

.home {
width: 100%;
min-height: 440px;
background: url("images/banner2.png");
display: grid;
justify-content: center;
align-items: center;
}

.home-text {
color: var(--bg-color);
text-align: center;
}

.home-title {
font-size: 3.5rem;
}

.home-subtitle {
font-size: 1rem;
font-weight: 400;
}

.about {
position: relative;
width: 100%;
display: flex !important;
justify-content: center;
align-items: center;
}

.about .contentBx {
max-width: 50%;
width: 50%;
text-align: left;
padding-right: 40px;
}

.titleText {
font-weight: 600;
color: #111;
font-size: 2rem;
margin-bottom: 10px;
}

.title-text {
color: #111;
font-size: 1em;
}

.about .imgBx {
position: relative;
min-width: 50%;
width: 50%;
min-height: 500px;
}

.btn2 {
position: relative;
display: inline-block;
margin-top: 30px;
padding: 10px 30px;
background: #fff;
border: .8px solid #111;
color: #333;
text-decoration: none;
transition: 0.5s;
}

.btn2:hover {
background-color: var(--second-color);
border: none;
color: #fff;
}

.post-filter {
display: flex;
justify-content: center;
align-items: center;
column-gap: 1.5rem;
margin-top: 2rem !important;
}

.filter-item {
font-size: 0.9rem;
font-weight: 500;
cursor: pointer;
}

.active-filter {
background: var(--second-color);
color: var(--bg-color);
padding: 4px 10px;
border-radius: 4px;
}

.post {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(280px, auto));
justify-content: center;
gap: 1.5rem;
}

.post-box {
background: var(--bg-color);
box-shadow: 0 4px 14px hsl(35deg 25% 15% / 10%);
padding: 15px;
border-radius: 0.5rem;
}

.post-img {
width: 100%;
height: 200px;
object-fit: cover;
object-position: center;
border-radius: 0.5rem;
}

.category {
font-size: 0.9rem;
font-weight: 500;
text-transform: uppercase;
color: var(--second-color);
}

.post-title {
font-size: 1.3rem;
font-weight: 600;
color: var(--text-color);
display: -webkit-box;
-webkit-line-clamp: 2;
-webkit-box-orient: vertical;
overflow: hidden;
}

.post-date {
display: flex;
font-size: 0.875rem;
text-transform: uppercase;
margin-top: 4px;
font-weight: 400;
}

.post-description {
font-size: 0.9rem;
line-height: 1.5rem;
margin: 5px 0 10px;
display: -webkit-box;
-webkit-line-clamp: 2;
-webkit-box-orient: vertical;
overflow: hidden;
}

.profile {
display: flex;
align-items: center;
gap: 10px;
}

.profile-img {
width: 40px;
height: 40px;
object-fit: cover;
object-position: center;
border-radius: 50%;
}

.profile-name {
font-size: 0.9rem;
color: var(--text-color);
font-weight: 600;
}

.slick-slider {
margin-top: 20px;
}

.slick-slide img {
border-radius: 15px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
width: 100%;
height: auto;
}

nav {
background-color: #34495e; /* Darker navigation bar color */
padding: 10px;
text-align: center;
}

nav a {
color: #ecf0f1;
margin: 0 15px;
text-decoration: none;
font-weight: bold;
transition: color 0.3s ease;
}

nav a:hover {
color: #3498db;
}

.tab-content {
padding: 20px;
}

h2,
h3 {
color: #3498db;
}

/* Add hover effect to nav links */
nav a:hover {
color: #3498db;
transform: scale(1.1);
transition: color 0.3s ease, transform 0.3s ease;
}

/* Add animation to home-title */
.home-title {
font-size: 3.5rem;
animation: bounce 1s infinite alternate;
}

@keyframes bounce {
0% {
transform: translateY(0);
}

100% {
transform: translateY(-10px);
}
}

/* Add hover effect to btn2 */
.btn2:hover {
background-color: var(--second-color);
border: none;
color: #fff;
transform: translateY(-2px);
transition: background-color 0.5s ease, transform 0.5s ease;
}

/* Add hover effect to post-box */
.post-box:hover {
transform: scale(1.03);
transition: transform 0.3s ease;
}

/* Add hover effect to filter-item */
.filter-item:hover {
color: var(--second-color);
transition: color 0.3s ease;
}

/* Add hover effect to slick-slider images */
.slick-slide img:hover {
transform: scale(1.1);
transition: transform 0.5s ease;
}
</style>
</head>

<body>
<header>
<div class="nav container">
<div class="logo">KOMMURI DILEEP KUMAR <span>Blog</span></div>
<nav>
</nav>
</div>
</header>

<div class="home" id="home" style="min-height: 300px;">
<div class="home-text">
<h1 class="home-title" style="color: #ecf0f1;">KOMMURI DILEEP KUMAR Blog</h1>
<p class="home-subtitle" style="color: #ecf0f1;">Traveler's Haven</p>
</div>
</div>


<div class="container">
<ul class="nav nav-tabs" id="myTabs">
<li class="nav-item">
<a class="nav-link active" data-toggle="tab" href="#about">About Me</a>
</li>
<li class="nav-item">
<a class="nav-link" data-toggle="tab" href="#contact">Contact</a>
</li>
<li class="nav-item">
<a class="nav-link" data-toggle="tab" href="#personal">Personal Information</a>
</li>
<li class="nav-item">
<a class="nav-link" data-toggle="tab" href="#skills">Skills</a>
</li>
<li class="nav-item">
    <a class="nav-link" data-toggle="tab" href="#projects">Projects</a>
    </li>
<li class="nav-item">
<a class="nav-link" data-toggle="tab" href="#hobbies">Hobbies</a>
</li>
<li class="nav-item">
<a class="nav-link" data-toggle="tab" href="#slider">Slider</a>
</li>
</ul>

<div class="tab-content">
<div class="tab-pane fade show active" id="about">
<section>
<h2>About Me</h2>
<p>Welcome to my corner of the internet where I share my passion for exploring the world, one destination at a time. I'm KOMMURI DILEEP KUMAR , a travel enthusiast and avid adventurer on a mission to inspire others to embark on their own transformative journeys. Through my travel blog, I invite you to join me as I wander through bustling cities, traverse scenic landscapes, and immerse myself in diverse cultures around the globe.</p>
</section>
</div>

<div class="tab-pane fade" id="contact">
<section class="contact-info">
<h2>Contact Information</h2>
<button class="btn btn-primary mb-3 collapse-section" data-toggle="collapse" data-target="#contactDetails">Show Contact Details</button>
<div id="contactDetails" class="collapse">
<ul>
<li><strong>Email:</strong> <a href="mailto:your.email@example.com">kommuridileep333@gmail.com</a></li>
<li><strong>Phone:</strong> 9398595152</li>
</ul>
</div>
<form>
<div class="form-group">
<label for="message">Send me a message:</label>
<textarea class="form-control" id="message" rows="3"></textarea>
</div>
<button type="submit" class="btn btn-primary">Send Message</button>
</form>
</section>
</div>

<div class="tab-pane fade" id="personal">
    <section class="Personal">
    <h2>Personal Information</h2>
    <ul>
    <li><strong>BTech:</strong> Malla Reddy College of Engineering and Technology </li>
    <li><strong>SSC:</strong> Sri Chaitanya Techno School</li>
    <li><strong>Intermediate:</strong> Sri Chaitanya junior Collage</li>
    </ul>
    </section>
    </div>
    


<div class="tab-pane fade" id="skills">
<section class="skills">
<h2>Skills</h2>
<ul>
<li><strong>Technical Skills:</strong> java, python, HTML, CSS </li>
<li><strong>Soft Skills:</strong> Time management, problem solving, teamwork and collaboration,Adaptability</li>
</ul>
</section>
</div>

<div class="tab-pane fade" id="projects">
    
    <div class="content">
        <div class="main-content">

        <h2>Projects</h2>
    </div>
    <div class="sidebar"></div>
    </div>
    
    <article>
    <h3>Spam Email Detection</h3>
    <p><strong>Role:</strong> backend</p>
    <p><strong>Description:</strong> Spam email is unsolicited and unwanted junk email sent out in bulk to an indiscriminate recipient list. Typically, spam is sent for commercial purposes. It can be sent in massive volume by botnets, networks of infected computers.</p>
    </article>
    <article>
    <h3>Fake Reviews Detection </h3>
    <p><strong>Role:</strong> backend</p>
    <p><strong>Description:</strong> Fake Review Detection will help us to identify whether the opinion given to the product is a true or fake review. Various methods can be used to detect it but we are focusing on finding the results using Machine learning Techniques. Our method focuses on the text content of the costumer reviews.</p>
    </article>
    </section>
    </div>

<div class="tab-pane fade" id="hobbies">
<section>
<h2>Hobbies and Interests</h2>
<p>Outside of work, I enjoy Travelling, Watching Movies, Listening to music.</p>
</section>
</div>
<!-- Added a new tab for the Slider -->
<div class="tab-pane fade" id="slider">
<section class="slick-slider">
<div><img src="C:\Users\akhil\OneDrive\Desktop\travel1.jpg" alt="Slide 1"></div>
<div><img src="C:\Users\akhil\OneDrive\Desktop\travel2.jpg" alt="Slide 2"></div>
<div><img src="C:\Users\akhil\OneDrive\Desktop\travel3.jpg" alt="Slide 3"></div>
<!-- Add more images as needed -->
</section>
</div>
</div>
</div>
<!-- Bootstrap JS and Popper.js -->
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"></script>

<!-- Slick Carousel JS -->
<script type="text/javascript" src="https://cdn.jsdelivr.net/jquery.slick/1.6.0/slick.min.js"></script>

<script>
$(document).ready(function () {
$('.slick-slider').slick({
slidesToShow: 1,
slidesToScroll: 1,
autoplay: true,
autoplaySpeed: 2000,
dots: true,
arrows: false
});

// Smooth scrolling for anchor links
$('a[href^="#"]').on('click', function (event) {
event.preventDefault();
$('html, body').animate({
scrollTop: $($.attr(this, 'href')).offset().top
}, 500);
});

// Toggle collapse for contact details
$('.collapse-section').click(function () {
$(this).text(function (i, text) {
return text === "Show Contact Details" ? "Hide Contact Details" : "Show Contact Details";
});
});

// Change navbar style on scroll
$(window).scroll(function () {
if ($(this).scrollTop() > 50) {
$('header').addClass('shadow');
} else {
$('header').removeClass('shadow');
}
});
});
</script>
</body>

</html>
