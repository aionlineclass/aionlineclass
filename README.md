<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AI Academy | Online Class Registration</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif}
body{background:#f5f7fb;color:#222}
header{background:linear-gradient(135deg,#0b3d91,#0d6efd);color:#fff;padding:80px 20px;text-align:center}
header h1{font-size:46px;margin-bottom:20px}
header p{font-size:20px;max-width:760px;margin:auto;line-height:1.8}
.btn{display:inline-block;margin-top:30px;padding:15px 40px;background:#fff;color:#0b3d91;text-decoration:none;border-radius:40px;font-weight:600}
.btn:hover{background:#ffc107;color:#000}
section{max-width:1100px;margin:auto;padding:60px 20px}
.title{text-align:center;color:#0b3d91;font-size:34px;margin-bottom:35px}
.cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:20px}
.card{background:#fff;padding:25px;border-radius:12px;box-shadow:0 6px 16px rgba(0,0,0,.08)}
.features{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:15px}
.feature{background:#fff;padding:18px;border-left:5px solid #0d6efd;border-radius:10px;box-shadow:0 4px 10px rgba(0,0,0,.06)}
.cta{background:#0b3d91;color:#fff;text-align:center;padding:70px 20px}
footer{background:#081b45;color:#fff;text-align:center;padding:20px}

/* chatbot */
#chatButton{position:fixed;bottom:20px;right:20px;width:60px;height:60px;border-radius:50%;background:#0d6efd;color:#fff;display:flex;align-items:center;justify-content:center;font-size:28px;cursor:pointer;box-shadow:0 6px 16px rgba(0,0,0,.3)}
#chatContainer{display:none;flex-direction:column;position:fixed;bottom:90px;right:20px;width:340px;height:470px;background:#fff;border-radius:15px;overflow:hidden;box-shadow:0 8px 25px rgba(0,0,0,.25)}
#chatHeader{background:#0b3d91;color:#fff;padding:15px;font-weight:600}
#close{float:right;cursor:pointer}
#chatMessages{flex:1;padding:12px;background:#f3f5f7;overflow-y:auto}
.bot,.user{padding:10px 12px;border-radius:12px;margin:8px 0;max-width:85%}
.bot{background:#e6e6e6}
.user{background:#0d6efd;color:#fff;margin-left:auto}
#inputArea{display:flex;border-top:1px solid #ddd}
#inputArea input{flex:1;border:none;padding:12px;outline:none}
#inputArea button{border:none;background:#0d6efd;color:#fff;width:60px;cursor:pointer}
</style>
</head>
<body>

<header>
<h1>Artificial Intelligence Academy</h1>
<p>Empowering students with future-ready skills in Artificial Intelligence, Python Programming, Data Science, Machine Learning and Big Data Analytics through live interactive online classes.</p>
<a class="btn" target="_blank" href="https://forms.gle/QqkkB47D7GgsWZV26">Register Now</a>
</header>

<section>
<h2 class="title">Our Courses</h2>
<div class="cards">
<div class="card"><h3>Artificial Intelligence</h3><p>AI with practical projects and real-world applications.</p></div>
<div class="card"><h3>Python Programming</h3><p>Learn Python from beginner to advanced with hands-on coding.</p></div>
<div class="card"><h3>Data Science</h3><p>Data analysis, visualization and machine learning.</p></div>
</div>
</section>

<section>
<h2 class="title">Why Choose Us?</h2>
<div class="features">
<div class="feature">✅ Live Interactive Classes</div>
<div class="feature">✅ Recorded Sessions</div>
<div class="feature">✅ Practical Coding</div>
<div class="feature">✅ Study Materials</div>
<div class="feature">✅ Doubt Clearing</div>
<div class="feature">✅ Beginner Friendly</div>
</div>
</section>

<section class="cta">
<h2>Start Your AI Journey Today</h2>
<p>Complete the registration form to reserve your seat.</p>
<a class="btn" target="_blank" href="https://forms.gle/QqkkB47D7GgsWZV26">Register for Online Classes</a>
</section>

<footer>© 2026 Artificial Intelligence Academy. All Rights Reserved.</footer>

<div id="chatButton" onclick="toggleChat()">💬</div>

<div id="chatContainer">
<div id="chatHeader">🤖 AI Assistant <span id="close" onclick="toggleChat()">✖</span></div>
<div id="chatMessages">
<div class="bot">👋 Welcome! Ask me about Courses, Fees, Registration, Python, AI or Contact.</div>
</div>
<div id="inputArea">
<input id="userInput" placeholder="Type your question...">
<button onclick="sendMessage()">➤</button>
</div>
</div>

<script>
function toggleChat(){
const c=document.getElementById('chatContainer');
c.style.display=(c.style.display==='flex')?'none':'flex';
}
function add(text,cls){
const d=document.createElement('div');
d.className=cls;
d.innerHTML=text;
const m=document.getElementById('chatMessages');
m.appendChild(d);
m.scrollTop=m.scrollHeight;
}
function reply(q){

q = q.toLowerCase().trim();

// Greetings
if(
q.includes("hi") ||
q.includes("hello") ||
q.includes("hey") ||
q.includes("good morning") ||
q.includes("good afternoon") ||
q.includes("good evening")
){
return `👋 Hello! Welcome to <b>Artificial Intelligence Academy</b>.<br><br>

I'm here to help you.<br><br>

You can ask me about:
<ul style="margin:8px 0 0 20px;">
<li>📘 Courses</li>
<li>💰 Fees</li>
<li>📝 Registration</li>
<li>🐍 Python</li>
<li>🤖 AI</li>
<li>📅 Class Timings</li>
<li>📞 Contact Details</li>
</ul>`;
}

// How are you
if(
q.includes("how are you") ||
q.includes("how r u")
){
return "😊 I'm doing great! Thank you for asking. How can I help you today?";
}

// About Academy
if (
    q.includes("about") ||
    q.includes("academy") ||
    q.includes("institute") ||
    q.includes("who are you")
) {
    return `
    🏫 <b>Artificial Intelligence Academy</b> provides live online classes in:

    <ul style="margin-top:10px; padding-left:20px;">
        <li>🤖 Artificial Intelligence</li>
        <li>🐍 Python Programming</li>
        <li>📊 Data Science</li>
        <li>🧠 Machine Learning</li>
        <li>📈 Big Data Analytics</li>
    </ul>

    <p>✅ Our classes are beginner-friendly and practical.</p>
    `;
}

// Courses
if (
    q.includes("course") ||
    q.includes("courses") ||
    q.includes("training") ||
    q.includes("learn")
) {
    return `
    <b>📚 We currently offer:</b>

    <ul style="margin:10px 0 10px 20px; padding-left:15px;">
        <li>🤖 Artificial Intelligence</li>
        <li>🐍 Python Programming</li>
        <li>📊 Data Science</li>
    </ul>

    <b>❓ Which course would you like to know more about?</b>
    `;
}

// AI
if (
    q.includes("artificial intelligence") ||
    q === "ai" ||
    q.includes("machine learning")
) {
    return `
    <b>🤖 AI Course includes:</b>

    <ul style="margin:10px 0 10px 20px; padding-left:15px;">
        <li>✅ AI Fundamentals</li>
        <li>✅ Machine Learning</li>
        <li>✅ Deep Learning Basics</li>
        <li>✅ Generative AI</li>
        <li>✅ Computer Vision</li>
        <li>✅ Natural Language Processing (NLP)</li>
    </ul>

    <b>🎓 Suitable for beginners and students.</b>
    `;
}

// Data Science
if (
    q.includes("data science") ||
    q.includes("analytics")
) {
    return `📊 Data Science Course includes:

✔ Data Analysis
✔ Data Visualization
✔ Machine Learning Basics
✔ Statistics
✔ Python for Data Science
✔ Pandas & NumPy
✔ Real-Time Projects

🎓 Suitable for beginners and students.`;
}

// Fees
if (
    q.includes("fee") ||
    q.includes("fees") ||
    q.includes("cost") ||
    q.includes("price")
) {
    return `💰 Fee Details

✔ Affordable course fees
✔ Easy payment options available
✔ Special discounts for students (if applicable)

📞 Contact us: +91 9100060289

💬 Please contact us to know the latest fee details.`;
}


// Registration
if (
    q.includes("register") ||
    q.includes("registration") ||
    q.includes("join") ||
    q.includes("admission") ||
    q.includes("enroll")
) {
    return `📝 Registration Process

✔ Click the "Register Now" button on this page.
✔ Fill in the registration form.
✔ Submit your details.
✔ Our team will contact you shortly.
✔ Complete the fee payment to confirm your admission.

📞 Need help? Contact us: +91 9100060289`;
}

// Timing
if (
    q.includes("timing") ||
    q.includes("time") ||
    q.includes("schedule") ||
    q.includes("batch")
) {
    return `🕒 Class Timings

✔ Morning Batch
✔ Evening Batch
✔ Weekend Batch
✔ Live Online Interactive Classes
✔ Recorded Sessions Available

📅 Contact us to know the current batch schedule.

📞 Phone: +91 9100060289`;
}

// Duration
if (
    q.includes("duration") ||
    q.includes("how long")
) {
    return `⏳ Course Duration

✔ Duration: 2 to 3 Months
✔ Live Online Interactive Classes
✔ Practical Hands-on Sessions
✔ Flexible Morning & Evening Batches
✔ Recorded Sessions Available

📞 For more details, contact us on WhatsApp:
+91 9100060289`;
}
// Online Classes
if (
    q.includes("online") ||
    q.includes("offline")
) {
    return `💻 Online Classes

✔ 100% Live Online Interactive Classes
✔ Learn from Anywhere
✔ Recorded Sessions Available
✔ Practical Hands-on Training
✔ Live Doubt Clearing Sessions
✔ Beginner-Friendly Teaching
✔ Study Materials Provided

📞 Contact us for batch details:
+91 9100060289`;
}

// Beginner
if (
    q.includes("beginner") ||
    q.includes("experience") ||
    q.includes("new")
) {
    return `😊 Beginner-Friendly Course

✔ No prior programming knowledge required
✔ Step-by-step teaching approach
✔ Easy-to-understand concepts
✔ Live practical coding sessions
✔ Doubt clearing support
✔ Recorded classes for revision
✔ Real-world projects for practice
✔ Suitable for School Students, College Students & Working Professionals

🎓 Start your AI journey with confidence!

📞 Contact us: +91 9100060289`;
}

// Recorded Classes
if (
    q.includes("record") ||
    q.includes("recording")
) {
    return `🎥 Recorded Sessions

✔ All live classes are recorded
✔ Watch anytime, anywhere
✔ Revise lessons multiple times
✔ Never miss a class
✔ Access recordings after each session
✔ Learn at your own pace

📞 Contact us: +91 9100060289`;
}


// Contact
if (
    q.includes("contact") ||
    q.includes("phone") ||
    q.includes("number") ||
    q.includes("mobile") ||
    q.includes("email")
) {
    return `📞 Contact Us

✔ Phone Number
   +91 9100060289

✔ WhatsApp
   +91 9100060289

✔ Website
   www.aionlineclass.in

✔ Email
   aionlineclass2k26@gmail.com

😊 Feel free to contact us for:
✔ Course Details
✔ Registration
✔ Fee Information
✔ Batch Timings`;
}

// Thanks
if(
q.includes("thank") ||
q.includes("thanks")
){
return "😊 You're welcome! Feel free to ask anything about our academy.";
}

// Bye
if(
q.includes("bye") ||
q.includes("see you")
){
return "👋 Thank you for visiting Artificial Intelligence Academy. Have a wonderful day!";
}

// Default
return `🤔 Sorry, I couldn't understand your question.

Try asking:

<ul>
<li>AI Course</li>
<li>Python Course</li>
<li>Data Science</li>
<li>Fees</li>
<li>Registration</li>
<li>Batch Timings</li>
<li>Duration</li>
<li>Contact Details</li>
`;
}function sendMessage(){
const i=document.getElementById('userInput');
const t=i.value.trim();
if(!t) return;
add(t,'user');
i.value='';
setTimeout(()=>add(reply(t),'bot'),400);
}
document.getElementById('userInput').addEventListener('keydown',e=>{
 if(e.key==='Enter') sendMessage();
});
</script>
</body>
</html>
