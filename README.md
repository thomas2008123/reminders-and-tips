# reminders-and-tips



Task 3A Data Collection 
To begin with, I made 2 separate YouTube videos showcasing the technical and non-technical sides of the website.
For the non-technical side I made a video showcasing the website itself rather than any of the code. This side helps to provide the user with a basic view of how the website functions from page to page and how the user experience would be. This allows for good data collection as it can reach a wide audience and it allows a firsthand view for the user as they are guided through the site. Given more time however, or a better working environment I would have dubbed the video over and emphasised certain parts as well as editing it down to where the user viewing it could get better explanations.
Non-technical video : https://youtu.be/QAU_8Pj5maM
For the technical side however, I made a video which instead showcased the JS code rather than the actual site as this allows for technical users to look at the code and give data on what could be improved with the code for the site to flow better as a whole. 
Given more time on this video I would have done similar adjustments to the ones mentioned in the non-technical fixes, but I would have also explained more of the code such as the CSS and html as well as the structure of the code and the way I organised it in order to make changes to code easy and effortless.
Technical video: https://www.youtube.com/watch?v=_rkhKpgwKiU
by getting both sides of the user database, the website will be able to develop much faster, as well as be a better and safer environment which is kindred to the users’ needs being especially developed for them.
Next I condensed the website down to a zip file and sent it to separate users so they could trial the site and see how it functions or see any way it could be improved, then along with this I would send a questionnaire the user can fill out so that I can collect data quickly and efficiently, to do this on a mass scale I decided to send to different departments in my college and to my friends so that I could have a wide user feedback with all different types of views.
Non-technical questionnaire: https://youtu.be/QAU_8Pj5maM    
technical questionnaire: https://www.youtube.com/watch?v=_rkhKpgwKiU
Then outside of college I interviewed a range of different users with different experience in technology from my parents & friends to people I work with at placement.


Interview questions:
Non-technical:
were there any points where you felt unsure of what you had to do?
what changes could of made you have a better experience?
Did you find the sites layout to make sense and be coherent throughout?
Was there anything you found to be frustrating?
Which feature did you find easiest and hardest to use?

parent 1
Were there any points where you felt unsure of what you had to do?
"at first i found it difficult to use as things on login page were not so well labelled, but i think that once i logged in it was easy to use"

What changes could have made you have a better experience?
"I think that the navbar could have better labels for the pages"

Did you find the site’s layout to make sense and be coherent throughout?
"The site is very well layed out and easy to follow"

Was there anything you found to be frustrating?
"Just that links could have been labeled slightly better"

Which feature did you find easiest and hardest to use?
"I found that the main parts of the site were well made and easy to understand, but the site could be better labeled"

parent 2 

Were there any points where you felt unsure of what you had to do?
"At first I took a moment to understand the login page, but after that everything was clear and easy to use."

What changes could have made you have a better experience?
"not much needed changing. The colour scheme was nice, the font size was good, and everything was easy to read."

Did you find the site’s layout to make sense and be coherent throughout?
"Yes, the site is very well layed out and quite consistent"

Was there anything you found to be frustrating?
"No, I did not find anything frustrating i think everything worked smoothly"

Which feature did you find easiest and hardest to use?
"I found the main features very easy to use and understand there was nothing particularly hard to use."

friend

Were there any points where you felt unsure of what you had to do?
"Not really honestly, it was pretty easy to use from login and i could tell where everything was meant to be"

What changes could have made you have a better experience?
"Would be a bit better with a more modern type of design with animations from page to page currently feels a little static ."

Did you find the site’s layout to make sense and be coherent throughout?
"thought that the layout all made sense and stayed coherent with other pages "

Was there anything you found to be frustrating?
"no was pretty simple to use"

Which feature did you find easiest and hardest to use?
"Thought that easiest feature was navigating through the site between pages but thought it was a bit hard to login at first"

