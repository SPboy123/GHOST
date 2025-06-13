# GHOST
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Chat</title>
    <style>
        body { font-family: Arial, sans-serif; padding: 20px; }
        #chat { height: 300px; overflow-y: auto; border: 1px solid #ccc; padding: 10px; }
        #messageInput { width: 80%; padding: 5px; }
        button { padding: 6px; }
    </style>
</head>
<body>
    <h2>Simple Chat</h2>
    <div id="chat"></div>
    <input id="messageInput" type="text" placeholder="Type a message...">
    <button onclick="sendMessage()">Send</button>

    <script>
        function sendMessage() {
            const input = document.getElementById('messageInput');
            const chat = document.getElementById('chat');

            if (input.value.trim()) {
                const message = document.createElement('p');
                message.textContent = input.value;
                chat.appendChild(message);

                input.value = '';
                chat.scrollTop = chat.scrollHeight;
            }
        }
    </script>
</body>
</html>
