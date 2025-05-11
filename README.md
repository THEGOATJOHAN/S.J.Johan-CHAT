<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>S.J.Johan - Personal Site</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: #f0f2f5;
      color: #333;
    }
    header {
      background-color: #4a76a8;
      color: white;
      padding: 1rem;
      text-align: center;
    }
    main {
      max-width: 800px;
      margin: 2rem auto;
      padding: 1rem;
      background: white;
      border-radius: 8px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }
    .chat-box {
      border: 1px solid #ccc;
      border-radius: 10px;
      padding: 1rem;
      max-height: 400px;
      overflow-y: auto;
      background: #e5e5ea;
    }
    .message {
      background-color: #ffffff;
      border-radius: 15px;
      padding: 0.5rem 1rem;
      margin: 0.5rem 0;
      max-width: 70%;
    }
    .from-user {
      background-color: #0084ff;
      color: white;
      margin-left: auto;
    }
    .input-group {
      display: flex;
      margin-top: 1rem;
    }
    input[type="text"] {
      flex: 1;
      padding: 0.5rem;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    button {
      padding: 0.5rem 1rem;
      margin-left: 0.5rem;
      background: #4a76a8;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <header>
    <h1>Welcome to S.J.Johan's Site</h1>
    <p>Personal Portfolio & Contact</p>
  </header>
  <main>
    <h2>Contact Me</h2>
    <div class="chat-box" id="chatBox">
      <div class="message">Hi! You can send me a message here.</div>
    </div>
    <div class="input-group">
      <input type="text" id="userInput" placeholder="Type your message..." />
      <button onclick="sendMessage()">Send</button>
    </div>
  </main>

  <script>
    function sendMessage() {
      const input = document.getElementById('userInput');
      const messageText = input.value.trim();
      if (!messageText) return;

      const chatBox = document.getElementById('chatBox');
      const userMessage = document.createElement('div');
      userMessage.className = 'message from-user';
      userMessage.textContent = messageText;
      chatBox.appendChild(userMessage);

      input.value = '';
      chatBox.scrollTop = chatBox.scrollHeight;
    }
  </script>

  <!-- Tidio Live Chat Script -->
  <script src="//code.tidio.co/wzsrvtc78azq6qbffqz6uzm601mj3nlz.js" async></script>
</body>
</html>
