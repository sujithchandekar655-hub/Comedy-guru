# Comedy-guru
Free Stand-up Comedy Learning Academy
from pathlib import Path

html = r'''<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#171323">
<title>Comedy Guru — Lessons 1–5</title>
<style>
:root{--bg:#100e18;--panel:#211c2c;--panel2:#2b2339;--text:#fff;--muted:#c8bed5;--accent:#c49aff;--line:#433650}
*{box-sizing:border-box}body{margin:0;background:var(--bg);color:var(--text);font:16px/1.65 system-ui,Arial,sans-serif;padding-bottom:32px}
header{padding:20px 16px;background:#1c1729;position:sticky;top:0;z-index:3;border-bottom:1px solid var(--line)}
.logo{font-size:24px;font-weight:900;color:var(--accent)}.sub{font-size:12px;color:var(--muted)}
main{max-width:760px;margin:auto;padding:16px}
.hero,.card{background:var(--panel);border:1px solid var(--line);border-radius:16px;padding:17px;margin:14px 0}
.hero{background:linear-gradient(135deg,#56358c,#241b39)}
h1{font-size:26px;line-height:1.25;margin:5px 0 10px}h2{font-size:22px;margin:6px 0 10px}h3{font-size:17px;margin:12px 0 5px}
p{margin:7px 0}.muted{color:var(--muted);font-size:14px}.tag{color:var(--accent);font-size:12px;font-weight:800;letter-spacing:.06em}
button{font:inherit;font-weight:700;color:white;background:#8053bc;border:0;border-radius:10px;padding:11px 14px;cursor:pointer}
button.secondary{background:#393047}button.lessonBtn{width:100%;text-align:left;background:var(--panel);border:1px solid var(--line);margin:7px 0;padding:14px}
input,textarea,select{width:100%;font:inherit;color:white;background:#171323;border:1px solid #514363;border-radius:10px;padding:12px;margin:6px 0}
textarea{min-height:100px}label{font-weight:700;font-size:14px}
details{background:var(--panel2);border-radius:11px;padding:12px;margin:10px 0;border:1px solid var(--line)}
summary{font-weight:800;cursor:pointer;color:#e5d4ff}
section.lesson{display:none}section.lesson.active{display:block}
.example{border-left:3px solid var(--accent);padding:9px 12px;margin:10px 0;background:#191522;border-radius:0 9px 9px 0}
.grid{display:grid;grid-template-columns:1fr;gap:8px}
.notice{padding:12px;border-radius:10px;background:#302743;color:#e6d9f4;font-size:13px}
.progress{height:8px;background:#51445f;border-radius:10px;overflow:hidden}.progress span{display:block;height:100%;width:0;background:var(--accent)}
.smallbtn{font-size:13px;padding:8px 10px}
@media(min-width:620px){.grid{grid-template-columns:1fr 1fr}main{padding:22px}}
</style>
</head>
<body>
<header><div class="logo">🎤 COMEDY GURU</div><div class="sub">LEARN • WRITE • PERFORM — HINGLISH + TELGLISH</div></header>
<main>
<div class="hero">
 <div class="tag">COMEDY WRITING ACADEMY • MODULE 01</div>
 <h1>Learn the craft behind the laugh.</h1>
 <p>In these lessons, comedy ko sirf “funny line” nahi samjhenge. Hum thinking process, joke construction, rewriting aur practice seekhenge.</p>
 <div class="progress"><span id="progressBar"></span></div><p class="muted" id="progressText">0 / 5 lessons completed</p>
</div>
<div id="lessonMenu">
 <h2>Lessons 1–5</h2>
 <button class="lessonBtn" onclick="openLesson(0)">01 · Observation Comedy <span class="muted">— Material notice karna</span></button>
 <button class="lessonBtn" onclick="openLesson(1)">02 · Exaggeration <span class="muted">— Reality ko stretch karna</span></button>
 <button class="lessonBtn" onclick="openLesson(2)">03 · Contrast <span class="muted">— Opposites se humour</span></button>
 <button class="lessonBtn" onclick="openLesson(3)">04 · Association <span class="muted">— Idea connections</span></button>
 <button class="lessonBtn" onclick="openLesson(4)">05 · Setup & Punchline <span class="muted">— Joke architecture</span></button>
</div>

<section class="lesson" id="l0">
<button class="secondary smallbtn" onclick="back()">← All lessons</button>
<div class="card"><span class="tag">LESSON 01 · FOUNDATION</span><h1>Observation Comedy</h1><p class="muted">Goal: daily life se relatable comedy material dhoondhna.</p></div>
<div class="card"><h2>1. Concept samjho</h2>
<p><b>Hinglish:</b> Observation comedy mein comedian normal life ki details notice karta hai—habits, contradictions, awkward moments, rules, reactions aur chhoti frustrations. Sirf “ye hua” likhna observation hai; “is mein interesting ya funny angle kya hai?” poochna writing ka start hai.</p>
<p><b>Tenglish:</b> Daily life lo jarige chinna details, habits, awkward moments ni observe cheyadam. Tarvata “indulo unusual point enti?” ani adigi comedy angle develop cheyadam.</p>
<div class="example"><b>Raw observation:</b> Exam ke ek din pehle student suddenly timetable banata hai.<br><b>Possible premise:</b> Student ka timetable padhai se zyada guilt manage karta hai.</div></div>
<div class="card"><h2>2. Technical process: Observation → Premise</h2>
<ol><li><b>Notice:</b> Kya hua? Specific detail likho.</li><li><b>Interpret:</b> Is behavior ke peeche ka reason/contradiction kya ho sakta hai?</li><li><b>Angle:</b> Apna point of view choose karo.</li><li><b>Premise:</b> Ek sentence mein comedy idea state karo.</li><li><b>Test:</b> Kya audience apni life se connect kar sakti hai?</li></ol>
<div class="notice">Writing tip: General statement “students lazy hain” weak hai. Specific detail “student alarm ko snooze karte hue apne future ko bhi snooze karta hai” zyada writable hai.</div></div>
<div class="card"><h2>3. Observation lenses</h2>
<details open><summary>Contradiction</summary><p>Log jo kehte hain aur jo karte hain usmein gap.</p><div class="example">“Main phone kam use karta hoon” bolkar screen-time report ko bina dekhe dismiss karna.</div></details>
<details><summary>Specific detail</summary><p>Broad topic ke bajaye recognizable tiny detail.</p><div class="example">Exam hall mein pen ke saath extra 3 pens le jaana, jaise pen nahi emergency team ho.</div></details>
<details><summary>Social rule</summary><p>Unwritten rules jo sab follow karte hain, par koi explain nahi karta.</p><div class="example">Family function mein “bas 5 minute mein nikalte hain” ka matlab sabko pata hai.</div></details>
<details><summary>Emotional truth</summary><p>Situation ke andar asli feeling: embarrassment, jealousy, pride, fear, relief.</p><div class="example">Online “seen” ke baad reply ka wait karna—phone nahi, apni self-respect refresh kar rahe hote hain.</div></details></div>
<div class="card"><h2>4. Joke examples + breakdown</h2>
<div class="example"><b>Example:</b> “Mere ghar mein exam se pehle sab motivational speaker ban jaate hain. Paper mera hota hai, lekin pressure poore family ka group project.”</div>
<p><b>Breakdown:</b> Observation: family exam pressure. Angle: individual exam ko group project banana. Technique: analogy + relatable exaggeration. Punch: “group project” reframes the family dynamic.</p>
<div class="example"><b>Example:</b> “Ghar wale kehte hain phone side mein rakho. Phir wahi phone se meri marksheet ka photo poore relatives ko bhejte hain.”</div>
<p><b>Breakdown:</b> Contradiction—phone bad when student uses it, useful when family uses it. The humor comes from the reversal, not from a random insult.</p></div>
<div class="card"><h2>5. Common mistakes</h2><ul><li>Topic ko joke samajhna: “college funny hai” abhi premise nahi.</li><li>Too general likhna; specific behavior add karo.</li><li>Dusre comedian ka exact joke copy karna.</li><li>Har line ko punchline banana; honest setup aur clear point bhi zaroori hai.</li><li>Audience ko context na dena.</li></ul></div>
<div class="card"><h2>6. Practice assignment</h2><p>3 everyday observations likho: home, college/work, phone/social media. Har observation se ek premise banao.</p><label>Observation 1 + premise</label><textarea id="p0a" placeholder="What happened? What's the unusual angle?"></textarea><label>Observation 2 + premise</label><textarea id="p0b"></textarea><label>Observation 3 + premise</label><textarea id="p0c"></textarea><button onclick="savePractice(0)">Save practice</button> <button class="secondary" onclick="complete(0)">Mark lesson complete</button></div>
</section>

<section class="lesson" id="l1">
<button class="secondary smallbtn" onclick="back()">← All lessons</button>
<div class="card"><span class="tag">LESSON 02 · COMEDY ENGINE</span><h1>Exaggeration</h1><p class="muted">Goal: ek real idea ko bigger, more intense, or absurd banana—without losing its connection to the truth.</p></div>
<div class="card"><h2>1. Concept</h2><p><b>Hinglish:</b> Exaggeration mein real feeling ya situation ko scale, duration, consequence ya reaction mein bada karte hain. Audience ko original truth pehchanna chahiye; tab exaggeration relatable rehta hai.</p><p><b>Tenglish:</b> Nijamaina situation ni size, intensity, time, consequence lo athiga penchadam. Original feeling audience ki connect avvali.</p><div class="example">Truth: Exam se pehle stress hota hai.<br>Exaggeration: “Exam paper dekha toh mere dimaag ne resignation letter submit kar diya.”</div></div>
<div class="card"><h2>2. Four technical types</h2>
<details open><summary>Scale exaggeration</summary><p>Small thing ko huge bana do.</p><div class="example">“Mummy ka ek ‘idhar aao’ sunke poora ghar courtroom ban jaata hai.”</div></details>
<details><summary>Duration exaggeration</summary><p>Time ko absurdly long/short present karo.</p><div class="example">“Uska reply itna late aaya, tab tak mera phone nahi—relationship ka archaeological record ban gaya.”</div></details>
<details><summary>Consequence escalation</summary><p>Small action ke consequences step-by-step escalate karo.</p><div class="example">Snooze → late → attendance miss → teacher call → ghar mein family meeting.</div></details>
<details><summary>Emotional exaggeration</summary><p>Inner feeling ko dramatic external event ki tarah describe karo.</p><div class="example">“Wi-Fi gaya toh ghar mein aisa silence tha jaise sabne ek saath meditation retreat join kiya.”</div></details></div>
<div class="card"><h2>3. Escalation ladder</h2><p>Build 3–4 steps. Har step previous se bigger ho aur same premise ko serve kare.</p><div class="example">1. Main exam se nervous tha.<br>2. Pen check kiya.<br>3. 4 pens le gaya.<br>4. Ek pen ko emotional support ke liye front bench pe bithaya.</div><p><b>Mechanics:</b> pattern + rising stakes + final surprising image. Sirf random bigger words se escalation nahi banti.</p></div>
<div class="card"><h2>4. Example breakdown</h2><div class="example">“Mera alarm itna ignore hota hai, ab woh bajne se pehle hi apni resignation mail draft karta hoga.”</div><p>Reality: alarm repeatedly ignored. Personification: alarm gets human job behavior. Exaggeration: resignation. Punch word/image: “resignation mail.”</p><div class="example">“Meri diet Monday se start hoti hai. Monday aata hai, diet ko main next Monday ka appointment de deta hoon.”</div><p>Technique: delay pattern + personification/appointment framing. Relatable self-contradiction.</p></div>
<div class="card"><h2>5. Common mistakes</h2><ul><li>Random absurdity without recognizable truth.</li><li>Too many exaggerations in one sentence; focus the punch.</li><li>Escalation steps don't connect to the premise.</li><li>Repeating “bahut zyada” instead of creating a vivid image.</li></ul></div>
<div class="card"><h2>6. Practice</h2><p>Choose one: late waking, exam stress, slow internet. Create a 3-step escalation and one final punchline.</p><label>Your escalation + punchline</label><textarea id="p1a"></textarea><label>What truth makes it relatable?</label><textarea id="p1b"></textarea><button onclick="savePractice(1)">Save practice</button> <button class="secondary" onclick="complete(1)">Mark lesson complete</button></div>
</section>

<section class="lesson" id="l2">
<button class="secondary smallbtn" onclick="back()">← All lessons</button>
<div class="card"><span class="tag">LESSON 03 · COMEDY ENGINE</span><h1>Contrast</h1><p class="muted">Goal: two different realities, expectations, identities, or behaviors ko juxtapose karke comic tension banana.</p></div>
<div class="card"><h2>1. Concept</h2><p><b>Hinglish:</b> Contrast tab kaam karta hai jab audience ek cheez expect kare aur saamne uska opposite ya mismatch aaye. Difference clear aur meaningful hona chahiye.</p><p><b>Tenglish:</b> Oka expectation ki opposite result, leka rendu mismatched situations ni pakkana pettadam valla humour create avuthundi.</p><div class="example">Expectation: “Main gym jaake fit banunga.”<br>Reality: “Gym membership card wallet mein fit ho gaya; main abhi bhi same.”</div></div>
<div class="card"><h2>2. Contrast types</h2>
<details open><summary>Expectation vs reality</summary><p>Audience anticipated result ko actual result se compare karti hai.</p><div class="example">“New year resolution: early rise. Reality: alarm aur main dono snooze ke supporters.”</div></details>
<details><summary>Words vs action</summary><p>Character kuch claim karta hai, behavior usko contradict karta hai.</p><div class="example">“Main drama se door hoon”—phir 11-minute voice note bhejna.</div></details>
<details><summary>Status mismatch</summary><p>Grand role or language vs tiny practical reality.</p><div class="example">“Main ghar ka financial advisor hoon. Meri advice: salary aate hi balance mat dekho.”</div></details>
<details><summary>Scale / setting mismatch</summary><p>Small situation ko grand context mein ya grand situation ko tiny context mein rakhna.</p><div class="example">“Meri study table par aaj international peace summit tha—book, phone aur main decide kar rahe the kaun pehle khulega.”</div></details></div>
<div class="card"><h2>3. Technical structure</h2><ol><li>Set the first side clearly (belief, promise, image).</li><li>Let audience form an expectation.</li><li>Introduce the second side that clashes with it.</li><li>Make the mismatch specific; cut extra explanation.</li></ol><div class="notice">Contrast aur misdirection related hain, same nahi: contrast is the mismatch; misdirection is the audience’s expectation being guided one way, then redirected.</div></div>
<div class="card"><h2>4. Example breakdown</h2><div class="example">“Instagram pe sab ‘living my best life’ likhte hain. Main ‘battery 3%, data khatam, ghar ka Wi-Fi password yaad nahi’ ke saath living my real life.”</div><p>Contrast: curated online image vs practical daily problems. Detail makes the contrast recognizable.</p><div class="example">“Papa bolte hain paisa tree pe nahi ugta. Lekin unka salary day pe mood aisa hota hai jaise orchard ka harvest aa gaya.”</div><p>Contrast: stated principle vs celebratory behavior. Use only if this fits the speaker’s lived experience.</p></div>
<div class="card"><h2>5. Common mistakes</h2><ul><li>Two unrelated things side by side without a clear mismatch.</li><li>Explaining the contrast after the audience already understands it.</li><li>Making the “reality” predictable or not surprising.</li><li>Using a comparison that does not reveal a point of view.</li></ul></div>
<div class="card"><h2>6. Practice</h2><p>Write two lines: “People think…” and “Actually…” Then turn the difference into one concise joke.</p><label>People think…</label><textarea id="p2a"></textarea><label>Actually…</label><textarea id="p2b"></textarea><label>My joke</label><textarea id="p2c"></textarea><button onclick="savePractice(2)">Save practice</button> <button class="secondary" onclick="complete(2)">Mark lesson complete</button></div>
</section>

<section class="lesson" id="l3">
<button class="secondary smallbtn" onclick="back()">← All lessons</button>
<div class="card"><span class="tag">LESSON 04 · IDEA GENERATION</span><h1>Association</h1><p class="muted">Goal: one thought se connected ideas nikaalna, phir unexpected but understandable connection se comedy material banana.</p></div>
<div class="card"><h2>1. Concept</h2><p><b>Hinglish:</b> Association ka matlab ek word, situation, emotion ya object se related next ideas dhoondhna. Comedy tab banti hai jab chain ko surprising direction mein le jaate ho—lekin connection audience ko samajh aaye.</p><p><b>Tenglish:</b> Oka word/situation nundi related ideas chain create cheyadam. Tarvata unexpected direction lo connect chesi funny angle build cheyadam.</p><div class="example">Exam → marks → career → salary → family expectations. Ab premise: “Mera exam paper ghar mein career planning meeting ka agenda ban jaata hai.”</div></div>
<div class="card"><h2>2. Association map: 5 routes</h2>
<details open><summary>Literal association</summary><p>Object ke obvious functions/parts.</p><div class="example">Phone → battery → charging → power bank → “friend who always asks for charger.”</div></details>
<details><summary>Emotional association</summary><p>Situation se related feeling.</p><div class="example">Seen message → anxiety → checking online status → self-appointed detective.</div></details>
<details><summary>Social association</summary><p>People, roles, rules, relationships.</p><div class="example">Family function → relatives → questions → job/marriage interview.</div></details>
<details><summary>Word association</summary><p>Sound, phrase, double meaning—context and clarity matter.</p><div class="example">“Deadline” → line → queue; build a fresh connection, not merely rhyme.</div></details>
<details><summary>Remote association</summary><p>Jump farther away, then find a bridge back to the original topic.</p><div class="example">Exam → courtroom → judge → verdict. “Result day ghar mein judge bhi papa, lawyer bhi mummy, accused bhi main.”</div></details></div>
<div class="card"><h2>3. Technical method: Chain, bridge, punch</h2><ol><li>Write starting topic.</li><li>Make 10 quick associations without judging.</li><li>Circle an unexpected branch.</li><li>Build a bridge: explain mentally why it connects.</li><li>Choose one clear premise and write a punch.</li></ol><div class="notice">Important: Association is an idea-generation tool. A chain alone is not a finished joke; it needs a point of view, structure and a clear ending.</div></div>
<div class="card"><h2>4. Example breakdown</h2><div class="example">“Mummy ne marks pooche. Marks se career, career se salary, salary se shaadi. Mere result ka syllabus mujhse zyada mummy ko pata hai.”</div><p>Chain: marks → career → salary → marriage. Final line compresses the chain into a surprising perspective.</p><div class="example">“Friend ne bola ‘bro, gym join kar.’ Main soch raha tha: gym → trainer → diet → groceries → cooking. Fitness se pehle mujhe ek full-time operations manager chahiye.”</div><p>Association chain becomes a relatable premise about the hidden work around a goal.</p></div>
<div class="card"><h2>5. Common mistakes</h2><ul><li>Associations are too random, no bridge.</li><li>Writing the first obvious connection only.</li><li>Explaining every link aloud, making joke slow.</li><li>Confusing brainstorming with the final punchline.</li></ul></div>
<div class="card"><h2>6. Practice</h2><p>Starting word: “Phone”. Make a chain of 8 links, circle the most unexpected link, then write a 1–2 line joke.</p><label>Your association chain</label><textarea id="p3a"></textarea><label>Your final joke</label><textarea id="p3b"></textarea><button onclick="savePractice(3)">Save practice</button> <button class="secondary" onclick="complete(3)">Mark lesson complete</button></div>
</section>

<section class="lesson" id="l4">
<button class="secondary smallbtn" onclick="back()">← All lessons</button>
<div class="card"><span class="tag">LESSON 05 · JOKE ARCHITECTURE</span><h1>Setup & Punchline</h1><p class="muted">Goal: audience ko clear context dena, expectation create karna, phir unexpected but logical reveal dena.</p></div>
<div class="card"><h2>1. The parts of a joke</h2><p><b>Premise:</b> The central idea or point of view.</p><p><b>Setup:</b> Context that makes the audience understand the situation and forms an expectation.</p><p><b>Misdirection:</b> Audience ko ek likely direction mein guide karna, then redirect karna.</p><p><b>Punchline:</b> The reveal/reversal that delivers the comic idea.</p><p><b>Tag:</b> An e
