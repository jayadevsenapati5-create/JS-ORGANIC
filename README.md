<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>JS ORGANIC</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial, sans-serif;
}

body{
background:#f8f8f8;
color:#333;
}

/* HERO */

.hero{
height:100vh;
background:url("https://i.ibb.co/27ymGjnm/HALDI.jpg") center/cover no-repeat;
display:flex;
align-items:center;
justify-content:center;
text-align:center;
color:white;
padding:20px;
}

.hero-content{
background:rgba(0,0,0,0.4);
padding:30px;
border-radius:10px;
}

.hero h1{
font-size:42px;
margin-bottom:10px;
}

.hero p{
font-size:18px;
margin-bottom:20px;
}

.btn{
background:#ff9800;
color:white;
padding:12px 25px;
border:none;
border-radius:5px;
font-size:16px;
cursor:pointer;
text-decoration:none;
}

/* PRODUCTS */

.products{
padding:40px 20px;
}

.products h2{
text-align:center;
margin-bottom:20px;
}

.carousel{
display:flex;
overflow-x:auto;
gap:20px;
padding-bottom:10px;
}

.card{
min-width:220px;
background:white;
border-radius:10px;
box-shadow:0 2px 8px rgba(0,0,0,0.1);
padding:15px;
text-align:center;
}

.card img{
width:100%;
border-radius:10px;
}

.card h3{
margin:10px 0;
}

.price{
color:#2e7d32;
font-weight:bold;
margin-bottom:10px;
}

.add-btn{
background:#4caf50;
color:white;
border:none;
padding:10px 15px;
border-radius:5px;
cursor:pointer;
}

/* CART FORM */

.order{
padding:40px 20px;
background:white;
}

.order h2{
text-align:center;
margin-bottom:20px;
}

form{
max-width:400px;
margin:auto;
display:flex;
flex-direction:column;
gap:10px;
}

input,textarea{
padding:10px;
border:1px solid #ccc;
border-radius:5px;
}

.submit-btn{
background:#ff9800;
border:none;
color:white;
padding:12px;
border-radius:5px;
font-size:16px;
cursor:pointer;
}

/* WHATSAPP */

.whatsapp{
position:fixed;
bottom:20px;
right:20px;
background:#25d366;
color:white;
width:60px;
height:60px;
border-radius:50%;
display:flex;
align-items:center;
justify-content:center;
font-size:28px;
text-decoration:none;
box-shadow:0 4px 10px rgba(0,0,0,0.3);
}

</style>
</head>

<body>

<!-- HERO -->

<section class="hero">

<div class="hero-content">

<h1>JS ORGANIC</h1>

<p>100% organic free chemical turmeric powder, no food colour add</p>

<a href="#products" class="btn">SHOP NOW</a>

</div>

</section>


<!-- PRODUCTS -->

<section class="products" id="products">

<h2>Our Products</h2>

<div class="carousel">

<div class="card">

<img src="https://i.ibb.co/27ymGjnm/HALDI.jpg">

<h3>Organic Turmeric Powder</h3>

<p class="price">₹200</p>

<button class="add-btn" onclick="addToCart('Organic Turmeric Powder - ₹200')">Add to Cart</button>

</div>


<div class="card">

<img src="https://i.ibb.co/27ymGjnm/HALDI.jpg">

<h3>Premium Turmeric Powder</h3>

<p class="price">₹350</p>

<button class="add-btn" onclick="addToCart('Premium Turmeric Powder - ₹350')">Add to Cart</button>

</div>


<div class="card">

<img src="https://i.ibb.co/27ymGjnm/HALDI.jpg">

<h3>Village Haldi Powder</h3>

<p class="price">₹500</p>

<button class="add-btn" onclick="addToCart('Village Haldi Powder - ₹500')">Add to Cart</button>

</div>

</div>

</section>



<!-- ORDER FORM -->

<section class="order">

<h2>Place Your Order</h2>

<form onsubmit="sendOrder(event)">

<input type="text" id="name" placeholder="Your Name" required>

<input type="tel" id="phone" placeholder="Phone Number" required>

<textarea id="cartItems" placeholder="Selected Items" readonly></textarea>

<button class="submit-btn">Place Order</button>

</form>

</section>


<!-- WHATSAPP BUTTON -->

<a href="https://wa.me/8908654900" class="whatsapp">💬</a>


<script>

let cart=[];

function addToCart(item){

cart.push(item);

document.getElementById("cartItems").value=cart.join("\n");

alert("Item added to cart");

}


function sendOrder(e){

e.preventDefault();

let name=document.getElementById("name").value;
let phone=document.getElementById("phone").value;
let items=cart.join(", ");

let body=
"Customer Name: "+name+
"%0D%0APhone: "+phone+
"%0D%0AItems: "+items;

window.location.href=
"mailto:jayadevsenapati5@gmail.com?subject=New Order from JS ORGANIC&body="+body;

}

</script>

</body>
</html>
