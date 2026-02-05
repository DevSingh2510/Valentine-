<Hello>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Be My Valentine 💖</title>

<style>
    body {
        background: linear-gradient(135deg, #ff758c, #ff7eb3);
        font-family: 'Arial', sans-serif;
        height: 100vh;
        margin: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        overflow: hidden;
    }

    .card {
        background: white;
        width: 85%;
        max-width: 350px;
        padding: 30px 20px;
        border-radius: 20px;
        text-align: center;
        box-shadow: 0 15px 30px rgba(0,0,0,0.2);
    }

    h1 {
        color: #e91e63;
        font-size: 22px;
        margin-bottom: 30px;
        line-height: 1.4;
    }

    .buttons {
        position: relative;
        height: 120px;
    }

    button {
        padding: 14px 26px;
        font-size: 18px;
        border-radius: 30px;
        border: none;
        cursor: pointer;
    }

    #yes {
        background-color: #e91e63;
        color: white;
    }

    #no {
        background-color: #ddd;
        color: #333;
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        top: 60px;
    }
</style>
</head>

<body>

<div class="card">
    <h1>Astha 💕<br>Will you be my Valentine?</h1>

    <div class="buttons">
        <button id="yes" onclick="yesClicked()">YES 💖</button>
        <button id="no">NO 🙈</button>
    </div>
</div>

<script>
    const noBtn = document.getElementById("no");

    function moveButton() {
        const x = Math.random() * (window.innerWidth - 100);
        const y = Math.random() * (window.innerHeight - 100);
        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    }

    // For mobile touch
    noBtn.addEventListener("touchstart", moveButton);
    // For desktop fallback
    noBtn.addEventListener("mouseover", moveButton);

    function yesClicked() {
        document.body.innerHTML = `
            <div style="
                display:flex;
                justify-content:center;
                align-items:center;
                height:100vh;
                background:linear-gradient(135deg,#ff9a9e,#fad0c4);
                font-family:Arial;
                text-align:center;
                padding:20px;
            ">
                <h1 style="color:#e91e63;">
                    YAYYYY 💖💖💖<br><br>
                    See you on our Valentine date 😘
                </h1>
            </div>
        `;
    }
</script>

</body>
</html>