Technical:
Were there any areas of code which you found to be unclear or insufficient?
Can you talk about any bugs which you encountered within the code?
Did you find any vulnerabilities within the code?
If you had to optimise one piece of the code what would it be?
Does the prototype follow good development practices?

I messaged some technical users online to gain further feedback on the prototype. This helped me collect opinions from people with stronger development knowledge.

technical user 1

Were there any areas of code which you found to be unclear or insufficient?
“The overall code was understandable, but some sections could be organised better and separated into smaller reusable functions.”

Can you talk about any bugs which you encountered within the code?
“I did not notice any major bugs, although there were a few minor styling inconsistencies on some pages.”

Did you find any vulnerabilities within the code?
“The main vulnerability would be relying on local storage for data. This is acceptable for a prototype, but a live system should use a secure back-end database.”

If you had to optimise one piece of the code what would it be?
“I would reduce repeated CSS and reorganise stylesheets so they are easier to maintain.”

Does the prototype follow good development practices?
“it follows good practices for a prototype and shows clear effort in planning and structure.”

technical user 2 

Technical User 2 – Online Software Engineer

Were there any areas of code which you found to be unclear or insufficient?
“The code was well commented and mostly easy to follow however some larger functions could be split into smaller modules.”

Can you talk about any bugs which you encountered within the code?
“I did not encounter any serious bugs, most features worked as expected during testing.”

Did you find any vulnerabilities within the code?
“Security could be improved further by using stronger password hashing and server-side authentication instead of relying on client-side storage.”

If you had to optimise one piece of the code what would it be?
“I would optimise the security of the project by moving user data to a secure back-end database.”

Does the prototype follow good development practices?
“This prototype presents good front-end development practices, clear commenting and a clear logical structure.”

Responses I got:
Response to feedback:
Questionnaire:
Interview: 


Building the Webpage – Development Explanation
1. Creating the Base HTML Structure

The first step was creating the basic HTML document structure. This ensures the browser correctly interprets the page and allows external files such as CSS to be linked.

Important elements included:

<!DOCTYPE html> to define the document type

<meta charset> to support different characters

<meta name="viewport"> to ensure the page is responsive

<link rel="stylesheet"> to connect the CSS stylesheet

Example:

<!DOCTYPE html>
<html lang="en">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title></title>
<link rel="stylesheet" href="style.css">
</head>
2. Structuring the Page Layout

The body of the webpage was organised using semantic HTML elements such as:

header

main

section

footer

These improve accessibility and search engine optimisation.

Example:

<body>

<header class="navbar">
</header>

<main>
<section class="section">
</section>
</main>

<footer class="footer">
</footer>

</body>
3. Creating the Navigation Bar

The navigation bar was created using a <header> element with links inside a <nav> element. This clearly defines the main navigation for screen readers.

Example:

<header class="navbar">

<div class="logo">
<img src="images/logo.png" alt="Website logo">
</div>

<nav aria-label="Main Navigation">
<a href="#">Home</a>
<a href="#">Our Producers</a>
<a href="#">Join Us</a>
<a href="#">Orders</a>
</nav>

</header>

To position the elements across the top of the page, Flexbox was used.

.navbar{
display:flex;
justify-content:space-between;
align-items:center;
padding:15px 40px;
background:#faf1e1;
}

Flexbox allows items to spread across the horizontal space and stay aligned vertically.

4. Creating a Promotional Banner

A promotional message was added below the navigation bar using a <div> element.

This provides a clear call-to-action for users.

Example:

<div class="promo">

</div>

The banner was styled using CSS:

.promo{
background:#8a622e;
color:white;
text-align:center;
padding:8px;
font-weight:600;
}
5. Creating Page Sections

Content was grouped into sections using the <section> element. This helps organise the page into logical areas.

Example:

<section class="section">

<h2>Section Title</h2>

<div class="grid">
<div class="card"></div>
<div class="card"></div>
</div>

</section>

