<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Shivanshi Bakery House — 100% Veg · Fresh · Delicious</title>
<style>
  :root{
    --accent:#d63447;
    --accent-2:#ffb3b3;
    --card-bg:#fff;
    --page-bg:#fff5f5;
    --muted:#6b6b6b;
    --radius:12px;
    font-family: "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
  }
  *{box-sizing:border-box}
  body{margin:0;background:var(--page-bg);color:#222}
  header{
    background: linear-gradient(180deg, rgba(214,52,71,0.95), rgba(255,179,179,0.95));
    color:#fff;padding:22px 16px;text-align:center;
  }
  header h1{margin:0;font-size:1.9rem;display:flex;align-items:center;justify-content:center;gap:10px}
  header p{margin:6px 0 0;font-size:0.95rem;color: #ffecec}
  .container{max-width:1100px;margin:18px auto;padding:0 16px}
  .hero{
    background:#fff;padding:14px;border-radius:var(--radius);box-shadow:0 6px 20px rgba(0,0,0,0.06);
    display:flex;gap:14px;align-items:center;
    margin-bottom:18px;
  }
  .hero img{width:40%;max-width:360px;border-radius:10px;display:block}
  .hero .lead{flex:1}
  .lead h2{margin:0;font-size:1.2rem;color:var(--accent)}
  .lead p{margin:8px 0;color:var(--muted)}
  .btn-wa{
    display:inline-block;margin-top:10px;padding:10px 14px;border-radius:8px;background:#25D366;color:white;text-decoration:none;font-weight:600;
    box-shadow:0 4px 12px rgba(37,211,102,0.2)
  }

  /* Menu grid */
  .section-title{display:flex;align-items:center;gap:10px}
  .section-title h3{margin:0;color:var(--accent)}
  .grid{
    display:grid;
    grid-template-columns: repeat(auto-fit,minmax(220px,1fr));
    gap:16px;margin-top:14px;
  }
  .card{
    background:var(--card-bg);border-radius:12px;overflow:hidden;box-shadow:0 6px 18px rgba(0,0,0,0.06);text-align:center;
    display:flex;flex-direction:column;
  }
  .card img{width:100%;height:160px;object-fit:cover}
  .card .card-body{padding:12px;flex:1;display:flex;flex-direction:column;justify-content:space-between}
  .item-name{font-weight:700;margin:6px 0;font-size:1rem}
  .item-sub{color:var(--muted);font-size:0.9rem;margin-bottom:8px}
  .order-row{display:flex;gap:8px;justify-content:center;margin-top:8px;flex-wrap:wrap}
  .order-btn{
    background:var(--accent);color:#fff;padding:8px 10px;border-radius:8px;text-decoration:none;font-weight:700;
  }
  .veg-badge{background:#e8f9ec;color:#2b7a36;padding:6px 8px;border-radius:999px;font-weight:700;font-size:0.9rem;display:inline-flex;align-items:center;gap:6px}

  label{font-size:0.9rem;margin:2px;}
  select,input{padding:4px;margin-left:4px;border-radius:6px;border:1px solid #ccc;width:70px;text-align:center}

  /* Contact & map */
  .contact{
    margin-top:20px;background:#fff;padding:14px;border-radius:12px;box-shadow:0 6px 18px rgba(0,0,0,0.04);
    display:grid;grid-template-columns:1fr 1fr;gap:12px;align-items:start;
  }
  .contact .info p{margin:6px 0}
  iframe.map{width:100%;height:220px;border-radius:10px;border:0}

  footer{margin-top:18px;padding:16px;text-align:center;color:#fff;background:var(--accent);border-radius:10px;margin-bottom:30px}

  /* Responsive tweaks */
  @media (max-width:720px){
    .hero{flex-direction:column}
    .hero img{width:100%;height:220px;object-fit:cover}
    .contact{grid-template-columns:1fr}
  }
</style>
</head>
<body>

<header>
  <div class="container">
    <h1>Shivanshi Bakery House 🍰 <span style="font-size:0.9rem">🌿</span></h1>
    <p>🌿 <strong>100% Veg</strong> · Freshly Baked · Custom Orders Welcome ✨</p>
  </div>
</header>

<main class="container">
  <!-- HERO -->
  <section class="hero" aria-label="hero">
    <img src="https://images.unsplash.com/photo-1606312617275-70a5a56056eb?auto=format&fit=crop&w=1000&q=80" alt="Delicious cakes on display">
    <div class="lead">
      <h2>Delicious Cakes. Heart-made. Everywhere smiles 🍰</h2>
      <p>Shivanshi Bakery House — Near Infocity Ave., Patia, Bhubaneswar. Fresh cakes, cupcakes, brownies and custom theme cakes for every celebration.</p>
      <a class="btn-wa" href="https://wa.me/917377670807?text=Hi%20Shivanshi%20Bakery%20House!%20I%20would%20like%20to%20place%20an%20order." target="_blank" rel="noopener">📱 Order on WhatsApp</a>
    </div>
  </section>

  <!-- MENU -->
  <section aria-label="menu">
    <div class="section-title">
      <h3>🍰 Our Specialties</h3>
      <div style="margin-left:auto" class="veg-badge">🌿 Full Veg</div>
    </div>

    <div class="grid" id="menu-grid">
      <!-- Cards will be inserted by JS -->
    </div>

    <button id="orderBtn" class="order-btn" style="width:100%;margin-top:12px;">📱 Place Order on WhatsApp</button>
  </section>

  <!-- CONTACT & MAP -->
  <section class="contact" aria-label="contact">
    <div class="info">
      <h3 style="color:var(--accent)">Contact Us 📞</h3>
      <p>Shivanshi Bakery House — Near Infocity Ave., Patia, Bhubaneswar</p>
      <p>Phone / WhatsApp: <strong><a href="tel:+917377670807">+91 73776 70807</a></strong></p>
      <p><a class="btn-wa" href="https://wa.me/917377670807?text=Hi%20Shivanshi%20Bakery%20House!%20I%20want%20to%20place%20an%20order." target="_blank">📱 Order Now on WhatsApp</a></p>
      <p style="color:var(--muted);font-size:0.95rem">Open: 8:00 AM – 9:00 PM (Daily)</p>
    </div>

    <div>
      <iframe class="map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3679.4694383623513!2d85.81958207501707!3d20.32240198114001!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3a19a7b4a90f4d4f%3A0x6a0bb2cb10bbba73!2sInfocity%20Ave%2C%20Patia%2C%20Bhubaneswar%2C%20Odisha!5e0!3m2!1sen!2sin!4v1690198596385!5m2!1sen!2sin" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>
  </section>

</main>

<footer>
  © 2025 Shivanshi Bakery House · Near Infocity Ave., Patia, Bhubaneswar · 🌿 100% Veg
</footer>

<script>
// All 18 items
const items=[
{name:"Chocolate Cake 🍫",desc:"Rich & creamy chocolate layers",priceHalf:400,priceOne:700,img:"https://images.unsplash.com/photo-1542826438-7c2d8f0f3c3a?auto=format&fit=crop&w=1000&q=80"},
{name:"Black Forest Cake 🍒",desc:"Classic chocolate & cherry delight",priceHalf:450,priceOne:800,img:"https://images.unsplash.com/photo-1549092332-0ac27c88fb1d?auto=format&fit=crop&w=1000&q=80"},
{name:"Truffle Cake ✨",desc:"Decadent truffle layers",priceHalf:500,priceOne:900,img:"https://images.unsplash.com/photo-1607082349048-7a7c0fbf6b49?auto=format&fit=crop&w=1000&q=80"},
{name:"Vanilla Cake 🌼",desc:"Light & fragrant vanilla sponge",priceHalf:350,priceOne:650,img:"https://images.unsplash.com/photo-1547592166-9d61790d5b4c?auto=format&fit=crop&w=1000&q=80"},
{name:"Strawberry Cake 🍓",desc:"Fresh strawberry topping",priceHalf:400,priceOne:750,img:"https://images.unsplash.com/photo-1527515637463-85f8fe31de02?auto=format&fit=crop&w=1000&q=80"},
{name:"Pineapple Cake 🍍",desc:"Tropical & juicy",priceHalf:400,priceOne:750,img:"https://images.unsplash.com/photo-1562440499-64a6b1ea7e5b?auto=format&fit=crop&w=1000&q=80"},
{name:"Rasamalai Cake 🧁",desc:"Indian sweet fusion cake",priceHalf:450,priceOne:850,img:"https://images.unsplash.com/photo-1615285144790-1a6bfc29a3c0?auto=format&fit=crop&w=1000&q=80"},
{name:"Cartoon Theme Cake 🧸",desc:"Custom character cakes for kids",priceHalf:600,priceOne:1200,img:"https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&w=1000&q=80"},
{name:"Floral Theme Cake 🌸",desc:"Elegant floral decorations",priceHalf:550,priceOne:1100,img:"https://images.unsplash.com/photo-1528825871115-3581a5387919?auto=format&fit=crop&w=1000&q=80"},
{name:"Fondant Cake 🎂",desc:"Smooth fondant finish & custom art",priceHalf:700,priceOne:1300,img:"https://images.unsplash.com/photo-1562007907-46743b3f8e28?auto=format&fit=crop&w=1000&q=80"},
{name:"Chocolate Brownies 🍫",desc:"Fudgy & gooey",priceHalf:50,priceOne:100,img:"https://images.unsplash.com/photo-1598379308875-2c3c6cc5a8d8?auto=format&fit=crop&w=1000&q=80"},
{name:"Nuts Brownie 🌰",desc:"Crunchy nuts & chocolate",priceHalf:60,priceOne:120,img:"https://images.unsplash.com/photo-1611665560912-cc57f3f2f0a8?auto=format&fit=crop&w=1000&q=80"},
{name:"Choco Lava Cake 🔥",desc:"Warm molten centre",priceHalf:80,priceOne:150,img:"https://images.unsplash.com/photo-1606756791748-d3b6d9e7e8b8?auto=format&fit=crop&w=1000&q=80"},
{name:"Chocolate Dry Fruits Cake 🥜",desc:"Luxury dry fruits & chocolate",priceHalf:450,priceOne:900,img:"https://images.unsplash.com/photo-1562440499-64a6b1ea7e5b?auto=format&fit=crop&w=1000&q=80"},
{name:"Banana Cake 🍌",desc:"Soft banana sponge",priceHalf:350,priceOne:650,img:"https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&w=1000&q=80"},
{name:"Chocolate Cupcakes 🧁",desc:"Perfect party cupcakes",priceHalf:50,priceOne:100,img:"https://images.unsplash.com/photo-1542345812-d98b5cd6cf98?auto=format&w=1000&q=80"},
{name:"Customize Cake 🎨",desc:"Tell us your theme & we create",priceHalf:700,priceOne:1500,img:"https://images.unsplash.com/photo-1527515637463-85f8fe31de02?auto=format&fit=crop&w=1000&q=80"},
{name:"Vanilla Cupcakes 🧁",desc:"Classic vanilla frosting",priceHalf:50,priceOne:100,img:"https://images.unsplash.com/photo-1499636136210-6f4ee915583e?auto=format&fit=crop&w=1000&q=80"}
];

const menuGrid=document.getElementById("menu-grid");

items.forEach((item,index)=>{
  const card=document.createElement("div");
  card.className="card";
  card.innerHTML=`
    <img src="${item.img}" alt="${item.name}">
    <div class="card-body">
      <div>
        <div class="item-name">${item.name}</div>
        <div class="item-sub">${item.desc}</div>
        <label>Size:
          <select id="size-${index}">
            <option value="0.5">1/2 kg - ₹${item.priceHalf}</option>
            <option value="1">1 kg - ₹${item.priceOne}</option>
          </select>
        </label>
        <label>Qty:
          <input type="number" id="qty-${index}" value="0" min="0">
        </label>
      </div>
    </div>
  `;
  menuGrid.appendChild(card);
});

document.getElementById("orderBtn").addEventListener("click",()=>{
  let msg="Hi Shivanshi Bakery House! I want to order:\n";
  let total=0;
  items.forEach((item,index)=>{
    const qty=parseInt(document.getElementById(`qty-${index}`)?.value || 0);
    if(qty>0){
      const size=parseFloat(document.getElementById(`size-${index}`)?.value || 0.5);
      const price=(size===0.5)?item.priceHalf:item.priceOne;
      const subtotal=qty*price;
      msg+=`${item.name} - ${size===0.5?"1/2 kg":"1 kg"} x ${qty} = ₹${subtotal}\n`;
      total+=subtotal;
    }
  });
  msg+="------------------------\n";
  msg+=`Total: ₹${total}`;
  if(total>0){
    const waLink="https://wa.me/917377670807?text="+encodeURIComponent(msg);
    window.open(waLink,"_blank");
  }else{
    alert("Please select quantity for at least one item.");
  }
});
</script>

</body>
</html># Shivanshi-bakery-house
Odisha fresh bakery 
