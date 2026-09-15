<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A Letter That Finds Its Person</title>

<style>
body{
    margin:0;
    background:#0f1020;
    color:white;
    font-family:Georgia, serif;
    overflow:hidden;
}

.page{
    display:none;
    height:100vh;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    text-align:center;
    padding:25px;
}

.active{
    display:flex;
}

button{
    margin-top:25px;
    padding:12px 28px;
    border:none;
    border-radius:30px;
    font-size:16px;
    cursor:pointer;
}

.stars{
    position:fixed;
    inset:0;
    background:
    radial-gradient(circle at 20% 30%, white 1px, transparent 2px),
    radial-gradient(circle at 70% 20%, white 1px, transparent 2px),
    radial-gradient(circle at 40% 80%, white 1px, transparent 2px),
    radial-gradient(circle at 90% 60%, white 1px, transparent 2px);
    animation:twinkle 4s infinite;
}

@keyframes twinkle{
    50%{opacity:.5}
}

.name{
    font-size:3rem;
    animation:fadeIn 2s ease;
}

@keyframes fadeIn{
    from{opacity:0;transform:translateY(20px)}
    to{opacity:1;transform:translateY(0)}
}

.heart{
    font-size:40px;
    animation:float 2s infinite alternate;
}

@keyframes float{
    from{transform:translateY(0)}
    to{transform:translateY(-15px)}
}
</style>
</head>
<body>

<div class="stars"></div>

<div id="p1" class="page active">
    <h1>🌙 A Letter Was Found</h1>
    <p>
        A message was written long ago...
        <br>
        but it never reached the right person.
    </p>
    <button onclick="show(2)">Find the Owner</button>
</div>

<div id="p2" class="page">
    <h1>✉️ Dear Stranger</h1>
    <p>
        If you're reading this,
        I need your help.
        <br><br>
        I'm looking for someone special.
    </p>
    <button onclick="show(3)">Tell Me More</button>
</div>

<div id="p3" class="page">
    <h2>Does this person have a beautiful smile?</h2>
    <button onclick="show(4)">Yes 😊</button>
    <button onclick="show(4)">Maybe 😄</button>
</div>

<div id="p4" class="page">
    <h2>Does this person make people happy?</h2>
    <button onclick="show(5)">Yes ❤️</button>
    <button onclick="show(5)">Definitely Yes ✨</button>
</div>

<div id="p5" class="page">
    <h2>Is this person worth celebrating today?</h2>
    <button onclick="show(6)">Yes 🎉</button>
    <button onclick="show(6)">Of Course 🎂</button>
</div>

<div id="p6" class="page">
    <div class="heart">❤️</div>

    <p>
        After searching everywhere...
        <br>
        I finally found the right person.
    </p>

    <div class="name">✨ RACHANA ✨</div>

    <h1>🎂 Happy Birthday 🎂</h1>

    <p style="max-width:600px">
        May your smile stay bright,
        your dreams stay big,
        and your happiness grow every day.
        <br><br>
        Thank you for being such a wonderful person.
    </p>
</div>

<script>
function show(n){
    document.querySelectorAll(".page")
    .forEach(p=>p.classList.remove("active"));

    document.getElementById("p"+n)
    .classList.add("active");
}
</script>

</body>
</html>
