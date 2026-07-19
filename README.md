/* ===========================
   AI Academy - Modern CSS
=========================== */

@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap');

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Poppins',sans-serif;
    scroll-behavior:smooth;
}

body{
    background:linear-gradient(135deg,#07162b,#0b3d91,#0d6efd);
    color:#fff;
    overflow-x:hidden;
}

/* Navigation */

nav{
    width:100%;
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:20px 10%;
    position:fixed;
    top:0;
    left:0;
    backdrop-filter:blur(15px);
    background:rgba(0,0,0,.25);
    z-index:1000;
}

.logo{
    font-size:30px;
    font-weight:700;
    color:#fff;
}

nav ul{
    display:flex;
    gap:30px;
    list-style:none;
}

nav ul li a{
    color:white;
    text-decoration:none;
    transition:.3s;
}

nav ul li a:hover{
    color:#00e5ff;
}

/* Hero */

.hero{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:100px 20px;
}

.hero-content{
    max-width:900px;
}

.hero h1{
    font-size:60px;
    font-weight:700;
    margin-bottom:20px;
}

.hero span{
    color:#00e5ff;
}

.hero p{
    font-size:20px;
    line-height:1.8;
    color:#ddd;
}

/* Buttons */

.btn{
    display:inline-block;
    margin-top:40px;
    padding:18px 45px;
    text-decoration:none;
    color:white;
    font-size:18px;
    font-weight:600;
    border-radius:50px;
    background:linear-gradient(45deg,#00c6ff,#0072ff);
    transition:.4s;
    box-shadow:0 10px 25px rgba(0,0,0,.3);
}

.btn:hover{
    transform:translateY(-5px);
    box-shadow:0 20px 35px rgba(0,0,0,.4);
}

/* Sections */

section{
    padding:90px 10%;
}

.section-title{
    text-align:center;
    font-size:40px;
    margin-bottom:60px;
}

/* Cards */

.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:30px;
}

.card{
    background:rgba(255,255,255,.08);
    backdrop-filter:blur(20px);
    border:1px solid rgba(255,255,255,.15);
    border-radius:20px;
    padding:35px;
    transition:.4s;
}

.card:hover{
    transform:translateY(-10px);
    box-shadow:0 20px 40px rgba(0,0,0,.35);
}

.card h3{
    margin-bottom:15px;
    color:#00e5ff;
}

.card p{
    color:#ddd;
    line-height:1.8;
}

/* Features */

.feature{
    display:flex;
    align-items:center;
    gap:15px;
    margin-bottom:18px;
    background:rgba(255,255,255,.08);
    padding:18px;
    border-radius:15px;
}

.feature i{
    font-size:28px;
}

/* CTA */

.cta{
    text-align:center;
    padding:100px 20px;
}

.cta h2{
    font-size:45px;
    margin-bottom:20px;
}

.cta p{
    color:#ddd;
    margin-bottom:30px;
}

/* Footer */

footer{
    background:#02111f;
    text-align:center;
    padding:25px;
    color:#bbb;
}

/* Floating WhatsApp */

.whatsapp{
    position:fixed;
    bottom:25px;
    right:25px;
    width:65px;
    height:65px;
    background:#25D366;
    color:white;
    border-radius:50%;
    display:flex;
    justify-content:center;
    align-items:center;
    text-decoration:none;
    font-size:32px;
    box-shadow:0 10px 25px rgba(0,0,0,.4);
    transition:.3s;
}

.whatsapp:hover{
    transform:scale(1.1);
}

/* Scrollbar */

::-webkit-scrollbar{
    width:8px;
}

::-webkit-scrollbar-thumb{
    background:#00c6ff;
    border-radius:20px;
}

/* Responsive */

@media(max-width:768px){

.hero h1{
    font-size:38px;
}

.hero p{
    font-size:17px;
}

nav{
    padding:15px 20px;
}

nav ul{
    display:none;
}

.section-title{
    font-size:32px;
}

}
