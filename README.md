# reminders-and-tips
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


