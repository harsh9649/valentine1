<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>For Shilpi ❤️</title>

  <style>
    body{
      margin:0;
      height:100vh;
      display:flex;
      justify-content:center;
      align-items:center;
      background: radial-gradient(circle at top, #ffd6e4, #ff2f60);
      font-family: Arial, sans-serif;
      overflow:hidden;
      color:white;
      text-align:center;
    }

    /* background sparkles */
    .sparkleBg{
      position:absolute;
      inset:0;
      background:
        radial-gradient(circle at 20% 30%, rgba(255,255,255,0.18), transparent 35%),
        radial-gradient(circle at 70% 20%, rgba(255,255,255,0.14), transparent 38%),
        radial-gradient(circle at 50% 70%, rgba(255,255,255,0.11), transparent 42%),
        radial-gradient(circle at 85% 75%, rgba(255,255,255,0.10), transparent 40%);
      animation: shimmer 5s ease-in-out infinite alternate;
      z-index:0;
      pointer-events:none;
    }
    @keyframes shimmer{
      from{ opacity:0.55; filter: blur(0px); }
      to{ opacity:0.9; filter: blur(0.5px); }
    }

    canvas{
      position:absolute;
      inset:0;
      pointer-events:none;
    }
    #confetti{ z-index:1; }
    #fireworks{ z-index:2; }

    .card{
      width: min(92vw, 560px);
      background: rgba(255,255,255,0.16);
      border: 1px solid rgba(255,255,255,0.22);
      padding: 28px 18px;
      border-radius: 22px;
      backdrop-filter: blur(7px);
      box-shadow: 0 12px 35px rgba(0,0,0,0.28);
      z-index:5;
      animation: pop 1.0s ease forwards;
      position: relative;
    }

    @keyframes pop{
      0%{ transform:scale(0.85); opacity:0;}
      100%{ transform:scale(1); opacity:1;}
    }

    h1{ font-size: 34px; margin: 0 0 8px; }

    .sub{
      font-size: 17px;
      opacity:0.96;
      margin-bottom: 10px;
    }

    /* ✅ GIF container */
    .gifWrap{
      width: min(320px, 80vw);
      border-radius: 18px;
      overflow:hidden;
      margin: 14px auto 14px;
      border: 1px solid rgba(255,255,255,0.28);
      box-shadow: 0 10px 28px rgba(0,0,0,0.25);
      position:relative;
      animation: glowPulse 2.4s ease-in-out infinite;
    }
    @keyframes glowPulse{
      0%{ transform:scale(1); box-shadow: 0 10px 28px rgba(0,0,0,0.25); }
      50%{ transform:scale(1.02); box-shadow: 0 0 26px rgba(255,255,255,0.32); }
      100%{ transform:scale(1); box-shadow: 0 10px 28px rgba(0,0,0,0.25); }
    }

    .gifWrap::after{
      content:"";
      position:absolute;
      inset:-12px;
      border-radius: 22px;
      border: 2px dashed rgba(255,255,255,0.26);
      animation: spin 12s linear infinite;
      pointer-events:none;
    }
    @keyframes spin{
      from{ transform: rotate(0deg); }
      to{ transform: rotate(360deg); }
    }

    .gifWrap img{
      width:100%;
      display:block;
    }

    /* ✅ GIF hidden initially */
    #gifBox{ display:none; }

    /* ✅ after YES show with animation */
    .showGif{
      display:block !important;
      animation: gifPop 0.55s ease forwards;
    }
    @keyframes gifPop{
      0%{ transform: scale(0.7); opacity:0; }
      100%{ transform: scale(1); opacity:1; }
    }

    #proposal{
      font-size: 28px;
      font-weight: 800;
      margin-top: 12px;
      animation: glow 1.2s ease-in-out infinite alternate;
    }
    @keyframes glow{
      from{ text-shadow: 0 0 6px rgba(255,255,255,0.30); }
      to{ text-shadow: 0 0 18px rgba(255,255,255,0.75); }
    }

    .btnRow{
      margin-top: 18px;
      display:flex;
      justify-content:center;
      gap: 14px;
      flex-wrap: wrap;
      position: relative;
      min-height: 60px;
    }

    button{
      border: none;
      padding: 12px 18px;
      border-radius: 14px;
      font-size: 16px;
      font-weight: 800;
      cursor: pointer;
      transition: transform .14s ease;
      user-select:none;
    }
    button:hover{ transform: translateY(-2px); }

    .yes{
      background: white;
      color:#ff2f60;
      animation: yesBounce 1.6s ease-in-out infinite;
    }
    @keyframes yesBounce{
      0%,100%{ transform: translateY(0); }
      50%{ transform: translateY(-4px); }
    }

    .no{
      background: rgba(0,0,0,0.20);
      color:white;
      border: 1px solid rgba(255,255,255,0.3);
      position: relative;
    }

    .small{
      margin-top: 12px;
      font-size: 15px;
      opacity: 0.95;
    }

    .hidden{ display:none; }

    /* floating hearts */
    .heart{
      position:absolute;
      width:14px;
      height:14px;
      background: rgba(255,255,255,0.95);
      transform: rotate(45deg);
      border-radius: 2px;
      animation: floatUp 3.8s linear infinite;
      opacity:0.85;
      z-index:3;
      pointer-events:none;
    }
    .heart:before,.heart:after{
      content:"";
      position:absolute;
      width:14px;
      height:14px;
      background: rgba(255,255,255,0.95);
      border-radius:50%;
    }
    .heart:before{ left:-7px; top:0; }
    .heart:after{ left:0; top:-7px; }
    @keyframes floatUp{
      0%{ transform: translateY(30px) rotate(45deg); opacity:0}
      10%{opacity:0.85}
      100%{ transform: translateY(-120vh) rotate(45deg); opacity:0}
    }

    #success{
      font-size: 26px;
      font-weight: 800;
      margin-top: 10px;
      line-height: 1.35;
    }

    /* BOOM text animation */
    .boomText{
      position:absolute;
      left:50%;
      top:50%;
      transform: translate(-50%,-50%) scale(0.2);
      font-weight:900;
      font-size: clamp(28px, 6vw, 70px);
      letter-spacing: 2px;
      text-shadow: 0 0 18px rgba(255,255,255,0.8);
      opacity:0;
      z-index:9;
      pointer-events:none;
      animation: boomPop 1s ease forwards;
    }
    @keyframes boomPop{
      0%   {opacity:0; transform:translate(-50%,-50%) scale(0.2);}
      25%  {opacity:1; transform:translate(-50%,-50%) scale(1.15);}
      60%  {opacity:1; transform:translate(-50%,-50%) scale(1.0);}
      100% {opacity:0; transform:translate(-50%,-50%) scale(1.8);}
    }
  </style>
