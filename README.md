<html lang="ca">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pàgina Web </title>
    <link rel="stylesheet" href="pep.css">
</head>
<body>

<div class="container">
    <h1>Benvingut a la nostra pàgina!</h1>
    <p>Escriu el teu nom:</p>
    <input type="text" id="nameInput" placeholder="Escriu el teu nom aquí">
    <br><br>
    <button onclick="saludarUser()">Saludar</button>

    <div id="greetingMessage" class="message"></div>

    <h2>Canvia el color de fons de la pàgina:</h2>
    <div class="colors">
        <button onclick="canviarColor('lightblue')">Blau</button>
        <button onclick="canviarColor('lightgreen')">Verd</button>
        <button onclick="canviarColor('lightcoral')">Vermell</button>
    </div>
</div>

<script>
    function saludarUser() {
        var userName = document.getElementById("nameInput").value;
        var greetingMessage = document.getElementById("greetingMessage");

        if (userName.trim() !== "") {
            greetingMessage.innerHTML = "Hola, " + userName + "! Benvingut a la meva pàgina web.";
        } else {
            greetingMessage.innerHTML = "Sisplau, introdueix el teu nom.";
        }
    }

    function canviarColor(color) {
        document.body.style.backgroundColor = color;
    }
</script>

</body>
</html>
