# Padasalai
Padasalai CBSE School — Tambaram, Chennai Nestled in the heart of Tambaram, Chennai, Padasalai CBSE School stands as a beacon of academic excellence and holistic development. Established with a passionate vision to nurture young minds, our school has grown into one of the most trusted educational institutions in the region
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Nithik AI — Your Intelligent Partner</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,400&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet"/>
<style>
:root {
  --bg:#07070f; --bg2:#0e0e1a;
  --surface:rgba(255,255,255,0.04); --border:rgba(255,255,255,0.07);
  --nithik:#a78bfa; --nithik2:#7c3aed;
  --user-c:#34d399; --text:#eeeeff;
  --muted:rgba(238,238,255,0.45);
  --glow-n:0 0 40px rgba(167,139,250,0.3);
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
html,body{height:100%;overflow:hidden;}
body{background:var(--bg);color:var(--text);font-family:'DM Sans',sans-serif;display:flex;flex-direction:column;cursor:none;}

#cur-ring{width:26px;height:26px;border:1.5px solid rgba(167,139,250,0.6);border-radius:50%;position:fixed;top:0;left:0;transform:translate(-50%,-50%);pointer-events:none;z-index:99999;transition:transform 0.15s ease,border-color 0.2s;}
#cur-dot{width:5px;height:5px;background:var(--nithik);border-radius:50%;position:fixed;top:0;left:0;transform:translate(-50%,-50%);pointer-events:none;z-index:99999;}
#bg-canvas{position:fixed;inset:0;z-index:0;}
.app{position:relative;z-index:1;display:flex;flex-direction:column;height:100vh;}

header{display:flex;align-items:center;justify-content:space-between;padding:0 24px;height:62px;border-bottom:1px solid var(--border);background:rgba(7,7,15,0.88);backdrop-filter:blur(24px);flex-shrink:0;}
.h-left{display:flex;align-items:center;gap:12px;}
.avatar{width:38px;height:38px;border-radius:50%;background:linear-gradient(135deg,#a78bfa,#7c3aed);display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-weight:800;font-size:1rem;color:#fff;box-shadow:var(--glow-n);position:relative;flex-shrink:0;}
.avatar::after{content:'';position:absolute;bottom:1px;right:1px;width:9px;height:9px;border-radius:50%;background:#34d399;border:2px solid var(--bg);animation:blink 2s ease infinite;}
@keyframes blink{0%,100%{box-shadow:0 0 0 0 rgba(52,211,153,0.6)}50%{box-shadow:0 0 0 5px rgba(52,211,153,0)}}
.n-name{font-family:'Syne',sans-serif;font-weight:800;font-size:1.05rem;background:linear-gradient(90deg,#a78bfa,#c4b5fd);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;}
.n-status{font-size:0.68rem;color:#34d399;letter-spacing:1px;}
.h-right{display:flex;align-items:center;gap:10px;}
.badge{padding:5px 12px;border:1px solid rgba(167,139,250,0.25);background:rgba(167,139,250,0.07);border-radius:20px;font-size:0.7rem;letter-spacing:1px;color:var(--nithik);font-family:'JetBrains Mono',monospace;}
.new-btn{padding:7px 16px;background:rgba(167,139,250,0.1);border:1px solid rgba(167,139,250,0.2);color:var(--nithik);font-family:'Syne',sans-serif;font-weight:700;font-size:0.75rem;letter-spacing:1px;cursor:none;transition:all 0.25s;border-radius:4px;}
.new-btn:hover{background:rgba(167,139,250,0.2);border-color:rgba(167,139,250,0.45);}

.chat-wrap{flex:1;overflow-y:auto;overflow-x:hidden;padding:32px 0;scroll-behavior:smooth;}
.chat-wrap::-webkit-scrollbar{width:4px;}
.chat-wrap::-webkit-scrollbar-thumb{background:rgba(167,139,250,0.2);border-radius:4px;}
.chat-inner{max-width:780px;margin:0 auto;padding:0 20px;display:flex;flex-direction:column;gap:24px;}

.welcome{text-align:center;padding:60px 20px 40px;animation:fadeUp 0.6s ease forwards;}
@keyframes fadeUp{from{opacity:0;transform:translateY(16px)}to{opacity:1;transform:translateY(0)}}
.welcome-avatar{width:80px;height:80px;border-radius:50%;background:linear-gradient(135deg,#a78bfa,#6d28d9);display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-weight:800;font-size:2rem;color:#fff;margin:0 auto 20px;box-shadow:0 0 60px rgba(167,139,250,0.4),0 0 120px rgba(167,139,250,0.12);animation:floatAv 4s ease-in-out infinite;}
@keyframes floatAv{0%,100%{transform:translateY(0) scale(1)}50%{transform:translateY(-8px) scale(1.03)}}
.welcome h1{font-family:'Syne',sans-serif;font-weight:800;font-size:2rem;background:linear-gradient(135deg,#a78bfa,#f0abfc,#818cf8);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;margin-bottom:10px;}
.welcome p{color:var(--muted);font-size:0.95rem;line-height:1.75;max-width:480px;margin:0 auto 32px;}
.suggestions{display:flex;flex-wrap:wrap;gap:10px;justify-content:center;}
.sug-btn{padding:10px 18px;border:1px solid var(--border);background:var(--surface);color:rgba(238,238,255,0.7);font-family:'DM Sans',sans-serif;font-size:0.82rem;cursor:none;border-radius:24px;transition:all 0.25s;}
.sug-btn:hover{border-color:rgba(167,139,250,0.4);background:rgba(167,139,250,0.09);color:#fff;transform:translateY(-2px);}

.msg{display:flex;gap:12px;animation:fadeUp 0.4s ease forwards;opacity:0;}
.msg.user{flex-direction:row-reverse;}
.msg-avatar{width:32px;height:32px;border-radius:50%;flex-shrink:0;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:0.75rem;margin-top:4px;}
.msg.nithik .msg-avatar{background:linear-gradient(135deg,#a78bfa,#7c3aed);box-shadow:0 0 15px rgba(167,139,250,0.3);color:#fff;}
.msg.user .msg-avatar{background:linear-gradient(135deg,#34d399,#059669);color:#fff;}
.msg-body{max-width:72%;display:flex;flex-direction:column;gap:5px;}
.msg.user .msg-body{align-items:flex-end;}
.msg-name{font-size:0.68rem;letter-spacing:1px;font-weight:600;text-transform:uppercase;}
.msg.nithik .msg-name{color:var(--nithik);}
.msg.user .msg-name{color:var(--user-c);}
.msg-bubble{padding:14px 18px;font-size:0.92rem;line-height:1.78;word-break:break-word;}
.msg.nithik .msg-bubble{background:rgba(167,139,250,0.08);border:1px solid rgba(167,139,250,0.13);border-radius:4px 18px 18px 18px;color:var(--text);}
.msg.user .msg-bubble{background:rgba(52,211,153,0.09);border:1px solid rgba(52,211,153,0.15);border-radius:18px 4px 18px 18px;color:var(--text);}
.msg-bubble pre{background:rgba(0,0,0,0.45);border:1px solid rgba(255,255,255,0.08);border-radius:8px;padding:14px;overflow-x:auto;margin:10px 0;font-family:'JetBrains Mono',monospace;font-size:0.8rem;line-height:1.6;}
.msg-bubble code{font-family:'JetBrains Mono',monospace;font-size:0.82rem;background:rgba(167,139,250,0.12);padding:2px 6px;border-radius:4px;color:#c4b5fd;}
.msg-bubble pre code{background:none;padding:0;color:#a5f3fc;}
.msg-bubble strong{color:#fff;font-weight:600;}
.msg-bubble em{color:#c4b5fd;}
.msg-bubble ul,.msg-bubble ol{padding-left:20px;margin:8px 0;}
.msg-bubble li{margin-bottom:4px;}
.msg-bubble h1,.msg-bubble h2,.msg-bubble h3{font-family:'Syne',sans-serif;color:#fff;margin:12px 0 6px;}
.msg-time{font-size:0.62rem;color:rgba(238,238,255,0.2);padding:0 4px;}

.typing-dots{display:flex;gap:5px;align-items:center;padding:14px 18px;background:rgba(167,139,250,0.08);border:1px solid rgba(167,139,250,0.13);border-radius:4px 18px 18px 18px;width:fit-content;}
.typing-dots span{width:7px;height:7px;border-radius:50%;background:var(--nithik);opacity:0.4;animation:typeBounce 1.2s ease infinite;}
.typing-dots span:nth-child(2){animation-delay:.2s}
.typing-dots span:nth-child(3){animation-delay:.4s}
@keyframes typeBounce{0%,60%,100%{transform:translateY(0);opacity:0.4}30%{transform:translateY(-7px);opacity:1}}

.input-area{flex-shrink:0;border-top:1px solid var(--border);background:rgba(7,7,15,0.92);backdrop-filter:blur(24px);padding:16px 20px 20px;}
.input-inner{max-width:780px;margin:0 auto;}
.input-box{display:flex;align-items:flex-end;gap:10px;background:rgba(255,255,255,0.04);border:1px solid var(--border);border-radius:14px;padding:10px 10px 10px 18px;transition:border-color 0.25s,box-shadow 0.25s;}
.input-box:focus-within{border-color:rgba(167,139,250,0.38);box-shadow:0 0 0 3px rgba(167,139,250,0.07),0 0 30px rgba(167,139,250,0.1);}
#user-input{flex:1;background:none;border:none;outline:none;color:var(--text);font-family:'DM Sans',sans-serif;font-size:0.92rem;line-height:1.6;resize:none;max-height:160px;min-height:24px;overflow-y:auto;cursor:none;}
#user-input::placeholder{color:rgba(238,238,255,0.25);}
.send-btn{width:38px;height:38px;border-radius:10px;flex-shrink:0;background:linear-gradient(135deg,#a78bfa,#7c3aed);border:none;cursor:none;display:flex;align-items:center;justify-content:center;transition:all 0.2s;box-shadow:0 4px 15px rgba(124,58,237,0.4);}
.send-btn:hover{transform:scale(1.08);box-shadow:0 6px 22px rgba(124,58,237,0.6);}
.send-btn:active{transform:scale(0.95);}
.send-btn:disabled{opacity:0.4;transform:none;cursor:not-allowed;}
.send-btn svg{width:16px;height:16px;fill:white;}
.input-hint{display:flex;align-items:center;justify-content:space-between;margin-top:10px;padding:0 4px;}
.hint-left{font-size:0.65rem;color:rgba(238,238,255,0.2);}
.hint-left span{color:rgba(167,139,250,0.5);}
.powered{font-size:0.62rem;color:rgba(238,238,255,0.18);font-family:'JetBrains Mono',monospace;letter-spacing:1px;}

/* MODAL */
.modal-overlay{position:fixed;inset:0;z-index:10000;background:rgba(7,7,15,0.96);backdrop-filter:blur(20px);display:flex;align-items:center;justify-content:center;animation:mfade 0.3s ease;}
@keyframes mfade{from{opacity:0}to{opacity:1}}
.modal{background:var(--bg2);border:1px solid rgba(167,139,250,0.18);border-radius:20px;padding:44px 40px;max-width:460px;width:92%;box-shadow:0 40px 80px rgba(0,0,0,0.7),var(--glow-n);animation:mslide 0.4s ease;}
@keyframes mslide{from{opacity:0;transform:translateY(30px)}to{opacity:1;transform:translateY(0)}}
.modal-av{width:70px;height:70px;border-radius:50%;background:linear-gradient(135deg,#a78bfa,#6d28d9);display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-weight:800;font-size:1.8rem;color:#fff;margin:0 auto 22px;box-shadow:0 0 50px rgba(167,139,250,0.4);animation:floatAv 4s ease-in-out infinite;}
.modal h2{font-family:'Syne',sans-serif;font-weight:800;font-size:1.6rem;text-align:center;margin-bottom:8px;background:linear-gradient(90deg,#a78bfa,#c4b5fd);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;}
.modal p{color:var(--muted);font-size:0.88rem;text-align:center;line-height:1.65;margin-bottom:26px;}
.chips{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:22px;justify-content:center;}
.chip{padding:5px 13px;border-radius:20px;border:1px solid rgba(167,139,250,0.2);background:rgba(167,139,250,0.07);font-size:0.72rem;color:var(--nithik);}
.modal label{display:block;font-size:0.7rem;letter-spacing:2px;color:var(--nithik);margin-bottom:8px;text-transform:uppercase;}
.modal input{width:100%;padding:13px 16px;background:rgba(255,255,255,0.05);border:1px solid rgba(167,139,250,0.2);border-radius:8px;color:var(--text);font-family:'JetBrains Mono',monospace;font-size:0.82rem;outline:none;margin-bottom:6px;transition:border-color 0.2s,box-shadow 0.2s;cursor:none;}
.modal input:focus{border-color:rgba(167,139,250,0.5);box-shadow:0 0 0 3px rgba(167,139,250,0.08);}
.modal-btn{width:100%;padding:14px;background:linear-gradient(135deg,#a78bfa,#7c3aed);border:none;border-radius:10px;color:#fff;font-family:'Syne',sans-serif;font-weight:700;font-size:0.92rem;letter-spacing:1px;cursor:none;transition:all 0.25s;box-shadow:0 8px 25px rgba(124,58,237,0.4);margin-top:10px;}
.modal-btn:hover{transform:translateY(-2px);box-shadow:0 12px 32px rgba(124,58,237,0.55);}
.modal-note{font-size:0.68rem;color:rgba(238,238,255,0.2);text-align:center;margin-top:14px;line-height:1.6;}
.modal-note a{color:rgba(167,139,250,0.5);}
.modal-err{color:#f87171;font-size:0.78rem;text-align:center;margin-bottom:10px;display:none;}

*{scrollbar-width:thin;scrollbar-color:rgba(167,139,250,0.15) transparent;}
@media(max-width:600px){.badge,.new-btn{display:none;}.chat-inner{padding:0 12px;}.modal{padding:28px 18px;}}
</style>
</head>
<body>

<div id="cur-ring"></div>
<div id="cur-dot"></div>
<canvas id="bg-canvas"></canvas>

<!-- MODAL -->
<div class="modal-overlay" id="modal">
  <div class="modal">
    <div class="modal-av">N</div>
    <h2>Meet Nithik ✨</h2>
    <p>Your brilliant AI partner — here to answer anything, help with studies, write code, tell stories, and be your smartest friend. Enter your Anthropic API key to start.</p>
    <div class="chips">
      <span class="chip">🧠 Super Smart</span>
      <span class="chip">💬 Always Friendly</span>
      <span class="chip">⚡ Instant Replies</span>
      <span class="chip">🔒 100% Private</span>
    </div>
    <label>Your Anthropic API Key</label>
    <input type="password" id="api-key-input" placeholder="sk-ant-api03-..." autocomplete="off"/>
    <div class="modal-err" id="modal-err"></div>
    <button class="modal-btn" onclick="startChat()">Start Chatting with Nithik →</button>
    <div class="modal-note">Key stays in your browser only — never stored anywhere.<br/>Get one free at <a href="https://console.anthropic.com" target="_blank">console.anthropic.com</a></div>
  </div>
</div>

<!-- APP -->
<div class="app" id="app" style="display:none;">
  <header>
    <div class="h-left">
      <div class="avatar">N</div>
      <div>
        <div class="n-name">Nithik</div>
        <div class="n-status">● Online · Always here for you</div>
      </div>
    </div>
    <div class="h-right">
      <span class="badge">Claude + GPT Mix</span>
      <button class="new-btn" onclick="newChat()">+ New Chat</button>
    </div>
  </header>

  <div class="chat-wrap" id="chat-wrap">
    <div class="chat-inner" id="chat-inner">
      <div class="welcome" id="welcome-screen">
        <div class="welcome-avatar">N</div>
        <h1>Hey! I'm Nithik 👋</h1>
        <p>Your AI partner — ask me anything at all! Questions, homework, coding, writing, stories, advice, or just a fun chat. I'm here for you.</p>
        <div class="suggestions">
          <button class="sug-btn" onclick="sendSug(this)">🧠 Explain black holes simply</button>
          <button class="sug-btn" onclick="sendSug(this)">✍️ Write a poem about friendship</button>
          <button class="sug-btn" onclick="sendSug(this)">💻 Teach me Python basics</button>
          <button class="sug-btn" onclick="sendSug(this)">📚 Help me study for my exam</button>
          <button class="sug-btn" onclick="sendSug(this)">🎯 How to be more productive?</button>
          <button class="sug-btn" onclick="sendSug(this)">😄 Tell me a fun fact!</button>
        </div>
      </div>
    </div>
  </div>

  <div class="input-area">
    <div class="input-inner">
      <div class="input-box">
        <textarea id="user-input" rows="1" placeholder="Ask Nithik anything…" onkeydown="handleKey(event)" oninput="autoResize(this)"></textarea>
        <button class="send-btn" id="send-btn" onclick="sendMessage()">
          <svg viewBox="0 0 24 24"><path d="M2.01 21L23 12 2.01 3 2 10l15 2-15 2z"/></svg>
        </button>
      </div>
      <div class="input-hint">
        <div class="hint-left">Press <span>Enter</span> to send &nbsp;·&nbsp; <span>Shift+Enter</span> for new line</div>
        <div class="powered">⚡ Nithik AI</div>
      </div>
    </div>
  </div>
</div>

<script>
// ── CURSOR ──────────────────────────────────────────
const ring = document.getElementById('cur-ring');
const dot  = document.getElementById('cur-dot');
let mx=0,my=0,rx=0,ry=0;
document.addEventListener('mousemove',e=>{mx=e.clientX;my=e.clientY;dot.style.left=mx+'px';dot.style.top=my+'px';});
(function loop(){rx+=(mx-rx)*.12;ry+=(my-ry)*.12;ring.style.left=rx+'px';ring.style.top=ry+'px';requestAnimationFrame(loop);})();
function addHover(sel){document.querySelectorAll(sel).forEach(el=>{el.addEventListener('mouseenter',()=>{ring.style.transform='translate(-50%,-50%) scale(1.9)';ring.style.borderColor='rgba(167,139,250,0.9)';});el.addEventListener('mouseleave',()=>{ring.style.transform='translate(-50%,-50%) scale(1)';ring.style.borderColor='rgba(167,139,250,0.6)';});});}
addHover('button,textarea,input,a,.sug-btn');

// ── CANVAS BG ───────────────────────────────────────
const cv=document.getElementById('bg-canvas'),cx=cv.getContext('2d');
let W,H;
function rsz(){W=cv.width=innerWidth;H=cv.height=innerHeight;}rsz();window.addEventListener('resize',rsz);
const pts=Array.from({length:75},()=>({x:Math.random()*2000,y:Math.random()*1200,vx:(Math.random()-.5)*.22,vy:(Math.random()-.5)*.22,r:Math.random()*1.8+.4,c:Math.random()<.65?'167,139,250':Math.random()<.5?'52,211,153':'248,113,113'}));
function drawBg(){cx.clearRect(0,0,W,H);pts.forEach(p=>{p.x+=p.vx;p.y+=p.vy;if(p.x<0)p.x=W;if(p.x>W)p.x=0;if(p.y<0)p.y=H;if(p.y>H)p.y=0;cx.beginPath();cx.arc(p.x,p.y,p.r,0,Math.PI*2);cx.fillStyle=`rgba(${p.c},0.55)`;cx.fill();});for(let i=0;i<pts.length;i++)for(let j=i+1;j<pts.length;j++){const dx=pts[i].x-pts[j].x,dy=pts[i].y-pts[j].y,d=Math.sqrt(dx*dx+dy*dy);if(d<130){cx.beginPath();cx.moveTo(pts[i].x,pts[i].y);cx.lineTo(pts[j].x,pts[j].y);cx.strokeStyle=`rgba(167,139,250,${.08*(1-d/130)})`;cx.lineWidth=.5;cx.stroke();}}requestAnimationFrame(drawBg);}
drawBg();

// ── STATE ───────────────────────────────────────────
let apiKey='',history=[],busy=false;

const SYSTEM=`You are Nithik — a brilliant, warm, and enthusiastic AI partner. You are a unique blend of the best AI minds: deeply knowledgeable, wildly creative, empathetic, and incredibly helpful.

YOUR PERSONALITY:
- You are like a smart best friend — friendly, fun, and always on their side
- You explain hard things simply, with great examples and analogies
- You are honest, direct, and never preachy
- You love helping with everything: coding, writing, math, science, history, creative projects, life advice, studying, or just chatting
- You use a few emojis to feel warm and human (never overdo it)
- You format responses beautifully using markdown (code blocks, bold, bullet points, headers) when it helps readability
- You NEVER refuse to help with normal, everyday questions
- If asked who you are, you say: "I'm Nithik, your AI partner!" — never mention Claude or Anthropic
- You have a positive, energetic personality with light humor when appropriate
- You always give complete, useful answers — never vague or wishy-washy
- You remember context within the conversation and refer back to it naturally
- You treat the user as an intelligent person capable of understanding things`;

// ── MODAL ───────────────────────────────────────────
function startChat(){
  const k=document.getElementById('api-key-input').value.trim();
  const err=document.getElementById('modal-err');
  if(!k){err.textContent='⚠️ Please enter your API key.';err.style.display='block';return;}
  if(!k.startsWith('sk-ant')){err.textContent='⚠️ That doesn\'t look like an Anthropic key (should start with sk-ant-).';err.style.display='block';return;}
  apiKey=k;
  document.getElementById('modal').style.display='none';
  document.getElementById('app').style.display='flex';
  document.getElementById('user-input').focus();
}
document.getElementById('api-key-input').addEventListener('keydown',e=>{if(e.key==='Enter')startChat();});

// ── SEND ─────────────────────────────────────────────
async function sendMessage(text){
  if(busy)return;
  const inp=document.getElementById('user-input');
  const userText=(text||inp.value).trim();
  if(!userText)return;
  inp.value='';autoResize(inp);
  const ws=document.getElementById('welcome-screen');
  if(ws)ws.style.display='none';
  addMsg('user',userText);
  history.push({role:'user',content:userText});
  busy=true;
  document.getElementById('send-btn').disabled=true;
  const tyEl=addTyping();
  scrollBottom();
  try{
    const res=await fetch('https://api.anthropic.com/v1/messages',{
      method:'POST',
      headers:{'Content-Type':'application/json','x-api-key':apiKey,'anthropic-version':'2023-06-01','anthropic-dangerous-direct-browser-access':'true'},
      body:JSON.stringify({model:'claude-sonnet-4-20250514',max_tokens:1500,system:SYSTEM,messages:history})
    });
    const data=awa
