<!doctype html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>English for Personal Trainers — Lesson 1 · Andrea</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: "Segoe UI", system-ui, -apple-system, sans-serif;
    background: linear-gradient(160deg, #0b1220 0%, #101b30 60%, #0d1626 100%);
    color: #e2e8f0;
    min-height: 100vh;
    line-height: 1.5;
  }
  .wrap { max-width: 940px; margin: 0 auto; padding: 20px 16px 90px; }

  /* ---------- header ---------- */
  header.top { margin-bottom: 6px; }
  .brand { font-size: 1.35rem; font-weight: 800; letter-spacing: .3px; }
  .brand .accent { color: #84cc16; }
  .lesson { color: #94a3b8; font-size: .92rem; margin-top: 2px; }
  .bar { display: flex; align-items: center; justify-content: space-between; gap: 10px; flex-wrap: wrap; margin-top: 14px; }
  #dots { display: flex; gap: 6px; flex-wrap: wrap; }
  .dot {
    border: 1px solid #2e4160; background: #141f35; color: #9fb0c8;
    font-size: .78rem; padding: 5px 11px; border-radius: 999px; cursor: pointer;
    transition: all .15s;
  }
  .dot:hover { border-color: #84cc16; color: #e2e8f0; }
  .dot.active { background: #84cc16; color: #0b1220; font-weight: 700; border-color: #84cc16; }
  .dot.done { border-color: #4d7c0f; color: #bef264; }
  .dot.done.active { background: #84cc16; color: #0b1220; }
  .score-pill {
    background: #141f35; border: 1px solid #2e4160; border-radius: 999px;
    padding: 5px 14px; font-weight: 700; font-size: .9rem; white-space: nowrap;
  }
  .score-pill span { color: #84cc16; }

  /* ---------- slides ---------- */
  .slide { display: none; animation: fade .35s ease; }
  .slide.active { display: block; }
  @keyframes fade { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; transform: none; } }
  .kicker {
    display: inline-block; font-size: .72rem; font-weight: 800; letter-spacing: 1.5px;
    color: #f59e0b; text-transform: uppercase; margin-bottom: 6px;
  }
  h1 { font-size: 1.7rem; line-height: 1.25; margin-bottom: 10px; }
  h2 { font-size: 1.3rem; margin-bottom: 8px; }
  p.lead { color: #b8c5d8; margin-bottom: 14px; }
  .card {
    background: #141f35; border: 1px solid #24344f; border-radius: 16px;
    padding: 18px 20px; margin-top: 14px;
  }
  .it { color: #94a3b8; font-style: italic; }

  /* ---------- cover ---------- */
  .goal-box {
    border-left: 4px solid #84cc16; padding: 12px 16px; background: rgba(132,204,22,.07);
    border-radius: 0 12px 12px 0; margin: 14px 0;
  }
  .steps { display: grid; grid-template-columns: repeat(auto-fit, minmax(160px, 1fr)); gap: 10px; margin-top: 14px; }
  .step { background: #141f35; border: 1px solid #24344f; border-radius: 12px; padding: 12px; text-align: center; }
  .step .n { display: inline-block; width: 26px; height: 26px; border-radius: 50%; background: #84cc16; color: #0b1220; font-weight: 800; line-height: 26px; margin-bottom: 6px; }
  .step .t { font-size: .88rem; font-weight: 700; }
  .step .d { font-size: .78rem; color: #94a3b8; }

  /* ---------- vocab ---------- */
  .vocab-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(270px, 1fr)); gap: 12px; margin-top: 14px; }
  .vcard { background: #141f35; border: 1px solid #24344f; border-radius: 14px; padding: 16px; display: flex; flex-direction: column; gap: 7px; }
  .vword { font-size: 1.15rem; font-weight: 800; color: #84cc16; }
  .vpron { color: #7c8ea8; font-size: .82rem; }
  .vit { font-size: .85rem; color: #fbbf24; }
  .vdef { font-size: .92rem; }
  .vex { font-size: .9rem; background: rgba(132,204,22,.08); border: 1px dashed #3f5a22; border-radius: 9px; padding: 8px 11px; margin-top: auto; }
  .vex::before { content: "💬 "; }
  .vtip { font-size: .8rem; color: #fca5a5; }

  /* ---------- exercises ---------- */
  .bank { display: flex; gap: 8px; flex-wrap: wrap; margin: 12px 0 18px; }
  .word {
    background: #1c2b47; color: #e2e8f0; border: 1px solid #3b5176; border-radius: 999px;
    padding: 7px 16px; font-size: .95rem; font-weight: 700; cursor: pointer; transition: all .15s;
  }
  .word:hover { border-color: #84cc16; }
  .word.used { opacity: .3; pointer-events: none; }
  .gap-sent { font-size: 1.05rem; margin: 14px 0 3px; }
  .gap-sent .num { display: inline-flex; width: 22px; height: 22px; border-radius: 50%; background: #24344f; color: #9fb0c8; font-size: .75rem; font-weight: 700; align-items: center; justify-content: center; margin-right: 8px; }
  .blank {
    display: inline-block; min-width: 120px; text-align: center; padding: 1px 10px;
    border-bottom: 3px dashed #5b7089; cursor: pointer; color: #fbbf24; font-weight: 700;
  }
  .blank:hover { border-color: #f59e0b; }
  .blank.active { border-color: #f59e0b; background: rgba(245,158,11,.15); border-radius: 6px 6px 0 0; }
  .blank.ok { color: #84cc16; border-color: #84cc16; background: rgba(132,204,22,.1); border-radius: 6px 6px 0 0; }
  .blank.ko { color: #f87171; border-color: #f87171; background: rgba(248,113,113,.1); border-radius: 6px 6px 0 0; }
  .hint { font-size: .8rem; color: #94a3b8; margin: 0 0 6px 30px; }
  .btn {
    background: #84cc16; color: #0b1220; border: none; border-radius: 999px;
    padding: 10px 20px; font-size: .95rem; font-weight: 800; cursor: pointer; transition: all .15s;
  }
  .btn:hover { background: #a3e635; }
  .btn.ghost { background: transparent; color: #cbd5e1; border: 1px solid #3b5176; }
  .btn.ghost:hover { border-color: #84cc16; color: #fff; background: transparent; }
  .btn.small { padding: 7px 14px; font-size: .82rem; }
  .btn:disabled { opacity: .4; cursor: default; }
  .fb { border-radius: 12px; padding: 12px 16px; margin-top: 14px; font-size: .95rem; display: none; }
  .fb.show { display: block; animation: fade .25s; }
  .fb.good { background: rgba(132,204,22,.1); border: 1px solid #4d7c0f; }
  .fb.bad { background: rgba(248,113,113,.08); border: 1px solid #7f1d1d; }

  /* ---------- word order ---------- */
  .pool, .answerline { display: flex; flex-wrap: wrap; gap: 8px; align-items: center; }
  .answerline {
    min-height: 58px; border: 2px dashed #2e4160; border-radius: 12px; padding: 10px 12px; margin-top: 12px;
  }
  .answerline.ok { border-color: #84cc16; background: rgba(132,204,22,.06); }
  .tile {
    background: #1c2b47; border: 1px solid #3b5176; color: #e2e8f0; border-radius: 10px;
    padding: 8px 14px; font-size: .95rem; font-weight: 700; cursor: pointer; transition: all .15s;
  }
  .tile:hover { border-color: #84cc16; }
  .tile.punct { border: none; background: transparent; font-size: 1.2rem; padding: 8px 2px; }
  .counter { font-size: .8rem; color: #94a3b8; }

  /* ---------- role play ---------- */
  .chat { display: flex; flex-direction: column; gap: 10px; margin-top: 14px; }
  .bubble { max-width: 82%; padding: 11px 15px; border-radius: 16px; font-size: .97rem; }
  .bubble.client { align-self: flex-start; background: #334155; border-bottom-left-radius: 4px; }
  .bubble.client b { color: #fbbf24; }
  .bubble.trainer { align-self: flex-end; background: #1a2e05; border: 1px solid #65a30d; border-bottom-right-radius: 4px; }
  .opts { display: flex; flex-direction: column; gap: 9px; margin-top: 16px; }
  .opt {
    text-align: left; background: #1c2b47; color: #e2e8f0; border: 1px solid #3b5176;
    border-radius: 12px; padding: 12px 16px; font-size: .95rem; cursor: pointer; transition: all .15s;
  }
  .opt:hover { border-color: #84cc16; background: #22345a; }
  .opt.wrong { border-color: #f87171; background: rgba(248,113,113,.08); opacity: .5; pointer-events: none; }
  .typing { color: #94a3b8; font-style: italic; font-size: .85rem; align-self: flex-start; }

  /* ---------- final summary ---------- */
  .finalbox { border: 1px solid #65a30d; background: rgba(132,204,22,.07); border-radius: 16px; padding: 20px; margin-top: 16px; }
  .finalbox h3 { margin-bottom: 6px; }
  .results { display: grid; grid-template-columns: repeat(auto-fit, minmax(150px,1fr)); gap: 10px; margin: 14px 0; }
  .res { background: #141f35; border: 1px solid #24344f; border-radius: 12px; padding: 12px; text-align: center; }
  .res .v { font-size: 1.3rem; font-weight: 800; color: #84cc16; }
  .res .l { font-size: .78rem; color: #94a3b8; }

  /* ---------- footer ---------- */
  footer.nav {
    position: fixed; left: 0; right: 0; bottom: 0; background: rgba(11,18,32,.92);
    border-top: 1px solid #24344f;
    display: flex; justify-content: center; padding: 12px 16px;
  }
  footer.nav .inner { display: flex; gap: 12px; align-items: center; max-width: 940px; width: 100%; justify-content: space-between; }
  .pageinfo { color: #7c8ea8; font-size: .85rem; }
  .done-badge { display: inline-block; background: rgba(132,204,22,.12); border: 1px solid #4d7c0f; color: #bef264; font-size: .78rem; border-radius: 999px; padding: 3px 10px; margin-top: 10px; }
</style>
</head>
<body>
<div class="wrap">

  <header class="top">
    <div class="brand">🏋️ English for <span class="accent">Personal Trainers</span></div>
    <div class="lesson">Lesson 1 · Talking with a new international client · ~45 min · Teacher: Luca</div>
    <div class="bar">
      <nav id="dots"></nav>
      <div class="score-pill">🏆 <span id="scoreTotal">0</span>/14 points</div>
    </div>
  </header>

  <!-- ============ SLIDE 0 · WELCOME ============ -->
  <section class="slide" id="s0">
    <span class="kicker">Welcome, Andrea! 💪</span>
    <h1>Your first conversation with an international client</h1>
    <p class="lead">You are a great personal trainer. Now let's give your English the same strength — so you can train <b>anyone</b>, not only Italian clients.</p>

    <div class="goal-box">
      <b>🎯 Today's goal:</b> learn 6 key words and use them in a real conversation with a new gym member — from "hello" to "let's book your first session".
      <div class="it">🇮🇹 Obiettivo di oggi: 6 parole chiave e una vera conversazione con un nuovo cliente straniero.</div>
    </div>

    <div class="steps">
      <div class="step"><div class="n">1</div><div class="t">Vocabulary</div><div class="d">6 key words for your job</div></div>
      <div class="step"><div class="n">2</div><div class="t">Fill the gaps</div><div class="d">you read and choose</div></div>
      <div class="step"><div class="n">3</div><div class="t">Build the phrases</div><div class="d">you build full sentences</div></div>
      <div class="step"><div class="n">4</div><div class="t">Role play 🎭</div><div class="d">you talk to a new client</div></div>
    </div>

    <div class="card">
      💡 <b>How to use this lesson:</b> click on the words and answers — everything is interactive! Say every word and every sentence <b>out loud</b>. You are training your English muscles. 🏋️
    </div>
  </section>

  <!-- ============ SLIDE 1 · VOCABULARY ============ -->
  <section class="slide" id="s1">
    <span class="kicker">Slide 1 · Vocabulary</span>
    <h2>6 words you need with a new client</h2>
    <p class="lead">Read each card, say the word out loud 3 times, then click <b>Next</b>.
      <span class="it">🇮🇹 Le traduzioni sono qui per aiutarti — poi ti abituerai a pensare in inglese!</span></p>
    <div class="vocab-grid" id="vocabGrid"></div>
    <div class="card">🔁 <b>Pro tip:</b> the example sentence is what YOU can really say to a new member. Memorize the sentence, not only the word!</div>
  </section>

  <!-- ============ SLIDE 2 · FILL THE GAPS ============ -->
  <section class="slide" id="s2">
    <span class="kicker">Slide 2 · Exercise 1</span>
    <h2>Fill the gaps ✏️</h2>
    <p class="lead">Click a gap, then click the right word from the bank. Check your answers at the end!
      <span class="it">🇮🇹 Clicca sullo spazio vuoto, poi scegli la parola giusta.</span></p>

    <div class="bank" id="gapBank"></div>
    <div id="gapSents"></div>

    <div style="display:flex; gap:10px; flex-wrap:wrap; margin-top:16px;">
      <button class="btn" id="gapCheck">Check answers ✓</button>
      <button class="btn ghost" id="gapReset">Reset</button>
    </div>
    <div class="fb" id="gapFb"></div>
  </section>

  <!-- ============ SLIDE 3 · BUILD THE PHRASES ============ -->
  <section class="slide" id="s3">
    <span class="kicker">Slide 3 · Exercise 2</span>
    <h2>Build the phrases 🧩</h2>
    <p class="lead">Click the words in the correct order to build the sentence — exactly what you will say to a new client.
      <span class="it">🇮🇹 Clicca le parole nell'ordine giusto per formare la frase.</span></p>

    <div class="card" id="orderCard">
      <div class="counter" id="orderCounter"></div>
      <button class="btn ghost small" id="orderHintBtn" style="margin-top:8px;">🇮🇹 Aiuto — show the Italian</button>
      <div class="hint" id="orderHint" style="margin-top:8px; display:none;"></div>
      <div class="answerline" id="orderAnswer"></div>
      <div class="pool" id="orderPool" style="margin-top:14px;"></div>
      <div style="display:flex; gap:10px; flex-wrap:wrap; margin-top:16px;">
        <button class="btn" id="orderCheck">Check ✓</button>
        <button class="btn ghost" id="orderClear">Clear</button>
        <button class="btn ghost" id="orderNext" style="display:none;">Next sentence →</button>
      </div>
      <div class="fb" id="orderFb"></div>
    </div>
    <div class="done-badge" id="orderDone" style="display:none;">✅ Exercise complete — excellent!</div>
  </section>

  <!-- ============ SLIDE 4 · ROLE PLAY ============ -->
  <section class="slide" id="s4">
    <span class="kicker">Slide 4 · Role play — the real thing 🎭</span>
    <h2>A new client is waiting for you…</h2>
    <p class="lead"><b>Tom</b> is a new member from abroad. He wants a personal trainer. Choose the best answer at each turn.
      <span class="it">🇮🇹 Prima prova qui da solo — poi faremo questa conversazione dal vivo nella nostra lezione, con me nei panni di Tom!</span></p>

    <div class="chat" id="chat"></div>
    <div class="opts" id="opts"></div>
    <button class="btn ghost small" id="roleHintBtn" style="margin-top:12px;">🇮🇹 Aiuto</button>
    <div class="hint" id="roleHint" style="margin-top:8px; display:none;"></div>
    <div class="fb" id="roleFb"></div>

    <div class="finalbox" id="finalBox" style="display:none;">
      <h3>🎉 Congratulations, Andrea!</h3>
      <p>You helped Tom — from "hello" to a booked trial session. This is EXACTLY what you will do with your first international client.</p>
      <div class="results" id="finalResults"></div>
      <p style="margin-top:10px;"><b>Next step:</b> in our next lesson we do this conversation <b>live</b> — your teacher will be Tom, and then we swap: YOU play the client too. Ready to unlock your international clients? 💪🌍</p>
      <button class="btn small" id="roleReplay" style="margin-top:12px;">↻ Practice the conversation again</button>
    </div>
  </section>

  <footer class="nav">
    <div class="inner">
      <button class="btn ghost" id="prevBtn">← Back</button>
      <div class="pageinfo" id="pageInfo"></div>
      <button class="btn" id="nextBtn">Next →</button>
    </div>
  </footer>
</div>

<script>
/* ================= DATA ================= */
var VOCAB = [
  { word: "membership", pron: "/ˈmem.bə.ʃɪp/", it: "abbonamento",
    def: "Your gym plan — what you can use and how much you pay.",
    ex: "Your membership includes the gym, the pool and one free session with me." },
  { word: "fitness goals", pron: "/ˈfɪt.nəs ɡəʊlz/", it: "obiettivi di fitness",
    def: "The results you want: lose weight, build muscle, get fit.",
    ex: "What are your fitness goals? Lose weight or build muscle?" },
  { word: "reps", pron: "/reps/", it: "ripetizioni",
    def: "One rep = one complete movement of an exercise.",
    ex: "Do ten reps, then rest for thirty seconds." },
  { word: "sets", pron: "/sets/", it: "serie",
    def: "A set = a group of reps, with a rest in between.",
    ex: "Three sets of ten reps. You can do it!" },
  { word: "strength training", pron: "/streŋθ ˈtreɪ.nɪŋ/", it: "allenamento di forza",
    def: "Training with weights to make your muscles stronger.",
    ex: "Strength training is great for building muscle.",
    tip: "⚠️ \"strength\" is one syllable: /streŋθ/ — a tricky word! We'll practice it together in the lesson." },
  { word: "tailored", pron: "/ˈteɪ.ləd/", it: "su misura",
    def: "Made only for you. A \"tailored plan\" = a personal plan.",
    ex: "I will create a tailored training plan just for you." }
];

var GAP = [
  { pre: "What are your fitness ", post: "? Do you want to lose weight or build muscle?", ans: "goals", hint: "🇮🇹 obiettivi" },
  { pre: "Your ", post: " includes the gym, the pool and one free session with me.", ans: "membership", hint: "🇮🇹 abbonamento" },
  { pre: "Do ten ", post: " of this exercise, then rest.", ans: "reps", hint: "🇮🇹 ripetizioni" },
  { pre: "Three ", post: " of ten reps each. You can do it!", ans: "sets", hint: "🇮🇹 serie" },
  { pre: "With ", post: " training, you use weights to make your muscles stronger.", ans: "strength", hint: "🇮🇹 di forza" },
  { pre: "I will create a ", post: " training plan just for you.", ans: "tailored", hint: "🇮🇹 su misura" }
];

var ORDER = [
  { target: "Would you like to book a free trial session?",
    tiles: ["Would", "you", "like", "to", "book", "a free trial session", "?"],
    hint: "Vuoi prenotare una seduta di prova gratuita?" },
  { target: "What are your fitness goals?",
    tiles: ["What", "are", "your", "fitness", "goals", "?"],
    hint: "Quali sono i tuoi obiettivi di fitness?" },
  { target: "I can create a tailored plan for you.",
    tiles: ["I", "can", "create", "a", "tailored", "plan", "for you", "."],
    hint: "Posso crearti un piano su misura." }
];

var ROLE = [
  { client: "Hi! I'm Tom. I'm new at this gym. I want to train with a personal trainer. Can you help me?",
    hint: "🇮🇹 Dai il benvenuto e presentati!",
    options: [
      { t: "Membership is 80 euros per month.", ok: false,
        fb: "Not yet! First welcome Tom and introduce yourself — prices come later. Prima il benvenuto, i prezzi dopo!" },
      { t: "Yes, of course! Welcome! I'm Andrea, your personal trainer.", ok: true,
        fb: "Perfect! A warm welcome + your name = a great first impression. 🤝" },
      { t: "Sorry, I only train Italian clients.", ok: false,
        fb: "Oh no! 😉 With English, EVERY client is your client. That's exactly why we are here!" }
    ] },
  { client: "Great, thanks! I want to lose some weight and build muscle. Where do I start?",
    hint: "🇮🇹 Usa le parole chiave \"tailored\" e \"fitness goals\"!",
    options: [
      { t: "You must run two hours every day.", ok: false,
        fb: "Too much! A good trainer starts simple with a realistic plan. Un buon trainer parte semplice!" },
      { t: "I don't know, ask at reception.", ok: false,
        fb: "No! Tom chose YOU — you are the expert. Tom ha scelto te: sei tu l'esperto!" },
      { t: "First, we do a small test. Then I create a tailored plan for your fitness goals.", ok: true,
        fb: "Bravissimo! You used \"tailored\" and \"fitness goals\" — two of your six new words! 🎯" }
    ] },
  { client: "Perfect! What does a typical session with you look like?",
    hint: "🇮🇹 Usa \"sets\" e \"reps\" nella risposta!",
    options: [
      { t: "It's a secret!", ok: false,
        fb: "A trainer always explains the session. Mystery is for magicians, not personal trainers! 😉" },
      { t: "First a warm-up. Then strength training: three sets of ten reps. We finish with stretching.", ok: true,
        fb: "Great answer! \"Sets\" and \"reps\" in a real sentence — you sound like a pro! 💪" },
      { t: "Only cardio, every day.", ok: false,
        fb: "Only cardio = no muscles! Tom wants to build muscle, so he needs strength training too." }
    ] },
  { client: "Sounds great! One question: is the membership included in the personal training price?",
    hint: "🇮🇹 Rispondi in modo chiaro e proponi la seduta di prova gratuita!",
    options: [
      { t: "Yes, everything is free!", ok: false,
        fb: "Careful! Be honest about prices — trust is everything with a new client. Sii onesto sui prezzi!" },
      { t: "I don't know, ask at reception.", ok: false,
        fb: "You know your prices! You are the professional here. Conosci i tuoi prezzi!" },
      { t: "No, the membership is separate. But your first personal training session is free!", ok: true,
        fb: "Perfect! A clear answer + a free trial session = a happy client. 🎁" }
    ] },
  { client: "Amazing! OK, I want to start. When can we begin?",
    hint: "🇮🇹 Proponi un giorno e un'ora precisi!",
    options: [
      { t: "Call me sometime.", ok: false,
        fb: "Too vague! Always give a day and a time. Proponi sempre giorno e ora precisi!" },
      { t: "Maybe next month.", ok: false,
        fb: "Too slow! Tom is excited NOW — keep the energy high. ⚡" },
      { t: "Excellent! I'm free on Tuesday at 6 pm. Would you like to book your free trial session?", ok: true,
        fb: "PERFECT! A day, a time, and the magic question. Tom is now YOUR client! 🎉" }
    ] }
];

/* ================= STATE ================= */
var MAX = { gap: GAP.length, order: ORDER.length, role: ROLE.length };
var TOTAL = MAX.gap + MAX.order + MAX.role;
var score = { gap: null, order: null, role: null };
var done = { vocab: false, gap: false, order: false, role: false };
var current = 0;

function $(id) { return document.getElementById(id); }

/* ================= NAVIGATION ================= */
var LABELS = ["👋 Welcome", "📖 Vocabulary", "✏️ Fill the gaps", "🧩 Build phrases", "🎭 Role play"];

function buildDots() {
  var nav = $("dots");
  LABELS.forEach(function (lab, i) {
    var b = document.createElement("button");
    b.className = "dot"; b.textContent = lab; b.onclick = function () { go(i); };
    nav.appendChild(b);
  });
}
function go(i) {
  current = i;
  var slides = document.querySelectorAll(".slide");
  for (var k = 0; k < slides.length; k++) { slides[k].classList.toggle("active", k === i); }
  var dots = document.querySelectorAll(".dot");
  for (var d = 0; d < dots.length; d++) { dots[d].classList.toggle("active", d === i); }
  $("prevBtn").disabled = (i === 0);
  $("nextBtn").style.visibility = (i === LABELS.length - 1) ? "hidden" : "visible";
  $("pageInfo").textContent = "Slide " + (i + 1) + " / " + LABELS.length;
  window.scrollTo(0, 0);
}
function refreshDots() {
  document.querySelectorAll(".dot")[1].classList.toggle("done", done.vocab);
  document.querySelectorAll(".dot")[2].classList.toggle("done", done.gap);
  document.querySelectorAll(".dot")[3].classList.toggle("done", done.order);
  document.querySelectorAll(".dot")[4].classList.toggle("done", done.role);
}
function totalScore() {
  var s = function (x) { return (x === null ? 0 : x); };
  return s(score.gap) + s(score.order) + s(score.role);
}
function updateScorePill() { $("scoreTotal").textContent = totalScore() + " / " + TOTAL; }

/* ================= SLIDE 1 · VOCAB ================= */
function renderVocab() {
  var g = $("vocabGrid");
  g.innerHTML = "";
  VOCAB.forEach(function (v) {
    var c = document.createElement("div");
    c.className = "vcard";
    c.innerHTML =
      '<div class="vword">' + v.word + "</div>" +
      '<div class="vpron">🔊 ' + v.pron + "</div>" +
      '<div class="vit">🇮🇹 ' + v.it + "</div>" +
      '<div class="vdef">' + v.def + "</div>" +
      (v.tip ? '<div class="vtip">' + v.tip + "</div>" : "") +
      '<div class="vex">' + v.ex + "</div>";
    g.appendChild(c);
  });
  done.vocab = true;
  refreshDots();
}

/* ================= SLIDE 2 · GAP FILL ================= */
var gapFilled = [];
var gapChecked = false;
var activeBlank = -1;

function renderGap() {
  var bank = $("gapBank");
  bank.innerHTML = "";
  var words = GAP.map(function (g) { return g.ans; });
  words.sort(function () { return Math.random() - 0.5; });
  words.forEach(function (w) {
    var b = document.createElement("button");
    b.className = "word"; b.textContent = w; b.dataset.word = w;
    b.onclick = function () { placeWord(w); };
    bank.appendChild(b);
  });

  var box = $("gapSents");
  box.innerHTML = "";
  gapFilled = GAP.map(function () { return null; });
  GAP.forEach(function (g, i) {
    var row = document.createElement("div");
    row.className = "gap-sent";
    var blank = document.createElement("span");
    blank.className = "blank"; blank.textContent = "______";
    blank.onclick = function () { selectBlank(i); };
    var num = document.createElement("span");
    num.className = "num"; num.textContent = (i + 1);
    row.appendChild(num);
    row.appendChild(document.createTextNode(g.pre));
    row.appendChild(blank);
    row.appendChild(document.createTextNode(g.post));
    var hint = document.createElement("div");
    hint.className = "hint"; hint.textContent = g.hint;
    box.appendChild(row); box.appendChild(hint);
  });
  gapChecked = false;
  activeBlank = -1;
}
function selectBlank(i) {
  if (gapFilled[i] !== null) {
    var w = gapFilled[i];
    gapFilled[i] = null;
    var bankWords = document.querySelectorAll("#gapBank .word");
    for (var k = 0; k < bankWords.length; k++) {
      if (bankWords[k].dataset.word === w) { bankWords[k].classList.remove("used"); }
    }
  }
  activeBlank = i;
  drawBlanks();
}
function placeWord(w) {
  if (gapFilled.indexOf(w) !== -1) return; // word already used
  var target = activeBlank;
  if (target === -1 || target === null || gapFilled[target] !== null) {
    target = gapFilled.indexOf(null);
  }
  if (target === -1) return;
  gapFilled[target] = w;
  var bankWords = document.querySelectorAll("#gapBank .word");
  for (var k = 0; k < bankWords.length; k++) {
    if (bankWords[k].dataset.word === w) { bankWords[k].classList.add("used"); }
  }
  activeBlank = gapFilled.indexOf(null);
  drawBlanks();
}
function drawBlanks() {
  var blanks = document.querySelectorAll("#gapSents .blank");
  for (var i = 0; i < blanks.length; i++) {
    blanks[i].textContent = (gapFilled[i] === null) ? "______" : gapFilled[i];
    blanks[i].classList.remove("active", "ok", "ko");
    if (i === activeBlank) { blanks[i].classList.add("active"); }
  }
}
function checkGap() {
  var fb = $("gapFb");
  var allFilled = gapFilled.every(function (x) { return x !== null; });
  if (!allFilled) {
    fb.className = "fb bad show";
    fb.innerHTML = "Fill all the gaps first! 🇮🇹 Riempi tutti gli spazi, poi controlla.";
    return;
  }
  var blanks = document.querySelectorAll("#gapSents .blank");
  var ok = 0;
  GAP.forEach(function (g, i) {
    var good = gapFilled[i].toLowerCase().trim() === g.ans;
    blanks[i].classList.add(good ? "ok" : "ko");
    if (good) { ok++; }
  });
  if (!gapChecked) { score.gap = ok; gapChecked = true; }
  if (ok === GAP.length) {
    done.gap = true;
    fb.className = "fb good show";
    fb.innerHTML = "🏆 Perfect! " + ok + "/" + GAP.length + " — all six words in the right place. You are ready for the next step!";
  } else {
    fb.className = "fb bad show";
    fb.innerHTML = "Almost! " + ok + "/" + GAP.length + " correct. Look at the red gaps, try again and check again — practice makes perfect! 🇮🇹 Guarda gli spazi rossi e riprova!";
  }
  refreshDots(); updateScorePill();
}
function resetGap() {
  renderGap();
  $("gapFb").className = "fb";
}

/* ================= SLIDE 3 · WORD ORDER ================= */
var orderIdx = 0;
var orderPlaced = [];
var orderFirstTry = true;
var orderTried = [false, false, false];

function renderOrder() {
  var o = ORDER[orderIdx];
  orderPlaced = []; orderFirstTry = true;
  $("orderHint").style.display = "none";
  $("orderFb").className = "fb";
  $("orderNext").style.display = "none";
  $("orderCounter").textContent = "Sentence " + (orderIdx + 1) + " of " + ORDER.length + (orderTried[orderIdx] ? " ✅ (solved)" : "");
  $("orderAnswer").className = "answerline";
  $("orderAnswer").innerHTML = '<span style="color:#5b7089;font-size:.85rem;">Click the words below to build the sentence…</span>';

  var pool = $("orderPool");
  pool.innerHTML = "";
  var idx = o.tiles.map(function (_, i) { return i; });
  idx.sort(function () { return Math.random() - 0.5; });
  idx.forEach(function (i) {
    var t = document.createElement("button");
    var isPunct = (o.tiles[i] === "?" || o.tiles[i] === ".");
    t.className = "tile" + (isPunct ? " punct" : "");
    t.textContent = o.tiles[i];
    t.onclick = function () { placeTile(i); };
    pool.appendChild(t);
  });
}
function drawAnswer() {
  var o = ORDER[orderIdx];
  var ans = $("orderAnswer");
  ans.innerHTML = "";
  if (orderPlaced.length === 0) {
    ans.innerHTML = '<span style="color:#5b7089;font-size:.85rem;">Click the words below to build the sentence…</span>';
  }
  orderPlaced.forEach(function (ti, p) {
    var isPunct = (o.tiles[ti] === "?" || o.tiles[ti] === ".");
    var t = document.createElement("button");
    t.className = "tile" + (isPunct ? " punct" : "");
    t.textContent = o.tiles[ti];
    t.onclick = function () { removeTile(p); };
    ans.appendChild(t);
  });
  var pool = $("orderPool").children;
  for (var k = 0; k < pool.length; k++) {
    var el = pool[k];
    var txt = el.textContent;
    var same = [];
    for (var j = 0; j < pool.length; j++) { if (pool[j].textContent === txt) { same.push(j); } }
    var usedCount = 0;
    orderPlaced.forEach(function (ti) { if (o.tiles[ti] === txt) { usedCount++; } });
    var pos = same.indexOf(k);
    el.style.display = (pos < usedCount) ? "none" : "";
  }
}
function placeTile(i) {
  orderPlaced.push(i);
  drawAnswer();
}
function removeTile(pos) {
  orderPlaced.splice(pos, 1);
  drawAnswer();
}
function checkOrder() {
  var o = ORDER[orderIdx];
  var fb = $("orderFb");
  if (orderPlaced.length !== o.tiles.length) {
    fb.className = "fb bad show";
    fb.innerHTML = "Use all the words! 🇮🇹 Usa tutte le parole per formare la frase.";
    return;
  }
  var correct = orderPlaced.every(function (v, i) { return v === i; });
  if (correct) {
    $("orderAnswer").classList.add("ok");
    fb.className = "fb good show";
    fb.innerHTML = "✅ \"" + o.target + "\" — perfect sentence! You can say this to a real client tomorrow. 💪";
    if (orderFirstTry && !orderTried[orderIdx]) {
      score.order = (score.order === null ? 0 : score.order) + 1;
    }
    orderTried[orderIdx] = true;
    $("orderCounter").textContent = "Sentence " + (orderIdx + 1) + " of " + ORDER.length + " ✅";
    if (orderIdx < ORDER.length - 1) {
      $("orderNext").style.display = "";
    } else {
      done.order = true;
      $("orderDone").style.display = "";
    }
    updateScorePill(); refreshDots();
  } else {
    fb.className = "fb bad show";
    fb.innerHTML = "Hmm, not the natural order yet. Click a word above to put it back, then try again. And click <b>🇮🇹 Aiuto</b> if you want the Italian! 🇮🇹 Riprova!";
    orderFirstTry = false;
  }
}
function clearOrder() {
  orderPlaced = [];
  drawAnswer();
  $("orderFb").className = "fb";
}

/* ================= SLIDE 4 · ROLE PLAY ================= */
var roleTurn = 0;
var roleScore = 0;
var typingTimer = null;

function bubble(text, who) {
  var b = document.createElement("div");
  b.className = "bubble " + who;
  b.innerHTML = (who === "client" ? "<b>Tom:</b> " : "<b>You:</b> ") + text;
  $("chat").appendChild(b);
  var box = $("chat");
  box.scrollTop = box.scrollHeight;
}
function showTyping() {
  var t = document.createElement("div");
  t.className = "typing"; t.id = "typing";
  t.textContent = "Tom is typing…";
  $("chat").appendChild(t);
}
function renderRoleOpts() {
  var turn = ROLE[roleTurn];
  var box = $("opts");
  box.innerHTML = "";
  var idx = turn.options.map(function (_, i) { return i; });
  idx.sort(function () { return Math.random() - 0.5; });
  idx.forEach(function (i) {
    var o = turn.options[i];
    var b = document.createElement("button");
    b.className = "opt"; b.textContent = o.t;
    b.onclick = function () { pickOption(b, o); };
    box.appendChild(b);
  });
  $("roleHint").style.display = "none";
}
function pickOption(el, o) {
  var fb = $("roleFb");
  if (o.ok) {
    el.style.borderColor = "#84cc16";
    el.style.background = "rgba(132,204,22,.12)";
    fb.className = "fb good show";
    fb.innerHTML = "✓ " + o.fb;
    $("opts").innerHTML = "";
    roleScore++;
    score.role = roleScore;
    bubble(o.t, "trainer");
    updateScorePill();
    roleTurn++;
    if (roleTurn < ROLE.length) {
      showTyping();
      typingTimer = setTimeout(function () {
        var t = document.getElementById("typing");
        if (t) { t.remove(); }
        bubble(ROLE[roleTurn].client, "client");
        renderRoleOpts();
      }, 1200);
    } else {
      finishRole();
    }
  } else {
    el.classList.add("wrong");
    fb.className = "fb bad show";
    fb.innerHTML = "✗ " + o.fb;
  }
}
function finishRole() {
  done.role = true;
  refreshDots(); updateScorePill();
  function fmt(x, m) { return (x === null ? "—" : x + "/" + m); }
  $("finalResults").innerHTML =
    '<div class="res"><div class="v">' + fmt(score.gap, MAX.gap) + '</div><div class="l">✏️ Fill the gaps</div></div>' +
    '<div class="res"><div class="v">' + fmt(score.order, MAX.order) + '</div><div class="l">🧩 Build phrases</div></div>' +
    '<div class="res"><div class="v">' + fmt(score.role, MAX.role) + '</div><div class="l">🎭 Role play</div></div>' +
    '<div class="res"><div class="v">' + totalScore() + "/" + TOTAL + '</div><div class="l">🏆 Total</div></div>';
  $("finalBox").style.display = "";
}
function startRole() {
  roleTurn = 0; roleScore = 0;
  if (typingTimer) { clearTimeout(typingTimer); }
  score.role = null;
  $("chat").innerHTML = "";
  $("finalBox").style.display = "none";
  $("roleFb").className = "fb";
  bubble(ROLE[0].client, "client");
  renderRoleOpts();
  updateScorePill();
}

/* ================= WIRE-UP ================= */
buildDots();
renderVocab();
renderGap();
renderOrder();
startRole();

$("prevBtn").onclick = function () { go(Math.max(0, current - 1)); };
$("nextBtn").onclick = function () { go(Math.min(LABELS.length - 1, current + 1)); };
$("gapCheck").onclick = checkGap;
$("gapReset").onclick = resetGap;
$("orderCheck").onclick = checkOrder;
$("orderClear").onclick = clearOrder;
$("orderNext").onclick = function () { orderIdx++; renderOrder(); };
$("orderHintBtn").onclick = function () {
  var h = $("orderHint");
  h.style.display = "";
  h.innerHTML = "🇮🇹 " + ORDER[orderIdx].hint;
};
$("roleHintBtn").onclick = function () {
  var h = $("roleHint");
  h.style.display = "";
  h.textContent = ROLE[roleTurn].hint;
};
$("roleReplay").onclick = startRole;

go(0);
updateScorePill();
</script>
</body>
</html>