The sections were centred and spaced using CSS.

.section{
padding:60px 40px;
max-width:1700px;
margin:auto;
text-align:center;
}
6. Using CSS Grid for Layout

Inside each section, CSS Grid was used to create a two-column layout.

Example:

.grid{
display:grid;
grid-template-columns:1fr 1fr;
gap:40px;
margin-top:20px;
}

grid-template-columns: 1fr 1fr; splits the layout into two equal columns, allowing content to sit side-by-side.

7. Creating Card Components

Reusable card containers were created to group content and images. This keeps the layout consistent.

Example:

<div class="card">
<p>Example content inside the card.</p>
</div>

CSS styling:

.card{
background:#e9dcc6;
padding:20px;
border-radius:20px;
}

Rounded corners and padding make the content easier to read and visually separated.

8. Adding Buttons

Buttons were added to allow user interaction.

Example:

<button>Action Button</button>

CSS styling:

button{
margin-top:15px;
padding:15px 30px;
border:none;
border-radius:30px;
background:#8a622e;
color:white;
font-weight:bold;
cursor:pointer;
}

The cursor:pointer property indicates that the element is clickable.

9. Creating the Footer

The footer contains additional navigation links and contact information.

Example:

<footer class="footer">

<div>
<h3>Greenfield Local Hub</h3>
<p>Message us at:</p>
<p>GreenfieldLocalHub@gmail.com</p>
</div>

<div>
<a href="#">Join Our Loyalty Club</a>
<a href="#">Our Producers</a>
<a href="#">Your Orders</a>
</div>

</footer>

Flexbox was used again to space the columns evenly.

.footer{
display:flex;
justify-content:space-between;
flex-wrap:wrap;
gap:40px;
}
10. Making the Page Fill the Screen

The body was set to use Flexbox so the footer remains at the bottom of the page.

Example:

body{
display:flex;
flex-direction:column;
min-height:100vh;
}

main{ flex:1; } allows the main content to expand and push the footer down.

nav

display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 15px 40px;


    justify content: flex 

button:hover {
    transform: scale(1.05);
}

transition: all .4s ease;

position fixed 
bottom 0

center

   display: block;
    margin: auto; 

set width

   max width:

body 

body {
    font-family: Arial, sans-serif;
    background: #f4f6f8;
    min-height: 100vh;
    display: flex;
    flex-direction: column; 
    min-height: 100vh; /* Ensures footer sticks to bottom */
    margin: 0;
    }
    

Add nav links as a class around the links
<ul class="nav-links">
</ul>

footer

.footer {
    background-color: #FF2A40;
    color: #f4f6f8;
    padding: 25px 40px;
    margin-top: auto; /* pushes footer to bottom */
}

.footer-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
}

.footer-links a {
    text-decoration: none;
    color: #f4f6f8;
    margin-right: 15px; 
}


/*
TABLE NOT SHOWING DATA? CHECK THESE FIRST:

1. renderTable() MUST receive an ARRAY
   ❌ renderTable(console.log(data))
   ✅ renderTable(myArray)

2. HTML IDs are CASE SENSITIVE
   JS:  getElementById("tableBody")
   HTML: id="tableBody"

3. Table structure MUST be:
   <table>
     <thead>...</thead>
     <tbody>...</tbody>
   </table>

4. Array must contain data
   console.log(consultations) before rendering

5. If forEach crashes → data is undefined or not an array
*/





📌 localStorage – Key Points

localStorage is a browser-based storage system

Data persists after page refresh

Stores data as key–value pairs

Values must be strings

Commonly used with JSON.stringify() and JSON.parse()

Data is specific to the website (origin-based)

Max size ≈ 5MB

📌 Why localStorage was used in this project

Prevents data loss on refresh

No server or database required

Easy to implement using JavaScript

Suitable for small datasets like form entries

