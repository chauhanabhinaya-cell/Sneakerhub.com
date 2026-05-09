# Sneakerhub.com
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Premium Shoes Store</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
}

body{
    background:#0a0a0a;
    color:white;
    overflow-x:hidden;
}

/* NAVBAR */

nav{
    width:100%;
    height:80px;
    position:fixed;
    top:0;
    left:0;
    background:rgba(0,0,0,0.6);
    backdrop-filter:blur(10px);
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:0 50px;
    z-index:1000;
}

.logo{
    font-size:32px;
    font-weight:700;
    letter-spacing:2px;
    color:#fff;
}

.logo span{
    color:#ff4d4d;
}

nav ul{
    display:flex;
    gap:30px;
    list-style:none;
}

nav ul li{
    cursor:pointer;
    transition:0.3s;
}

nav ul li:hover{
    color:#ff4d4d;
}

/* HERO SECTION */

.hero{
    width:100%;
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    padding:120px 80px 50px;
    position:relative;
    overflow:hidden;
}

.hero-left{
    width:50%;
    z-index:10;
}

.hero-left h1{
    font-size:80px;
    line-height:1;
    margin-bottom:20px;
}

.hero-left h1 span{
    color:#ff4d4d;
}

.hero-left p{
    color:#bbb;
    line-height:1.7;
    margin-bottom:30px;
    width:80%;
}

.hero-btns{
    display:flex;
    gap:20px;
}

.btn{
    padding:15px 30px;
    border:none;
    border-radius:50px;
    font-size:16px;
    cursor:pointer;
    transition:0.3s;
}

.btn-primary{
    background:#ff4d4d;
    color:white;
}

.btn-primary:hover{
    transform:translateY(-5px);
}

.btn-secondary{
    background:transparent;
    border:2px solid white;
    color:white;
}

.btn-secondary:hover{
    background:white;
    color:black;
}

/* FLOATING SHOES */

.hero-right{
    width:50%;
    position:relative;
    height:700px;
}

.shoe{
    position:absolute;
    width:260px;
    animation:float 4s ease-in-out infinite;
    filter:drop-shadow(0 20px 30px rgba(255,77,77,0.4));
}

.shoe1{
    top:40px;
    left:120px;
}

.shoe2{
    top:260px;
    right:50px;
    animation-delay:1s;
}

.shoe3{
    bottom:20px;
    left:60px;
    animation-delay:2s;
}

@keyframes float{
    0%{
        transform:translateY(0px) rotate(-5deg);
    }
    50%{
        transform:translateY(-25px) rotate(5deg);
    }
    100%{
        transform:translateY(0px) rotate(-5deg);
    }
}

/* CATEGORY */

.section-title{
    text-align:center;
    font-size:50px;
    margin-bottom:60px;
}

.section-title span{
    color:#ff4d4d;
}

.categories{
    padding:100px 60px;
}

.category-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:30px;
}

.card{
    background:#111;
    border-radius:25px;
    padding:30px;
    transition:0.4s;
    border:1px solid rgba(255,255,255,0.08);
}

.card:hover{
    transform:translateY(-10px);
    box-shadow:0 0 30px rgba(255,77,77,0.3);
}

.card img{
    width:100%;
    height:200px;
    object-fit:contain;
}

.card h3{
    margin-top:20px;
    font-size:24px;
}

.card p{
    color:#bbb;
    margin:10px 0;
    line-height:1.6;
}

.price{
    color:#ff4d4d;
    font-size:24px;
    font-weight:600;
    margin-bottom:15px;
}

.buy-btn{
    width:100%;
    padding:12px;
    border:none;
    border-radius:12px;
    background:#ff4d4d;
    color:white;
    font-size:16px;
    cursor:pointer;
    transition:0.3s;
}

.buy-btn:hover{
    background:#ff2222;
}

/* FILTER SECTION */

.filters{
    padding:80px 60px;
}

.filter-box{
    background:#111;
    padding:40px;
    border-radius:25px;
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:20px;
}

.filter-box select,
.filter-box input{
    padding:15px;
    border:none;
    border-radius:12px;
    background:#1c1c1c;
    color:white;
    font-size:16px;
}

.filter-box button{
    padding:15px;
    border:none;
    border-radius:12px;
    background:#ff4d4d;
    color:white;
    font-size:16px;
    cursor:pointer;
}

/* AVAILABILITY */

.availability{
    padding:100px 60px;
}

