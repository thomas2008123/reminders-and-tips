# reminders-and-tips


center

   display: block;
    margin: auto; 

set width

   max width:





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