📌 localStorage vs CSV
Feature	localStorage	CSV
Survives refresh	✅	❌
Auto-loads	✅	❌
Exportable	❌	✅
Secure	Browser-only	File-based
Best use	Persistence	Backup / sharing
📌 Example Code (reference)
// Save data
localStorage.setItem("consultations", JSON.stringify(consultations));

// Load data
const stored = localStorage.getItem("consultations");
if (stored) {
  consultations = JSON.parse(stored);
}

📌 Common mistakes to avoid

Forgetting to stringify objects

Using different key names when saving/loading

Expecting CSV files to auto-load

Clearing localStorage unintentionally


.reduce p {
    max-width: 50%;
    text-align: center;
    margin: 0 auto;
} add margin 0 auto to ensure items center properly

How to add a line between text

<p>First section of text</p>

<hr>

<p>Second section of text</p> 


* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: system-ui, sans-serif;
}

/* Navbar */
.navbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: #004648;
    padding: 15px 20px;
    position: relative;
}

.logo {
    color: white;
    font-weight: bold;
    font-size: 18px;
}

/* Hide checkbox */
#menu-toggle {
    display: none;
}

/* Hamburger icon */
.hamburger {
    display: none;
    flex-direction: column;
    cursor: pointer;
}

.hamburger span {
    height: 3px;
    width: 25px;
    background: white;
    margin: 4px 0;
    transition: 0.3s;
}

/* Menu (desktop) */
.menu {
    list-style: none;
    display: flex;
    gap: 20px;
}

.menu a {
    color: white;
    text-decoration: none;
    font-size: 15px;
}

/* MOBILE STYLES */
@media (max-width: 768px) {

    /* Show hamburger */
    .hamburger {
        display: flex;
    }

    /* Hide menu by default */
    .menu {
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        background: #004648;
        flex-direction: column;
        overflow: hidden;
        max-height: 0;
        transition: max-height 0.3s ease;
    }

    .menu li {
        text-align: center;
        padding: 15px 0;
    }

    /* Toggle menu open */
    #menu-toggle:checked ~ .menu {
        max-height: 300px;
    }
}


<nav class="navbar">
    <div class="logo">MySite</div>

    <!-- Checkbox toggle -->
    <input type="checkbox" id="menu-toggle">

    <!-- Hamburger icon -->
    <label for="menu-toggle" class="hamburger">
        <span></span>
        <span></span>
        <span></span>
    </label>

    <!-- Menu -->
    <ul class="menu">
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
    </ul>
</nav>


writing forms 

 HOW TO DO TEXT NEXT TO IMAGE

<section class="image-text">
    <img src="img/consultations.png" alt="Sustainable energy illustration">

    <div class="image-text-content">
        <h2>Reduce Your Carbon Footprint</h2>
        <p>
            Small changes can make a big difference. Switching to renewable
            energy, driving electric vehicles, and reducing flights all help
            lower emissions.
        </p>
        <p>
            Roslin Technologies helps you make informed, sustainable choices
            that benefit both the planet and your wallet.
        </p>
    </div>
</section> 


.image-text {
    display: flex;
    align-items: center;
    gap: 40px;
    max-width: 1200px;
    margin: 80px auto;
    padding: 20px;
}

.image-text img {
    width: 45%;
    border-radius: 10px;
}

.image-text-content {
    width: 55%;
}

.image-text-content h2 {
    color: #004648;
    margin-bottom: 10px;
}

.image-text-content p {
    line-height: 1.6;
}

📱 Make it responsive (important)

Add this to your media query:

@media (max-width: 900px) {
    .image-text {
        flex-direction: column;
        text-align: center;
    }

    .image-text img,
    .image-text-content {
        width: 100%;
    }
}


Now it stacks cleanly on mobile.



Added regex email system 

html 
<div class="form-Email">
                <label for="Email">* Email</label>
                <input type="email" name="Email" id="Email" required>
                <small id="emailError"></small>
            </div>



            