.availability-box{
    background:linear-gradient(135deg,#111,#1f1f1f);
    border-radius:30px;
    padding:50px;
    text-align:center;
}

.availability-box h2{
    font-size:40px;
    margin-bottom:20px;
}

.availability-box input{
    width:70%;
    padding:18px;
    border:none;
    border-radius:50px;
    background:#222;
    color:white;
    margin-top:20px;
    font-size:16px;
}

.availability-box button{
    margin-top:20px;
    padding:15px 40px;
    border:none;
    border-radius:50px;
    background:#ff4d4d;
    color:white;
    cursor:pointer;
    font-size:18px;
}

/* FOOTER */

footer{
    margin-top:100px;
    padding:40px;
    text-align:center;
    background:#050505;
    color:#888;
}

/* RESPONSIVE */

@media(max-width:1000px){

    .hero{
        flex-direction:column;
    }

    .hero-left{
        width:100%;
        text-align:center;
    }

    .hero-left p{
        width:100%;
    }

    .hero-right{
        width:100%;
        margin-top:50px;
        height:600px;
    }

    .hero-left h1{
        font-size:55px;
    }

    nav{
        padding:0 20px;
    }

}

</style>
</head>

<body>

<!-- NAVBAR -->

<nav>
    <div class="logo">SHOE<span>X</span></div>

    <ul>
        <li>Home</li>
        <li>Categories</li>
        <li>Brands</li>
        <li>Pricing</li>
        <li>Availability</li>
    </ul>
</nav>

<!-- HERO -->

<section class="hero">

    <div class="hero-left">
        <h1>PREMIUM <span>SHOES</span> COLLECTION</h1>

        <p>
            Discover premium sneakers, running shoes, streetwear shoes and luxury collections with futuristic design and ultra comfort.
        </p>

        <div class="hero-btns">
            <button class="btn btn-primary">Explore Now</button>
            <button class="btn btn-secondary">View Collection</button>
        </div>
    </div>

    <div class="hero-right">

        <img class="shoe shoe1"
        src="https://pngimg.com/d/running_shoes_PNG5816.png">

        <img class="shoe shoe2"
        src="https://pngimg.com/d/running_shoes_PNG5817.png">

        <img class="shoe shoe3"
        src="https://pngimg.com/d/running_shoes_PNG5823.png">

    </div>

</section>

<!-- FILTERS -->

<section class="filters">

    <h2 class="section-title">Find Your <span>Shoes</span></h2>

    <div class="filter-box">

        <select>
            <option>Select Brand</option>
            <option>Nike</option>
            <option>Adidas</option>
            <option>Puma</option>
            <option>Jordan</option>
        </select>

        <select>
            <option>Select Category</option>
            <option>Running</option>
            <option>Sneakers</option>
            <option>Sports</option>
            <option>Casual</option>
        </select>

        <select>
            <option>Price Range</option>
            <option>₹1000 - ₹3000</option>
            <option>₹3000 - ₹7000</option>
            <option>₹7000+</option>
        </select>

        <button>Search</button>

    </div>

</section>

<!-- CATEGORIES -->

<section class="categories">

    <h2 class="section-title">Trending <span>Collections</span></h2>

    <div class="category-grid">

        <div class="card">

            <img src="https://pngimg.com/d/running_shoes_PNG5816.png">

            <h3>Nike Air Max</h3>

            <p>
                Lightweight premium running sneakers with air cushioning and modern design.
            </p>

            <div class="price">₹6,999</div>

            <button class="buy-btn">View Details</button>

        </div>

        <div class="card">

            <img src="https://pngimg.com/d/running_shoes_PNG5823.png">

            <h3>Adidas Ultraboost</h3>

            <p>
                High performance sports shoes built for comfort and speed.
            </p>

            <div class="price">₹8,499</div>

            <button class="buy-btn">View Details</button>

        </div>

        <div class="card">

            <img src="https://pngimg.com/d/running_shoes_PNG5817.png">

            <h3>Puma Street X</h3>

            <p>
                Stylish streetwear sneakers with futuristic aesthetic and premium feel.
            </p>

            <div class="price">₹5,499</div>

            <button class="buy-btn">View Details</button>

        </div>

    </div>

</section>

<!-- AVAILABILITY -->

<section class="availability">

    <div class="availability-box">

        <h2>Check Availability Near You</h2>

        <p>
            Enter your address or city to check delivery and product availability.
        </p>

        <input type="text" placeholder="Enter Address / City">

        <br>

        <button onclick="checkAvailability()">
            Check Now
        </button>

    </div>

</section>

<!-- FOOTER -->

<footer>
    © 2026 SHOEX Premium Shoes Website | Designed with Luxury UI
</footer>

<script>

function checkAvailability(){

    alert("Shoes are available in your area ✅");

}

</script>

</body>
</html>
