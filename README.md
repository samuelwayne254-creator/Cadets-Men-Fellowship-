# Cadets-Men-Fellowship
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cadets Men Fellowship</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
    scroll-behavior: smooth;
}

body {
    line-height: 1.6;
}

/* NAVBAR */
header {
    background: rgba(0,0,0,0.8);
    color: #fff;
    padding: 15px 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    z-index: 1000;
}

nav a {
    color: #fff;
    margin-left: 20px;
    text-decoration: none;
    transition: 0.3s;
}

nav a:hover {
    color: #f4a261;
}

/* HERO */
.hero {
    height: 100vh;
    background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)),
                url('https://images.unsplash.com/photo-1529070538774-1843cb3265df');
    background-size: cover;
    background-position: center;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 20px;
}

.hero h2 {
    font-size: 50px;
    animation: fadeInDown 1.5s ease;
}

.hero p {
    margin: 20px 0;
    font-size: 20px;
    animation: fadeInUp 1.5s ease;
}

.btn {
    background: #f4a261;
    color: #fff;
    padding: 12px 25px;
    border: none;
    cursor: pointer;
    border-radius: 5px;
    transition: transform 0.3s, background 0.3s;
}

.btn:hover {
    transform: scale(1.1);
    background: #e76f51;
}

/* FEATURES */
.features {
    padding: 60px 20px;
    text-align: center;
}

.feature-box {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}

.card {
    background: #f4f4f4;
    margin: 15px;
    padding: 25px;
    width: 280px;
    border-radius: 10px;
    transition: transform 0.4s, box-shadow 0.4s;
    opacity: 0;
    transform: translateY(40px);
}

.card.show {
    opacity: 1;
    transform: translateY(0);
}

.card:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.2);
}

/* FOOTER */
footer {
    background: #111;
    color: white;
    text-align: center;
    padding: 20px;
}

/* ANIMATIONS */
@keyframes fadeInDown {
    from {opacity: 0; transform: translateY(-50px);}
    to {opacity: 1; transform: translateY(0);}
}

@keyframes fadeInUp {
    from {opacity: 0; transform: translateY(50px);}
    to {opacity: 1; transform: translateY(0);}
}

/* RESPONSIVE */
@media (max-width: 768px) {
    header {
        flex-direction: column;
    }

    nav {
        margin-top: 10px;
    }

    .hero h2 {
        font-size: 32px;
    }

    .hero p {
        font-size: 16px;
    }
}
</style>
</head>

<body>

<header>
    <h1>Cadets Men Fellowship</h1>
    <nav>
        <a href="#">Home</a>
        <a href="#features">Mission</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<section class="hero">
    <div>
        <h2>Building Strong Men of Purpose</h2>
        <p>Empowering men through faith, discipline, and brotherhood.</p>
        <button class="btn">Join Us</button>
    </div>
</section>

<section class="features" id="features">
    <h3>Our Mission</h3>
    <div class="feature-box">
        <div class="card">
            <h4>Brotherhood</h4>
            <p>We stand together as one strong and united family.</p>
        </div>
        <div class="card">
            <h4>Discipline</h4>
            <p>We build character through consistency and commitment.</p>
        </div>
        <div class="card">
            <h4>Faith</h4>
            <p>We grow spiritually and walk in purpose.</p>
        </div>
    </div>
</section>

<footer id="contact">
    <p>© 2026 Cadets Men Fellowship | All Rights Reserved</p>
</footer>

<script>
// SCROLL ANIMATION
const cards = document.querySelectorAll('.card');

window.addEventListener('scroll', () => {
    cards.forEach(card => {
        const cardTop = card.getBoundingClientRect().top;
        if (cardTop < window.innerHeight - 50) {
            card.classList.add('show');
        }
    });
});
</script>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cadets Men Fellowship</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
    scroll-behavior: smooth;
}

body {
    line-height: 1.6;
}

/* NAVBAR */
header {
    background: rgba(0,0,0,0.8);
    color: #fff;
    padding: 15px 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    z-index: 1000;
}

