# cliff-restaurant
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cliff Restaurant | Luxury Dining</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: 'Segoe UI', sans-serif;
}

body{
    background:#0f172a;
    color:white;
    scroll-behavior:smooth;
}

/* NAVIGATION */
nav{
    position:fixed;
    width:100%;
    top:0;
    background:rgba(0,0,0,0.8);
    padding:15px 40px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    z-index:1000;
}

nav h2{
    color:gold;
    letter-spacing:2px;
}

nav ul{
    list-style:none;
    display:flex;
    gap:20px;
}

nav ul li a{
    color:white;
    text-decoration:none;
    font-weight:500;
}

nav ul li a:hover{
    color:gold;
}

/* HERO SECTION */
header{
    height:100vh;
    background:linear-gradient(rgba(0,0,0,0.75), rgba(0,0,0,0.75)),
    url('cliff-bg.png') center/cover no-repeat;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:20px;
}

header h1{
    font-size:70px;
    letter-spacing:3px;
    text-transform:uppercase;
    border:3px solid gold;
    padding:20px 40px;
}

header p{
    margin-top:20px;
    font-size:20px;
    color:#ddd;
}

/* SECTIONS */
section{
    padding:100px 20px;
    text-align:center;
}

section h2{
    font-size:36px;
    margin-bottom:20px;
    color:gold;
}

/* ABOUT */
.about{
    max-width:900px;
    margin:auto;
    color:#ccc;
    line-height:1.8;
}

/* MENU */
.menu-container{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:30px;
    max-width:1100px;
    margin:auto;
}

.menu-item{
    background:#1e293b;
    padding:20px;
    border-radius:10px;
    transition:0.3s;
}

.menu-item:hover{
    transform:translateY(-10px);
}

.menu-item h3{
    color:gold;
}

/* FORM */
form{
    max-width:500px;
    margin:auto;
}

input, select, textarea{
    width:100%;
    padding:12px;
    margin:10px 0;
    border:none;
    border-radius:5px;
}

button{
    background:gold;
    border:none;
    padding:12px 20px;
    cursor:pointer;
    font-weight:bold;
    transition:0.3s;
}

button:hover{
    background:white;
    color:black;
}

/* FOOTER */
footer{
    background:#111;
    padding:40px;
    text-align:center;
}

/* MODAL */
.modal{
    display:none;
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    background:rgba(0,0,0,0.8);
    align-items:center;
    justify-content:center;
}

.modal-content{
    background:#1e293b;
    padding:30px;
    border-radius:10px;
}

/* WHATSAPP FLOAT */
.whatsapp-float{
    position:fixed;
    bottom:20px;
    right:20px;
    background:#25D366;
    color:white;
    font-size:28px;
    width:60px;
    height:60px;
    border-radius:50%;
    display:flex;
    align-items:center;
    justify-content:center;
    text-decoration:none;
}

/* RESPONSIVE */
@media(max-width:768px){
    header h1{
        font-size:40px;
    }

    nav ul{
        display:none;
    }
}
</style>
</head>

<body>

<nav>
    <h2>CLIFF</h2>
    <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#reservation">Reservation</a></li>
        <li><a href="#contact">Contact</a></li>
    </ul>
</nav>

<header>
    <div>
        <h1>Cliff Restaurant</h1>
        <p>Luxury Dining Above The Ocean</p>
    </div>
</header>

<section id="about">
    <h2>About Us</h2>
    <div class="about">
        <p>
        Experience breathtaking ocean views, gourmet meals, and unforgettable moments.
        Cliff Restaurant combines elegance and nature to deliver a dining experience like no other.
        </p>
    </div>
</section>

<section id="menu">
    <h2>Our Special Menu</h2>
    <div class="menu-container">
        <div class="menu-item">
            <h3>Grilled Salmon</h3>
            <p>Ksh 2,500</p>
        </div>
        <div class="menu-item">
            <h3>Steak Deluxe</h3>
            <p>Ksh 3,200</p>
        </div>
        <div class="menu-item">
            <h3>Seafood Platter</h3>
            <p>Ksh 4,500</p>
        </div>
    </div>
</section>

<section id="reservation">
    <h2>Reserve a Table</h2>
    <form onsubmit="handleReservation(event)">
        <input type="text" placeholder="Full Name" required>
        <input type="email" placeholder="Email Address" required>
        <input type="date" required>
        <select required>
            <option value="">Select Time</option>
            <option>12:00 PM</option>
            <option>3:00 PM</option>
            <option>7:00 PM</option>
        </select>
        <select required>
            <option value="">Guests</option>
            <option>1</option>
            <option>2</option>
            <option>4</option>
            <option>6</option>
        </select>
        <textarea placeholder="Special Requests"></textarea>
        <button type="submit">Request Reservation</button>
    </form>
</section>

<section id="contact">
    <h2>Find Us</h2>
    <p>📞 +254 103 808 895</p>
    <p>📧 saidthekneg@gmail.com</p>
    <p>💰 M-Pesa: 0726815198</p>
    <br>
    <iframe 
        src="https://maps.google.com/maps?q=Nairobi&t=&z=13&ie=UTF8&iwloc=&output=embed"
        width="100%" height="300" style="border:0;">
    </iframe>
</section>

<footer>
    <p>© 2026 Cliff Restaurant | All Rights Reserved</p>
</footer>

<div class="modal" id="successModal">
    <div class="modal-content">
        <h2>Reservation Sent</h2>
        <p>Please send deposit to:</p>
        <h3>0726815198</h3>
        <br>
        <button onclick="closeModal()">Close</button>
    </div>
</div>

<a href="https://wa.me/254103808895" class="whatsapp-float" target="_blank">💬</a>

<script>
function handleReservation(e){
    e.preventDefault();

    const name = e.target.querySelector('input[type="text"]').value;
    const email = e.target.querySelector('input[type="email"]').value;
    const date = e.target.querySelector('input[type="date"]').value;
    const time = e.target.querySelectorAll('select')[0].value;
    const guests = e.target.querySelectorAll('select')[1].value;
    const requests = e.target.querySelector('textarea').value;

    const message = `
Reservation - Cliff Restaurant
Name: ${name}
Email: ${email}
Date: ${date}
Time: ${time}
Guests: ${guests}
Requests: ${requests}
    `;

    const encoded = encodeURIComponent(message);

    window.open(`https://wa.me/254103808895?text=${encoded}`, '_blank');
    window.open(`mailto:saidthekneg@gmail.com?subject=Reservation&body=${encoded}`);

    document.getElementById("successModal").style.display="flex";
    e.target.reset();
}

function closeModal(){
    document.getElementById("successModal").style.display="none";
}
</script>

</body>
</html>
