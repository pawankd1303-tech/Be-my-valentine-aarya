
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Be My Valentine 💘</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: 'Comic Sans MS', cursive, sans-serif;
    }

    .card {
      background: white;
      padding: 40px 60px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      position: relative;
    }

    h1 {
      color: #e6005c;
      margin-bottom: 30px;
    }

    button {
      padding: 12px 25px;
      font-size: 18px;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      margin: 10px;
    }

    #yesBtn {
      background: #ff4d6d;
      color: white;
    }

    #noBtn {
      background: #999;
      color: white;
      position: absolute;
    }
  </style>
</head>
<body>

  <div class="card" id="card">
    <h1>Will you be my Valentine? 💖</h1>
    <button id="yesBtn" onclick="yesClicked()">Yes 💕</button>
    <button id="noBtn">No 🙃</button>
  </div>

  <script>
    const noBtn = document.getElementById("noBtn");
    const card = document.getElementById("card");

    // initial position
    noBtn.style.left = "60%";
    noBtn.style.top = "70%";

    noBtn.addEventListener("mouseover", moveButton);

    function moveButton() {
      const cardRect = card.getBoundingClientRect();
      const btnRect = noBtn.getBoundingClientRect();

      const maxX = cardRect.width - btnRect.width;
      const maxY = cardRect.height - btnRect.height;

      const x = Math.random() * maxX;
      const y = Math.random() * maxY;

      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }

    function yesClicked() {
      document.body.innerHTML = `
        <div style="
          height:100vh;
          display:flex;
          justify-content:center;
          align-items:center;
          background:linear-gradient(135deg,#ff758c,#ff7eb3);
          font-family:'Comic Sans MS', cursive;
          color:white;
          text-align:center;
        ">
          <h1>Yayyy! 💕🥰<br>You just made my Valentine perfect 💘</h1>
        </div>
      `;
    }
  </script>

</body>
</html>
If you want, I can:
Add hearts animation 💗
Add background music 🎵
Make it mobile-perfect
Personalize with her name & inside joke
Just say the word 😉