nav a {
    color: #fff;
    margin-left: 20px;
    text-decoration: none;
    transition: 0.3s;
}

nav a:hover {
    color: #f4a261;
}

/* HERO */
.hero {
    height: 100vh;
    background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)),
                url('https://images.unsplash.com/photo-1529070538774-1843cb3265df');
    background-size: cover;
    background-position: center;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 20px;
}

.hero h2 {
    font-size: 50px;
    animation: fadeInDown 1.5s ease;
}

.hero p {
    margin: 20px 0;
    font-size: 20px;
    animation: fadeInUp 1.5s ease;
}

.btn {
    background: #f4a261;
    color: #fff;
    padding: 12px 25px;
    border: none;
    cursor: pointer;
    border-radius: 5px;
    transition: transform 0.3s, background 0.3s;
}

.btn:hover {
    transform: scale(1.1);
    background: #e76f51;
}

/* FEATURES */
.features {
    padding: 60px 20px;
    text-align: center;
}

.feature-box {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}

.card {
    background: #f4f4f4;
    margin: 15px;
    padding: 25px;
    width: 280px;
    border-radius: 10px;
    transition: transform 0.4s, box-shadow 0.4s;
    opacity: 0;
    transform: translateY(40px);
}

.card.show {
    opacity: 1;
    transform: translateY(0);
}

.card:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.2);
}

/* FOOTER */
footer {
    background: #111;
    color: white;
    text-align: center;
    padding: 20px;
}

/* ANIMATIONS */
@keyframes fadeInDown {
    from {opacity: 0; transform: translateY(-50px);}
    to {opacity: 1; transform: translateY(0);}
}

@keyframes fadeInUp {
    from {opacity: 0; transform: translateY(50px);}
    to {opacity: 1; transform: translateY(0);}
}

/* RESPONSIVE */
@media (max-width: 768px) {
    header {
        flex-direction: column;
    }

    nav {
        margin-top: 10px;
    }

    .hero h2 {
        font-size: 32px;
    }

    .hero p {
        font-size: 16px;
    }
}
</style>
/* WhatsApp Button */
.whatsapp-btn {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: #25D366;
    color: white;
    font-size: 24px;
    padding: 15px;
    border-radius: 50%;
    text-decoration: none;
    box-shadow: 0 5px 15px rgba(0,0,0,0.3);
    transition: transform 0.3s;
    z-index: 1000;
}

.whatsapp-btn:hover {
    transform: scale(1.1);
}
</head>

<body>

<header>
    <h1>Cadets Men Fellowship</h1>
    <nav>
        <a href="#">Home</a>
        <a href="#features">Mission</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<section class="hero">
    <div>
        <h2>Building Strong Men of Purpose</h2>
        <p>Empowering men through faith, discipline, and brotherhood.</p>
        <button class="btn">Join Us</button>
    </div>
</section>

<section class="features" id="features">
    <h3>Our Mission</h3>
    <div class="feature-box">
        <div class="card">
            <h4>Brotherhood</h4>
            <p>We stand together as one strong and united family.</p>
        </div>
        <div class="card">
            <h4>Discipline</h4>
            <p>We build character through consistency and commitment.</p>
        </div>
        <div class="card">
            <h4>Faith</h4>
            <p>We grow spiritually and walk in purpose.</p>
        </div>
    </div>
</section>

<footer id="contact">
    <p>© 2026 Cadets Men Fellowship | All Rights Reserved</p>
</footer>

<script>
// SCROLL ANIMATION
const cards = document.querySelectorAll('.card');

window.addEventListener('scroll', () => {
    cards.forEach(card => {
        const cardTop = card.getBoundingClientRect().top;
        if (cardTop < window.innerHeight - 50) {
            card.classList.add('show');
        }
    });
});
</script>
<!-- WhatsApp Button -->
<a href="https://wa.me/254782141192" class="whatsapp-btn" target="_blank">
    💬
</a>
</body>
</html>


</html>
