<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">
<meta name="theme-color" content="#101827">
<title>Giga Earn BD</title>

<script src="https://telegram.org/js/telegram-web-app.js"></script>
<script src="https://ad.gigapub.tech/script?id=8982"></script>

<style>
*{box-sizing:border-box;margin:0;padding:0}
body{background:#0b1220;color:white;font-family:Arial,sans-serif}
button,input,select{font:inherit}
.app{max-width:480px;margin:auto;padding:18px 16px 100px}
.header{display:flex;justify-content:space-between;align-items:center;margin-bottom:22px}
.logo{font-size:21px;font-weight:900;color:#43dfa0}
.user{background:#1c2b40;padding:10px 13px;border-radius:25px;font-size:13px}
.page{display:none}
.page.active{display:block}
.card{background:#19283d;border:1px solid #2d4059;border-radius:17px;padding:19px;margin-bottom:16px}
.muted{font-size:13px;color:#9eafc5;line-height:1.7}
.title{font-size:19px;margin-bottom:13px}
.balance-card{background:linear-gradient(130deg,#087e60,#064c48);border:0}
.balance{font-size:37px;font-weight:900;margin:12px 0}
.balance-label{font-size:13px;color:#d5fff0}
.stats{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:20px}
.stat{background:#19283d;border:1px solid #2d4059;border-radius:15px;padding:16px}
.stat-icon{font-size:25px}
.stat-label{font-size:12px;color:#9eafc5;margin:8px 0}
.stat-value{font-size:21px;font-weight:bold}
.heading{font-size:17px;margin:22px 0 13px}
.ad-card{text-align:center;padding:25px 17px}
.ad-icon{font-size:48px;margin-bottom:13px}
.main-btn{width:100%;border:0;border-radius:12px;padding:15px;background:#35dc98;color:#062b1d;font-weight:bold;margin-top:16px}
.main-btn:disabled{opacity:.5}
.secondary-btn{width:100%;padding:13px;border:0;border-radius:11px;background:#30445e;color:white;margin-top:11px}
.status{font-size:12px;color:#aabbd0;line-height:1.6;margin-top:13px}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.menu-item{background:#19283d;border:1px solid #2d4059;border-radius:15px;padding:19px 8px;text-align:center;cursor:pointer}
.menu-icon{font-size:28px;margin-bottom:9px}
.menu-item p{font-size:12px;color:#9eafc5;margin-top:6px}
.section-title{font-size:20px;margin:10px 0 17px}
.row{display:flex;justify-content:space-between;align-items:center;gap:10px;padding:14px 0;border-bottom:1px solid #304157;font-size:13px}
.row:last-child{border:0}
.input{width:100%;padding:14px;border-radius:10px;border:1px solid #30445e;background:#0d192a;color:white;margin-top:12px}
.ref-link{background:#0d192a;padding:13px;border-radius:10px;font-size:12px;word-break:break-all;margin-top:14px}
.empty{text-align:center;padding:22px;color:#9eafc5;font-size:13px}
.nav{position:fixed;bottom:0;left:0;right:0;max-width:480px;margin:auto;display:flex;justify-content:space-around;background:#17253a;border-top:1px solid #30445e;padding:12px 4px calc(12px + env(safe-area-inset-bottom));z-index:10}
.nav button{border:0;background:none;color:#91a3ba;display:flex;flex-direction:column;align-items:center;gap:5px;font-size:11px;min-width:60px}
.nav button.active{color:#43dfa0}
.nav-icon{font-size:21px}
.footer{text-align:center;color:#71839c;font-size:11px;padding:20px}
</style>
</head>

<body>
<div class="app">

<header class="header">
 <div class="logo">⚡ GIGA EARN BD</div>
 <div class="user">👤 <span id="username">Guest</span></div>
</header>

<!-- HOME -->
<section id="home" class="page active">

 <div class="card">
  <h2 id="welcome">Welcome Back! 👋</h2>
  <p class="muted">Giga Earn BD-তে আপনাকে স্বাগতম।</p>
 </div>

 <div class="card balance-card">
  <p class="balance-label">💰 TOTAL BALANCE</p>
  <div class="balance">৳ <span id="balance">0.00</span></div>
  <p class="balance-label">Available Balance</p>
 </div>

 <div class="stats">
  <div class="stat">
   <div class="stat-icon">🎬</div>
   <p class="stat-label">Ads Watched</p>
   <div class="stat-value" id="adsCount">0</div>
  </div>
  <div class="stat">
   <div class="stat-icon">👥</div>
   <p class="stat-label">Referrals</p>
   <div class="stat-value" id="refCount">0</div>
  </div>
 </div>

 <h3 class="heading">🎯 Watch & Earn</h3>

 <div class="card ad-card">
  <div class="ad-icon">📺</div>
  <h3>Watch Advertisement</h3>
  <p class="muted">বিজ্ঞাপন দেখুন এবং রিওয়ার্ড সংগ্রহ করুন।</p>
  <button class="main-btn" id="watchBtn">▶ WATCH ADS</button>
  <p class="status" id="adStatus">Ready to watch ads.</p>
 </div>

 <h3 class="heading">📱 Quick Menu</h3>

 <div class="grid">
  <div class="menu-item" onclick="showPage('wallet')">
   <div class="menu-icon">💰</div>
   <b>My Wallet</b>
   <p>আমার ব্যালেন্স</p>
  </div>
  <div class="menu-item" onclick="showPage('refer')">
   <div class="menu-icon">👥</div>
   <b>Referral</b>
   <p>বন্ধু আমন্ত্রণ</p>
  </div>
  <div class="menu-item" onclick="showPage('history')">
   <div class="menu-icon">📜</div>
   <b>History</b>
   <p>লেনদেনের ইতিহাস</p>
  </div>
  <div class="menu-item" onclick="showPage('profile')">
   <div class="menu-icon">👤</div>
   <b>Profile</b>
   <p>আমার অ্যাকাউন্ট</p>
  </div>
 </div>
</section>

<!-- WALLET -->
<section id="wallet" class="page">
 <h2 class="section-title">💰 My Wallet</h2>

 <div class="card balance-card">
  <p class="balance-label">Available Balance</p>
  <div class="balance">৳ <span id="walletBalance">0.00</span></div>
 </div>

 <div class="card">
  <h3>💳 Withdraw Request</h3>
  <p class="muted">উত্তোলনের জন্য আবেদন করুন।</p>

  <input class="input" type="number" id="amount" placeholder="Enter Amount">
  <select class="input" id="method">
   <option value="bKash">bKash</option>
   <option value="Nagad">Nagad</option>
   <option value="Rocket">Rocket</option>
  </select>
  <input class="input" type="tel" id="number" placeholder="Payment Number">

  <button class="main-btn" onclick="withdraw()">SUBMIT REQUEST</button>
  <p class="status" id="withdrawStatus">Withdrawal backend is not connected.</p>
 </div>
</section>

<!-- REFERRAL -->
<section id="refer" class="page">
 <h2 class="section-title">👥 Referral Program</h2>

 <div class="card">
  <div style="text-align:center;font-size:48px">🎁</div>
  <h3 style="text-align:center;margin:12px">Invite Your Friends</h3>
  <p class="muted" style="text-align:center">বন্ধুদের সঙ্গে তোমার লিংক শেয়ার করো।</p>

  <div class="ref-link" id="refLink">Telegram required</div>

  <button class="main-btn" onclick="copyReferral()">📋 COPY LINK</button>
  <button class="secondary-btn" onclick="shareReferral()">📤 SHARE LINK</button>
  <p class="status">Referral bonus পেতে backend verification প্রয়োজন।</p>
 </div>
</section>

<!-- HISTORY -->
<section id="history" class="page">
 <h2 class="section-title">📜 Transaction History</h2>
 <div class="card">
  <div id="historyList" class="empty">কোনো রেকর্ড নেই।</div>
 </div>
</section>

<!-- PROFILE -->
<section id="profile" class="page">
 <h2 class="section-title">👤 My Profile</h2>

 <div class="card">
  <div style="font-size:55px;text-align:center">👨‍💻</div>
  <h3 id="profileName" style="text-align:center;margin:12px">Guest User</h3>
  <p class="muted" style="text-align:center">Giga Earn BD Member</p>

  <div class="row"><span>Telegram ID</span><b id="telegramId">Guest</b></div>
  <div class="row"><span>Application ID</span><b>8982</b></div>
  <div class="row"><span>Ad Network</span><b>GigaPub</b></div>
  <div class="row"><span>Balance</span><b>৳ <span id="profileBalance">0.00</span></b></div>
 </div>
</section>

<div class="footer">© 2026 Giga Earn BD</div>
</div>

<!-- NAVIGATION -->
<nav class="nav">
 <button class="active" data-page="home" onclick="showPage('home',this)">
  <span class="nav-icon">🏠</span>Home
 </button>
 <button data-page="wallet" onclick="showPage('wallet',this)">
  <span class="nav-icon">💰</span>Wallet
 </button>
 <button data-page="refer" onclick="showPage('refer',this)">
  <span class="nav-icon">👥</span>Refer
 </button>
 <button data-page="profile" onclick="showPage('profile',this)">
  <span class="nav-icon">👤</span>Profile
 </button>
</nav>

<script>
"use strict";

// TELEGRAM
const tg = window.Telegram?.WebApp;
tg?.ready();
tg?.expand();

const user = tg?.initDataUnsafe?.user || null;
const BOT_USERNAME = "YOUR_BOT_USERNAME";

// LOCAL DEMO DATA
let balance = 0;
let adsCount = 0;
let historyData = [];
let busy = false;

// USER INFORMATION
if(user){
 const fullName = [user.first_name,user.last_name]
  .filter(Boolean).join(" ") || "User";

 document.getElementById("username").textContent = user.first_name || "User";
 document.getElementById("welcome").textContent = "Welcome, " + fullName + " 👋";
 document.getElementById("profileName").textContent = fullName;
 document.getElementById("telegramId").textContent = user.id;
}

// PAGE NAVIGATION
function showPage(page,btn){
 document.querySelectorAll(".page").forEach(el=>{
  el.classList.remove("active");
 });

 document.getElementById(page).classList.add("active");

 document.querySelectorAll(".nav button").forEach(el=>{
  el.classList.remove("active");
 });

 const target = btn || document.querySelector(
  '.nav button[data-page="'+page+'"]'
 );
 target?.classList.add("active");

 window.scrollTo({top:0,behavior:"smooth"});
}

// UPDATE BALANCE DISPLAY
function updateUI(){
 ["balance","walletBalance","profileBalance"].forEach(id=>{
  document.getElementById(id).textContent = balance.toFixed(2);
 });

 document.getElementById("adsCount").textContent = adsCount;
}

// GIGAPUB AD
async function watchAd(){
 if(busy) return;

 const btn = document.getElementById("watchBtn");
 const status = document.getElementById("adStatus");

 if(typeof window.showGiga !== "function"){
  status.textContent = "Ad SDK not loaded. Check GigaPub approval.";
  return;
 }

 busy = true;
 btn.disabled = true;
 btn.textContent = "LOADING AD...";

 status.textContent = "Advertisement loading...";

 try{
  await window.showGiga();

  adsCount++;
  updateUI();

  addHistory("Advertisement completed","Pending verification");

  status.textContent =
   "Ad completed. Reward verification is pending.";

  tg?.HapticFeedback?.notificationOccurred("success");

 }catch(error){
  status.textContent = "Ad not completed. Please try again.";
  tg?.HapticFeedback?.notificationOccurred("error");

 }finally{
  busy = false;
  btn.disabled = false;
  btn.textContent = "▶ WATCH ADS";
 }
}

document.getElementById("watchBtn").addEventListener("click",watchAd);

// REFERRAL
function getReferralLink(){
 if(!user || BOT_USERNAME === "YOUR_BOT_USERNAME") return "";
 return "https://t.me/" + BOT_USERNAME + "?startapp=" + user.id;
}

function setupReferral(){
 document.getElementById("refLink").textContent =
  getReferralLink() || "Set your bot username to activate referral link.";
}

async function copyReferral(){
 const link = getReferralLink();

 if(!link){
  alert("আগে নিজের Bot Username সেট করো।");
  return;
 }

 try{
  await navigator.clipboard.writeText(link);
  alert("Referral link copied!");
 }catch(e){
  alert(link);
 }
}

function shareReferral(){
 const link = getReferralLink();

 if(!link){
  alert("Bot Username সেট করো।");
  return;
 }

 const shareURL = "https://t.me/share/url?url=" +
  encodeURIComponent(link) +
  "&text=" + encodeURIComponent("Join Giga Earn BD!");

 if(tg) tg.openTelegramLink(shareURL);
 else window.open(shareURL,"_blank");
}

// HISTORY
function addHistory(title,amount){
 historyData.unshift({
  title,
  amount,
  date:new Date().toLocaleString()
 });
 renderHistory();
}

function renderHistory(){
 const box = document.getElementById("historyList");
 box.replaceChildren();

 if(historyData.length === 0){
  box.className = "empty";
  box.textContent = "কোনো রেকর্ড নেই।";
  return;
 }

 box.className = "";

 historyData.forEach(item=>{
  const row = document.createElement("div");
  row.className = "row";

  const info = document.createElement("div");
  const title = document.createElement("b");
  title.textContent = item.title;

  const date = document.createElement("p");
  date.className = "muted";
  date.textContent = item.date;

  info.append(title,date);

  const amount = document.createElement("b");
  amount.textContent = item.amount;

  row.append(info,amount);
  box.append(row);
 });
}

// WITHDRAW FORM
function withdraw(){
 const amount = Number(document.getElementById("amount").value);
 const number = document.getElementById("number").value.trim();
 const method = document.getElementById("method").value;

 const status = document.getElementById("withdrawStatus");

 if(!Number.isFinite(amount) || amount <= 0){
  status.textContent = "সঠিক পরিমাণ লিখুন।";
  return;
 }

 if(!number || !/^[0-9+\-\s]{8,20}$/.test(number)){
  status.textContent = "সঠিক পেমেন্ট নম্বর লিখুন।";
  return;
 }

 status.textContent =
  "Withdrawal backend সংযুক্ত নেই। আবেদন জমা হয়নি।";
}

// INITIALIZE
setupReferral();
updateUI();
renderHistory();

</script>
</body>
</html>