js
const emailInput = document.getElementById("Email");
const emailError = document.getElementById("emailError");

const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

emailInput.addEventListener("input", () => {
    if (!emailRegex.test(emailInput.value)) {
        emailError.textContent = "Please enter a valid email address";
        emailError.style.color = "red";
    } else {
        emailError.textContent = "";
    }
});


Nice clean signup form 👍
To make it “work with hashing”, you need JavaScript to hash the password before you store or send it anywhere.

I’ll show you the correct approach, step by step, and explain why each part exists.

⚠️ First: important reality check

Pure HTML/JS hashing is OK for demos / coursework

Real apps MUST hash on the server (Node, PHP, Python, etc.)

Never store plain passwords

Never rely on client-side hashing alone for production

That said — here’s how to do it properly for a frontend-only setup.

Step 1: Add a submit button + script link

Update your HTML slightly:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Signup</title>
    <script defer src="signup.js"></script>
</head>
<body>
    <div class="wrapper">
        <h1>Signup</h1>

        <form id="signup-form">
            <div>
                <input type="text" id="firstname-input" placeholder="First name" required>
            </div>

            <div>
                <input type="email" id="email-input" placeholder="Email" required>
            </div>

            <div>
                <input type="password" id="password-input" placeholder="Password" required>
            </div>

            <button type="submit">Create Account</button>
        </form>
    </div>
</body>
</html>

Step 2: Hash the password using Web Crypto API

Create signup.js

This uses SHA-256, which is the correct browser-native hashing method.

const form = document.getElementById("signup-form");

form.addEventListener("submit", async (e) => {
    e.preventDefault();

    const firstname = document.getElementById("firstname-input").value;
    const email = document.getElementById("email-input").value;
    const password = document.getElementById("password-input").value;

    const hashedPassword = await hashPassword(password);

    const user = {
        firstname,
        email,
        password: hashedPassword
    };

    // Save to localStorage (demo only)
    localStorage.setItem("user", JSON.stringify(user));

    alert("Account created successfully!");
    console.log(user);
});

Step 3: The hashing function (this is the key part)
async function hashPassword(password) {
    const encoder = new TextEncoder();
    const data = encoder.encode(password);

    const hashBuffer = await crypto.subtle.digest("SHA-256", data);

    const hashArray = Array.from(new Uint8Array(hashBuffer));
    const hashHex = hashArray
        .map(byte => byte.toString(16).padStart(2, "0"))
        .join("");

    return hashHex;
}

What this does:

Converts password → binary

Hashes it using SHA-256

Outputs a safe hexadecimal string

Original password is never stored

Step 4: What gets stored (example)

Instead of:

"password": "mypassword123"


You get:

"password": "ef92b778ba..."


Even you can’t reverse it 🔐

Step 5: How login would work later

On login:

User enters password

Hash entered password

Compare hash with stored hash

If equal → success

if (hashedInputPassword === storedUser.password) {
    // login success
}

🔒 Important security notes (exam gold)

Hashing ≠ encryption (cannot be reversed)

Passwords should never be stored in plain text

Production systems use:

bcrypt

argon2

scrypt

These require a backend

Perfect — let’s bolt a login system straight onto what you already have 👍
This will:

Use the same hashing

Support login validation

Redirect to a home page on success

Stay copy-paste friendly

I’ll assume you’re using localStorage (frontend-only / coursework style).

1️⃣ Update SIGNUP to support multiple users (important)
🔁 signup.js (UPDATED)
const form = document.getElementById("signup-form");

form.addEventListener("submit", async (e) => {
    e.preventDefault();

    const firstname = document.getElementById("firstname-input").value;
    const email = document.getElementById("email-input").value;
    const password = document.getElementById("password-input").value;

    const hashedPassword = await hashPassword(password);

    const newUser = {
        firstname,
        email,
        password: hashedPassword
    };

    let users = JSON.parse(localStorage.getItem("users")) || [];

    // prevent duplicate accounts
    if (users.some(user => user.email === email)) {
        alert("Account already exists");
        return;
    }

    users.push(newUser);
    localStorage.setItem("users", JSON.stringify(users));

    alert("Signup successful!");
    window.location.href = "login.html";
});