</head>

<body>
  <div class="sparkleBg"></div>

  <!-- Music file: perfect.mp3 -->
  <audio id="bgMusic" preload="auto">
    <source src="perfect.mp3" type="audio/mpeg">
  </audio>

  <canvas id="confetti"></canvas>
  <canvas id="fireworks"></canvas>

  <div class="card">
    <h1>Hi Shilpi ❤️</h1>
    <div class="sub">Just one question…</div>

    <!-- ✅ GIF (hidden initially) -->
    <div class="gifWrap" id="gifBox">
      <img src="valentine.gif" alt="Valentine GIF">
    </div>

    <div id="main">
      <div id="proposal">Will you be my Valentine, Shilpi? 💌</div>

      <div class="btnRow" id="btnRow">
        <button class="yes" onclick="yesClicked()">YES 💖</button>
        <button class="no" id="noBtn" onclick="noClicked()">NO 🙈</button>
      </div>

      <div class="small" id="hint">Tip: Choose wisely 😄</div>
    </div>

    <div id="afterYes" class="hidden">
      <div id="success">
        Shilpi, I’m really happy you said yes ❤️ <br/>
        This means a lot to me.
      </div>
      <div class="small">— Harsh ❤️</div>
    </div>
  </div>

<script>
  // Confetti canvas
  const confCanvas = document.getElementById("confetti");
  const confCtx = confCanvas.getContext("2d");

  // Fireworks canvas
  const fwCanvas = document.getElementById("fireworks");
  const fwCtx = fwCanvas.getContext("2d");

  function resize(){
    confCanvas.width = innerWidth;
    confCanvas.height = innerHeight;
    fwCanvas.width = innerWidth;
    fwCanvas.height = innerHeight;
  }
  addEventListener("resize", resize);
  resize();

  // Confetti
  let confettiOn = false;
  const pieces = [];

  function addConfetti(){
    pieces.length = 0;
    for(let i=0;i<220;i++){
      pieces.push({
        x: Math.random()*confCanvas.width,
        y: -20 - Math.random()*confCanvas.height,
        r: 2 + Math.random()*4,
        s: 1 + Math.random()*3.2,
        a: Math.random()*Math.PI,
      });
    }
  }

  function drawConfetti(){
    confCtx.clearRect(0,0,confCanvas.width,confCanvas.height);
    if(confettiOn){
      pieces.forEach(p=>{
        p.y += p.s;
        p.x += Math.sin(p.a) * 1.1;
        p.a += 0.02;

        confCtx.beginPath();
        confCtx.arc(p.x,p.y,p.r,0,Math.PI*2);
        confCtx.fillStyle = "rgba(255,255,255,0.85)";
        confCtx.fill();

        if(p.y > confCanvas.height+40){
          p.y = -20;
          p.x = Math.random()*confCanvas.width;
        }
      });
    }
    requestAnimationFrame(drawConfetti);
  }

  // Hearts
  function spawnHearts(){
    const h = document.createElement("div");
    h.className = "heart";
    h.style.left = Math.random()*100 + "vw";
    h.style.animationDuration = (2.2 + Math.random()*3.6) + "s";
    const size = (10 + Math.random()*22);
    h.style.width = h.style.height = size + "px";
    document.body.appendChild(h);
    setTimeout(()=>h.remove(), 6500);
  }
  function heartBurst(){
    for(let i=0;i<40;i++){
      setTimeout(spawnHearts, i*110);
    }
  }

  // BOOM text
  function boom(text){
    const el = document.createElement("div");
    el.className = "boomText";
    el.textContent = text;
    document.body.appendChild(el);
    setTimeout(()=>el.remove(), 1000);
  }

  // Fireworks
  const fireworks = [];
  function fireworkBurst(x,y){
    const count = 55 + Math.floor(Math.random()*40);
    for(let i=0;i<count;i++){
      fireworks.push({
        x,y,
        vx: (Math.random()-0.5)*8,
        vy: (Math.random()-0.5)*8,
        life: 60 + Math.random()*30
      });
    }
  }
  function drawFireworks(){
    fwCtx.clearRect(0,0,fwCanvas.width,fwCanvas.height);

    for(let i=fireworks.length-1;i>=0;i--){
      const p = fireworks[i];
      p.x += p.vx;
      p.y += p.vy;
      p.vy += 0.05;
      p.life -= 1;

      fwCtx.beginPath();
      fwCtx.arc(p.x,p.y,2,0,Math.PI*2);
      fwCtx.fillStyle = "rgba(255,255,255,0.92)";
      fwCtx.fill();

      if(p.life<=0) fireworks.splice(i,1);
    }
    requestAnimationFrame(drawFireworks);
  }

  // No prank
  const noBtn = document.getElementById("noBtn");
  const btnRow = document.getElementById("btnRow");
  let noCount = 0;

  function moveNoButton(){
    const rect = btnRow.getBoundingClientRect();
    const maxX = rect.width - 110;
    const maxY = 12;

    noBtn.style.position = "absolute";
    noBtn.style.left = Math.max(0, Math.random()*maxX) + "px";
    noBtn.style.top  = Math.max(0, Math.random()*maxY) + "px";
  }

  function noClicked(){
    noCount++;
    document.getElementById("hint").innerText =
      (noCount <= 2) ? "Shilpi… NO mat dabao 🙈😄" :
      (noCount <= 4) ? "Hehe… NO ab pakad me nahi aayega 😁" :
      "Bas bas… YES hi option hai 😍";
    moveNoButton();
  }
  noBtn.addEventListener("mouseenter", moveNoButton);
  noBtn.addEventListener("touchstart", (e)=>{ e.preventDefault(); moveNoButton(); });

  // YES action
  function yesClicked(){
    // Show GIF only after yes
    const gif = document.getElementById("gifBox");
    gif.classList.add("showGif");

    // Play music
    const music = document.getElementById("bgMusic");
    music.volume = 0.65;
    music.play().catch(()=>{});

    // Switch to success message
    document.getElementById("main").classList.add("hidden");
    document.getElementById("afterYes").classList.remove("hidden");

    // Animations
    confettiOn = true;
    addConfetti();

    heartBurst();
    setInterval(spawnHearts, 480);

    const bursts = 10;
    for(let i=0;i<bursts;i++){
      setTimeout(()=>{
        fireworkBurst(
          Math.random()*fwCanvas.width,
          (Math.random()*fwCanvas.height*0.6) + 50
        );
      }, i*240);
    }

    // Cute minimal BOOM
    ["BOOM 💥","CRACKERS 🎆","YAY ✨"].forEach((w,idx)=>{
      setTimeout(()=>boom(w), idx*330);
    });
  }

  drawConfetti();
  drawFireworks();
</script>

</body>
</html># valentine1
