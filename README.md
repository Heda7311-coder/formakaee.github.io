# formakaee.github.io
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Letter from Kae</title>
<style>
  body {
    margin: 0;
    background: linear-gradient(to bottom, #0b1b29, #081018);
    font-family: 'Georgia', serif;
    color: #f1f5f9;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    padding: 20px;
  }
  .paper {
    background: #fffaf3;
    color: #222;
    padding: 24px;
    border-radius: 10px;
    max-width: 600px;
    width: 100%;
    box-shadow: 0 6px 20px rgba(0,0,0,0.3);
    font-size: 18px;
    line-height: 1.6;
    white-space: pre-wrap;
    overflow-y: auto;
    max-height: 80vh;
  }
  .highlight {
    display: block;
    margin-top: 20px;
    font-weight: bold;
    font-size: 20px;
    color: #ff4d6d;
    text-align: center;
    animation: glow 1.5s ease-in-out infinite alternate;
  }
  @keyframes glow {
    from { text-shadow: 0 0 5px #ff4d6d; }
    to { text-shadow: 0 0 15px #ff99aa; }
  }
  .btn {
    margin-top: 14px;
    padding: 8px 14px;
    background: #ff4d6d;
    border: none;
    color: white;
    border-radius: 6px;
    cursor: pointer;
    font-weight: bold;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .btn:hover {
    filter: brightness(1.1);
  }
</style>
</head>
<body>
<div>
  <div class="paper" id="letter"></div>
  <button class="btn" id="replayBtn" style="display:none;">Replay Letter</button>
</div>

<script>
  const letterEl = document.getElementById('letter');
  const replayBtn = document.getElementById('replayBtn');

  const letterText = `hi madam makaeee,

I realize now how much I’ve missed u ett maybe i choose the wrong path i also MISS the laughter and the late night talks huhu, I'll always choose you, like a tulip seeks the sun.
I can’t pretend anymore dili nako kaya. You’ve always been there in my heart, no matter what i do to distract myself i always think about u
So here I am, ready to return, ready to make it right. I told u na mobalik ko dibaa diba we promised to each other na magbalik japon if whatever happens please comeback na give me 1 more chance lovey

\u2764\uFE0F PLEASE BALIK NA LAST CHANCE HANGYO NANI ET HEHEEHEHHEHEHE.`;

  let index = 0;
  let typingSpeed = 45;

  function typeLetter() {
    if (index < letterText.length) {
      letterEl.innerHTML += letterText.charAt(index);
      index++;
      setTimeout(typeLetter, typingSpeed);
    } else {
      const finalMsg = document.createElement('span');
      finalMsg.className = 'highlight';
      finalMsg.textContent = "PLEASE PLEASE HANGYO NANI NI DUTDUT HEHE ❤️";
      letterEl.appendChild(finalMsg);
      replayBtn.style.display = 'block';
    }
  }

  replayBtn.addEventListener('click', () => {
    letterEl.textContent = "";
    index = 0;
    replayBtn.style.display = 'none';
    typeLetter();
  });

  typeLetter();
</script>
</body>
</html>