async function hashPassword(password) {
    const encoder = new TextEncoder();
    const data = encoder.encode(password);
    const hashBuffer = await crypto.subtle.digest("SHA-256", data);

    return Array.from(new Uint8Array(hashBuffer))
        .map(b => b.toString(16).padStart(2, "0"))
        .join("");
}

2️⃣ Create login.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Login</title>
    <script defer src="login.js"></script>
</head>
<body>
    <div class="wrapper">
        <h1>Login</h1>

        <form id="login-form">
            <div>
                <input type="email" id="login-email" placeholder="Email" required>
            </div>

            <div>
                <input type="password" id="login-password" placeholder="Password" required>
            </div>

            <button type="submit">Login</button>
        </form>
    </div>
</body>
</html>

3️⃣ Create login.js
const form = document.getElementById("login-form");

form.addEventListener("submit", async (e) => {
    e.preventDefault();

    const email = document.getElementById("login-email").value;
    const password = document.getElementById("login-password").value;

    const users = JSON.parse(localStorage.getItem("users")) || [];
    const hashedPassword = await hashPassword(password);

    const user = users.find(
        u => u.email === email && u.password === hashedPassword
    );

    if (!user) {
        alert("Invalid email or password");
        return;
    }

    // save logged-in user session
    localStorage.setItem("loggedInUser", JSON.stringify(user));

    alert("Login successful!");
    window.location.href = "home.html";
});

async function hashPassword(password) {
    const encoder = new TextEncoder();
    const data = encoder.encode(password);
    const hashBuffer = await crypto.subtle.digest("SHA-256", data);

    return Array.from(new Uint8Array(hashBuffer))
        .map(b => b.toString(16).padStart(2, "0"))
        .join("");
}

4️⃣ Create a protected home.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Home</title>
    <script defer src="home.js"></script>
</head>
<body>
    <h1>Welcome</h1>
    <p id="user-name"></p>

    <button id="logout">Logout</button>
</body>
</html>

5️⃣ home.js (session check)
const user = JSON.parse(localStorage.getItem("loggedInUser"));

if (!user) {
    window.location.href = "login.html";
}

document.getElementById("user-name").textContent =
    `Hello, ${user.firstname}!`;

document.getElementById("logout").addEventListener("click", () => {
    localStorage.removeItem("loggedInUser");
    window.location.href = "login.html";
});

✅ What you now have (exam-ready)

✔ Password hashing
✔ Signup & login
✔ Duplicate account prevention
✔ Session handling
✔ Protected page
✔ Clean separation of files

🔒 Key line to mention for marks

“Passwords are hashed using SHA-256 before being stored. During login, the entered password is hashed and compared to the stored hash.”

If you want next:

🔐 Password strength checker

🧂 Salted hashing explanation

🧠 Teacher-proof security write-up

🌍 Backend version (Node / PHP)

Just say the word 😄




document.addEventListener("DOMContentLoaded", () => {
    const logoutLink = document.getElementById("logout-link");

    if (logoutLink) {
        logoutLink.addEventListener("click", (e) => {
            e.preventDefault();

            // Ask the user to confirm logout
            const confirmLogout = confirm("Are you sure you want to log out?");
            
            if (confirmLogout) {
                // User clicked OK, proceed with logout
                localStorage.removeItem("loggedInUser");
                window.location.href = "login.html";
            } else {
                // User clicked Cancel, do nothing
                return;
            }
        });
    }
});

<!--Sign out-->
            <a href="#" id="logout-link">Sign out</a>
css main body 

body {
    font-family: Arial, sans-serif;
    background: #f4f6f8;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}
