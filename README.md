<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Babygirl 💖</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ff6f91, #ffb6c1);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: "Arial Rounded MT Bold", Arial, sans-serif;
      text-align: center;
      overflow: hidden;
    }

    .card {
      background: white;
      padding: 28px;
      border-radius: 28px;
      width: 90%;
      max-width: 380px;
      box-shadow: 0 15px 40px rgba(0,0,0,0.25);
      animation: pop 0.8s ease;
    }

    @keyframes pop {
      from { transform: scale(0.7); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }

    h1 { color: #ff4d6d; margin-bottom: 10px; }
    p { font-size: 17px; line-height: 1.5; margin: 12px 0; }
    h2 { color: #ff4d6d; margin-top: 18px; }

    button {
      width: 100%;
      padding: 15px;
      margin-top: 12px;
      border: none;
      border-radius: 40px;
      font-size: 18px;
      cursor: pointer;
    }

    #yes { background: #ff4d6d; color: white; }
    #no { background: #f2f2f2; }

    .heart {
      position: fixed;
      bottom: -20px;
      color: #ff4d6d;
      animation: floatUp 4s linear forwards;
    }

    @keyframes floatUp {
      to { transform: translateY(-120vh); opacity: 0; }
    }
  </style>
</head>

<body>

  <div class="card" id="card">
    <h1>Hey Babygirl 🥹💖</h1>

    <p>
      Being with you has been the best thing to happen to me in this life,  
      you made me the happiest man in the world and I’ll forever love you for that.  
      Which is why I want to use this moment to ask you this:
    </p>

    <p>
      I feel sad that we won’t be able to celebrate this Valentine the proper way because of the distance,  
      but I promise you the next one I’ll make it all up to you.  
      I still hope your answer is yes tho 🥲
    </p>

    <h2>Would you be my Valentine? 💘</h2>

    <button id="yes" onclick="yes()">Yes 💖</button>
    <button id="no" onclick="no()">No 🙈</button>
  </div>

  <script>
    function yes() {
      // WhatsApp message and your number
      const number = "08123751827";
      const message = encodeURIComponent(
        "Yes daddy😍❤️ I’ll be your Valentine! you made me the happiest woman alive 💕"
      );

      document.getElementById("card").innerHTML = `
        <h1>YAY!!! 💕🥰</h1>
        <p>
          Babygirl, you just made my heart so happy ❤️<br>
          I can’t wait to celebrate us in person someday 💘
        </p>
      `;

      for (let i = 0; i < 30; i++) setTimeout(createHeart, i * 120);

      // Open WhatsApp directly to your chat
      setTimeout(() => {
        window.location.href = "https://wa.me/" + number + "?text=" + message;
      }, 1300);
    }

    function no() {
      const lines = [
        "Hey… try again 😌",
        "Think about it, Babygirl 🥹",
        "I made this just for you 🥺",
        "You know you want to 💕"
      ];
      alert(lines[Math.floor(Math.random() * lines.length)]);
    }

    function createHeart() {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.innerHTML = "❤️";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = Math.random() * 22 + 18 + "px";
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 4000);
    }
  </script>

</body>
</html>
