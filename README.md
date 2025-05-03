<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday!</title>
  <style>
    body {
      background: black;
      color: white;
      text-align: center;
      font-family: 'Comic Sans MS', cursive;
      padding: 50px;
    }
    h1 {
      font-size: 3em;
    }
    .balloons {
      font-size: 2em;
      animation: float 2s ease-in-out infinite;
    }
    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-20px); }
      100% { transform: translateY(0); }
    }
    button {
      padding: 10px 20px;
      font-size: 1em;
      background: white;
      color: black;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      margin-top: 30px;
    }
    .cake {
      position: relative;
      width: 200px;
      margin: 30px auto;
    }
    .cake img {
      width: 100%;
      display: block;
    }
    .flame {
      position: absolute;
      width: 10px;
      height: 20px;
      background: orange;
      border-radius: 50% 50% 0 0;
      animation: flicker 0.2s infinite;
      top: -20px;
    }
    .flame:nth-child(2) { left: 40px; }
    .flame:nth-child(3) { left: 90px; }
    .flame:nth-child(4) { left: 140px; }

    @keyframes flicker {
      0% { transform: scaleY(1); opacity: 1; }
      50% { transform: scaleY(1.2); opacity: 0.8; }
      100% { transform: scaleY(1); opacity: 1; }
    }

    .hidden {
      display: none;
    }

    #messageBox {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0, 0, 0, 0.8);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 999;
    }

    .modal {
      background: white;
      color: black;
      padding: 20px;
      border-radius: 20px;
      max-width: 90%;
      text-align: left;
      font-size: 1.1em;
      box-shadow: 0 0 20px #fff;
    }

    .modal button {
      margin-top: 15px;
      padding: 8px 15px;
      font-size: 1em;
      border: none;
      border-radius: 10px;
      background: black;
      color: white;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Happy Birthday mam!</h1>
  <div class="balloons">🎈🎉🎂🎁</div>
  <p>You're a molecule of awesomeness, bonded with kindness and love..💕</p>

  <div class="cake">
    <div class="flame" id="flame1"></div>
    <div class="flame" id="flame2"></div>
    <div class="flame" id="flame3"></div>
    <img src="https://i.imgur.com/7KXU43P.png" alt="Birthday Cake">
  </div>

  <button onclick="blowCandles()">Click for a Surprise</button>

  <div id="messageBox" class="hidden">
    <div class="modal">
      <p>
        She's so cute.<br>
        She's so beautiful.<br>
        Her smile is pure magic.<br>
        Her eyes shine like stars.<br>
        She laughs like a child.<br>
        She talks so sweetly.<br>
        She walks with grace.<br>
        Her vibe is peaceful.<br>
        She's soft like a rose.<br>
        She looks like a dream.<br>
        Her presence feels warm.<br>
        She lights up the room.<br>
        She makes people happy.<br>
        She cares from the heart.<br>
        She's real and raw.<br>
        She's special, truly one of a kind..<br>
        She's just... wow.......<br>
        And she is you 🥹💕
      </p>
      <button onclick="closeMessage()">Close</button>
    </div>
  </div>

  <script>
    function blowCandles() {
      document.getElementById('flame1').classList.add('hidden');
      document.getElementById('flame2').classList.add('hidden');
      document.getElementById('flame3').classList.add('hidden');

      setTimeout(() => {
        document.getElementById('messageBox').classList.remove('hidden');
      }, 1200);
    }

    function closeMessage() {
      document.getElementById('messageBox').classList.add('hidden');
    }
  </script>
</body>
</html>
