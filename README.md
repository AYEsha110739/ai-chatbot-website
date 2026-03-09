<!DOCTYPE html>
<html>
<head>
<title>AI Chat</title>

<style>
body{
font-family: Arial;
text-align:center;
margin-top:40px;
}

#chatbox{
width:300px;
height:300px;
border:1px solid #ccc;
margin:auto;
overflow:auto;
padding:10px;
}

input{
width:200px;
padding:10px;
}

button{
padding:10px;
}
</style>
</head>

<body>

<h2>AI Chat Bot</h2>

<div id="chatbox"></div>

<br>

<input type="text" id="userInput" placeholder="Ask something...">
<button onclick="sendMessage()">Send</button>

<script>

function sendMessage(){

let input = document.getElementById("userInput").value;

let chat = document.getElementById("chatbox");

chat.innerHTML += "<p><b>You:</b> " + input + "</p>";

let reply = "I don't understand.";

if(input.toLowerCase().includes("hello"))
reply="Hello! How can I help you?";

if(input.toLowerCase().includes("name"))
reply="I am a simple AI chatbot.";

if(input.toLowerCase().includes("time"))
reply="Check your system time.";

chat.innerHTML += "<p><b>Bot:</b> " + reply + "</p>";

document.getElementById("userInput").value="";
}

</script>

</body>
</html># ai-chatbot-website
Simple AI chatbot website using HTML, CSS, and JavaScript
