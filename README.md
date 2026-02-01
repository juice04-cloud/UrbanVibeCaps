# UrbanVibeCaps
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Urban Vibe Caps</title>
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:Arial,sans-serif;}
body{background:#f5f5f5;}
header{background:#000;color:#fff;padding:20px;text-align:center;font-size:28px;font-weight:bold;}
nav{background:#222;display:flex;justify-content:center;gap:20px;padding:10px;position:sticky;top:0;z-index:1000;}
nav a{color:#fff;text-decoration:none;font-weight:bold;}
nav a:hover{color:#ff004f;}
.hero{background:url('hero.jpg') no-repeat center/cover;height:250px;display:flex;align-items:center;justify-content:center;color:#fff;font-size:28px;font-weight:bold;text-shadow:2px 2px 5px #000;text-align:center;}
section{margin:30px 15px;text-align:center;}
section h2{margin-bottom:15px;font-size:24px;color:#000;}
section p{font-size:16px;color:#555;}
#countdown{font-size:18px;font-weight:bold;margin-bottom:20px;color:#ff004f;}
.products-container{display:flex;overflow-x:auto;gap:15px;padding-bottom:20px;scroll-snap-type:x mandatory;}
.product{min-width:220px;background:#fff;border-radius:10px;padding:15px;text-align:center;box-shadow:0 2px 5px rgba(0,0,0,0.2);scroll-snap-align:start;position:relative;transition:transform 0.3s;}
.product:hover{transform:scale(1.05);}
.product-images{position:relative;overflow:hidden;border-radius:10px;cursor:pointer;}
.product-images img{width:100%;display:block;transition: transform 0.3s;}
.product-images img.active{display:block;}
.product-images img:not(.active){display:none;}
.arrow{position:absolute;top:50%;transform:translateY(-50%);background:rgba(0,0,0,0.5);color:#fff;width:25px;height:25px;text-align:center;line-height:25px;font-weight:bold;border-radius:50%;cursor:pointer;user-select:none;}
.arrow-left{left:5px;}
.arrow-right{right:5px;}
.product h3{margin:10px 0 5px;font-size:18px;}
.product p{margin:5px 0;font-size:14px;color:#333;}
.product .badge{position:absolute;top:10px;left:10px;background:#ff004f;color:#fff;padding:3px 8px;font-size:12px;border-radius:5px;font-weight:bold;animation: blink 1s infinite;}
@keyframes blink{0%,50%,100%{opacity:1;}25%,75%{opacity:0.5;}}
.color-options{display:flex;justify-content:center;gap:5px;margin-bottom:10px;}
.color-options div{width:25px;height:25px;border-radius:50%;border:2px solid #ccc;cursor:pointer;transition: transform 0.2s;}
.color-options div.selected{border:2px solid #ff004f;transform:scale(1.2);}
select{width:100%;padding:8px;margin:5px 0 10px;border-radius:5px;border:1px solid #ccc;}
button{background:#ff004f;color:#fff;border:none;padding:10px;border-radius:5px;cursor:pointer;font-weight:bold;width:100%;transition: all 0.3s;}
button:hover{background:#e60045;transform: scale(1.05);}
#cart{position:fixed;top:70px;right:10px;background:#fff;border:1px solid #ccc;padding:15px;border-radius:10px;width:220px;box-shadow:0 2px 8px rgba(0,0,0,0.3);max-height:400px;overflow-y:auto;z-index:100;}
#cart h3{margin-bottom:10px;text-align:center;}
.cart-item{display:flex;justify-content:space-between;margin-bottom:10px;font-size:14px;}
.cart-total{font-weight:bold;text-align:center;margin-top:10px;}
#checkout{background:#ff004f;color:#fff;border:none;padding:10px;border-radius:5px;cursor:pointer;width:100%;font-weight:bold;margin-top:10px;}
#checkout:hover{background:#e60045;}
footer{background:#222;color:#fff;text-align:center;padding:20px;margin-top:20px;font-size:14px;}
#zoomModal{display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.9);justify-content:center;align-items:center;z-index:999;}
#zoomModal img{max-width:90%;max-height:90%;border-radius:10px;}
#zoomModal span{position:absolute;top:20px;right:20px;color:#fff;font-size:30px;cursor:pointer;font-weight:bold;}
</style>
</head>
<body>

<header>Urban Vibe Caps</header>

<nav>
<a href="#products-section">Shop</a>
<a href="#about">About</a>
<a href="#contact">Contact</a>
</nav>

<div class="hero">Limited Drops: Fitted Caps & Beanies</div>

<section id="products-section">
<div id="countdown">Next Drop in: 02:00:00</div>
<div class="products-container">

<!-- 5 Fitted Caps -->
<div class="product" data-name="Fitted Cap 1" data-price="220">
<div class="badge">Limited</div>
<div class="product-images"><img src="fitted-cap1.jpg" class="active"></div>
<h3>Fitted Cap 1</h3>
<p>R220</p>
<select><option>6 7/8</option><option>7</option><option>7 1/4</option><option>7 1/2</option></select>
<div class="color-options"><div style="background:black;" class="selected"></div><div style="background:red;"></div><div style="background:blue;"></div></div>
<button onclick="addToCart(this)">Add to Cart</button>
</div>

<div class="product" data-name="Fitted Cap 2" data-price="220">
<div class="badge">Limited</div>
<div class="product-images"><img src="fitted-cap2.jpg" class="active"></div>
<h3>Fitted Cap 2</h3>
<p>R220</p>
<select><option>6 7/8</option><option>7</option><option>7 1/4</option><option>7 1/2</option></select>
<div class="color-options"><div style="background:black;" class="selected"></div><div style="background:red;"></div><div style="background:blue;"></div></div>
<button onclick="addToCart(this)">Add to Cart</button>
</div>

<div class="product" data-name="Fitted Cap 3" data-price="220">
<div class="badge">Limited</div>
<div class="product-images"><img src="fitted-cap3.jpg" class="active"></div>
<h3>Fitted Cap 3</h3>
<p>R220</p>
<select><option>6 7/8</option><option>7</option><option>7 1/4</option><option>7 1/2</option></select>
<div class="color-options"><div style="background:black;" class="selected"></div><div style="background:red;"></div><div style="background:blue;"></div></div>
<button onclick="addToCart(this)">Add to Cart</button>
</div>

<div class="product" data-name="Fitted Cap 4" data-price="220">
<div class="badge">Limited</div>
<div class="product-images"><img src="fitted-cap4.jpg" class="active"></div>
<h3>Fitted Cap 4</h3>
<p>R220</p>
<select><option>6 7/8</option><option>7</option><option>7 1/4</option><option>7 1/2</option></select>
<div class="color-options"><div style="background:black;" class="selected"></div><div style="background:red;"></div><div style="background:blue;"></div></div>
<button onclick="addToCart(this)">Add to Cart</button>
</div>

<div class="product" data-name="Fitted Cap 5" data-price="220">
<div class="badge">Limited</div>
<div class="product-images"><img src="fitted-cap5.jpg" class="active"></div>
<h3>Fitted Cap 5</h3>
<p>R220</p>
<select><option>6 7/8</option><option>7</option><option>7 1/4</option><option>7 1/2</option></select>
<div class="color-options"><div style="background:black;" class="selected"></div><div style="background:red;"></div><div style="background:blue;"></div></div>
<button onclick="addToCart(this)">Add to Cart</button>
</div>

<!-- 5 Beanies -->
<div class="product" data-name="Beanie 1" data-price="180">
<div class="badge">Limited</div>
<div class="product-images"><img src="beanie1.jpg" class="active"></div>
<h3>Beanie 1</h3>
<p>R180</p>
<div class="color-options"><div style="background:black;" class="selected"></div><div style="background:white;"></div><div style="background:grey;"></div></div>
<button onclick="addToCart(this)">Add to Cart</button>
</div>

<div class="product" data-name="Beanie 2" data-price="180">
<div class="badge">Limited</div>
<div class="product-images"><img src="beanie2.jpg" class="active"></div>
<h3>Beanie 2</h3>
<p>R180</p>
<div class="color-options"><div style="background:black;" class="selected"></div><div style="background:white;"></div><div style="background:grey;"></div></div>
<button onclick="addToCart(this)">Add to Cart</button>
</div>

<div class="product" data-name="Beanie 3" data-price="180">
<div class="badge">Limited</div>
<div class="product-images"><img src="beanie3.jpg" class="active"></div>
<h3>Beanie 3</h3>
<p>R180</p>
<div class="color-options"><div style="background:black;" class="selected"></div><div style="background:white;"></div><div style="background:grey;"></div></div>
<button onclick="addToCart(this)">Add to Cart</button>
</div>

<div class="product" data-name="Beanie 4" data-price="180">
<div class="badge">Limited</div>
<div class="product-images"><img src="beanie4.jpg" class="active"></div>
<h3>Beanie 4</h3>
<p>R180</p>
<div class="color-options"><div style="background:black;" class="selected"></div><div style="background:white;"></div><div style="background:grey;"></div></div>
<button onclick="addToCart(this)">Add to Cart</button>
</div>

<div class="product" data-name="Beanie 5" data-price="180">
<div class="badge">Limited</div>
<div class="product-images"><img src="beanie5.jpg" class="active"></div>
<h3>Beanie 5</h3>
<p>R180</p>
<div class="color-options"><div style="background:black;" class="selected"></div><div style="background:white;"></div><div style="background:grey;"></div></div>
<button onclick="addToCart(this)">Add to Cart</button>
</div>

</div>
</section>

<div id="cart">
<h3>Cart</h3>
<div id="cart-items"></div>
<div class="cart-total">Total: R<span id="cart-total">0</span></div>
<button id="checkout" onclick="checkout()">Checkout</button>
</div>

<div id="zoomModal" onclick="closeZoom()"><span onclick="closeZoom()">&times;</span><img id="zoomImg" src=""></div>

<section id="about"><h2>About Urban Vibe Caps</h2>
<p>Trendy fitted caps and beanies for teens. Pay first, then we ship directly to your door. Limited drops weekly — don’t miss out!</p>
</section>

<section id="contact"><h2>Contact Us</h2>
<p>WhatsApp: <a href="https://wa.me/your_number" target="_blank">Chat Now</a></p>
</section>

<footer>&copy; 2026 Urban Vibe Caps. All Rights Reserved.</footer>

<script>
// JavaScript functions remain unchanged
let cart=[];
function addToCart(button){const product=button.parentElement;const name=product.dataset.name;const price=Number(product.dataset.price);const colorDiv=product.querySelector('.color-options .selected');const color=colorDiv?colorDiv.style.background:"";const sizeSelect=product.querySelector('select');const size=sizeSelect?sizeSelect.value:"";let option=color+(size?` / ${size}`:"");button.style.transform='scale(1.2)';setTimeout(()=>button.style.transform='scale(1)',300);cart.push({name,price,option});renderCart();}
function renderCart(){const cartItems=document.getElementById('cart-items');cartItems.innerHTML='';let total=0;cart.forEach((item,index)=>{total+=item.price;const div=document.createElement('div');div.className='cart-item';div.innerHTML=`${item.name} (${item.option}) - R${item.price} <button onclick="removeItem(${index})">X</button>`;cartItems.appendChild(div);});document.getElementById('cart-total').innerText=total;}
function removeItem(index){cart.splice(index,1);renderCart();}
function checkout(){if(cart.length===0){alert('Your cart is empty!');return;}let message="Hello! I want to order:\\n";cart.forEach(item=>{message+=`${item.name} (${item.option}) - R${item.price}\\n`;});message+=`Total: R${cart.reduce((a,b)=>a+b.price,0)}\\nPlease let me know how to pay.`;window.location.href="https://wa.me/your_number?text="+encodeURIComponent(message);}
let dropTime=new Date().getTime()+2*60*60*1000;function updateCountdown(){let now=new Date().getTime();let distance=dropTime-now;if(distance<0){document.getElementById('countdown').innerText="Drop is live!";return;}let h=Math.floor(distance/(1000*60*60));let m=Math.floor((distance%(1000*60*60))/(1000*60));let s=Math.floor((distance%(1000*60))/1000);document.getElementById('countdown').innerText=`Next Drop in: ${String(h).padStart(2,'0')}:${String(m).padStart(2,'0')}:${String(s).padStart(2,'0')}`;}setInterval(updateCountdown,1000);
function selectColor(el){const parent=el.parentElement;parent.querySelectorAll('div').forEach(d=>d.classList.remove('selected'));el.classList.add('selected');}
function zoomImage(img){document.getElementById('zoomImg').src=img.src;document.getElementById('zoomModal').style.display='flex';}
function closeZoom(){document.getElementById('zoomModal').style.display='none';}
</script>

</body>
</html>
