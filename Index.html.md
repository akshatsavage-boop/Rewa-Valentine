#   
<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8" />  
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>  
  <title>Be My Valentine ❤️</title>  
  
  <style>  
    body {  
      margin: 0;  
      font-family: 'Arial', sans-serif;  
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);  
      display: flex;  
      justify-content: center;  
      align-items: center;  
      height: 100vh;  
      color: #333;  
    }  
  
    .card {  
      background: white;  
      border-radius: 20px;  
      padding: 30px;  
      text-align: center;  
      max-width: 320px;  
      width: 90%;  
      box-shadow: 0 20px 40px rgba(0,0,0,0.2);  
    }  
  
    h1 {  
      color: #6ee7b7;  
      margin-bottom: 15px;  
    }  
  
    img {  
      width: 120px;  
      margin: 15px 0;  
    }  
  
    .question {  
      font-size: 18px;  
      margin-bottom: 20px;  
      color: #e11d48;  
    }  
  
    .buttons {  
      display: flex;  
      justify-content: center;  
      gap: 15px;  
    }  
  
    button {  
      border: none;  
      border-radius: 10px;  
      padding: 12px 20px;  
      font-size: 18px;  
      cursor: pointer;  
      transition: all 0.3s ease;  
    }  
  
    .yes-button {  
      background: #ec4899;  
      color: white;  
    }  
  
    .no-button {  
      background: #e5e7eb;  
      color: #111827;  
    }  
  </style>  
</head>  
  
<body>  
  <div class="card">  
    <h1>Be My Valentine 💚</h1>  
  
    <img src="https://i.imgur.com/9YzZ1nL.png" alt="Cute Bear"/>  
  
    <div class="question">  
      Will you be my Valentine, Rewa? 💕  
    </div>  
  
    <div class="buttons">  
      <button class="yes-button" onclick="handleYesClick()">Yes</button>  
      <button class="no-button" onclick="handleNoClick()">No</button>  
    </div>  
  </div>  
  
  <script>  
    const messages = [  
      "Are you sure? 🥺",  
      "Pookie please 🥹",  
      "Think again 😢",  
      "Don’t break my heart 💔",  
      "Last chance 😭"  
    ];  
  
    let messageIndex = 0;  
  
    function handleNoClick() {  
      const noButton = document.querySelector('.no-button');  
      const yesButton = document.querySelector('.yes-button');  
  
      noButton.textContent = messages[messageIndex];  
      messageIndex = (messageIndex + 1) % messages.length;  
  
      const currentSize = parseFloat(  
        window.getComputedStyle(yesButton).fontSize  
      );  
  
      yesButton.style.fontSize = (currentSize * 1.3) + "px";  
    }  
  
    function handleYesClick() {  
      document.body.innerHTML = `  
        <div style="  
          display:flex;  
          flex-direction:column;  
          justify-content:center;  
          align-items:center;  
          height:100vh;  
          background:linear-gradient(135deg,#f472b6,#ec4899);  
          color:white;  
          text-align:center;  
          font-family:Arial;  
        ">  
          <h1>YAYYY!!! 💖🥰</h1>  
          <p style="font-size:20px;">  
            Best Valentine ever ❤️  
          </p>  
        </div>  
      `;  
    }  
  </script>  
</body>  
</html>  
