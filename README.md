<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Green Quest</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <img src="https://example.com/path/to/your/logo.png" alt="Green Quest Logo" id="logo">
        <h1>Green Quest</h1>
        <p>¡Descubre, aprende y actúa para salvar nuestro planeta!</p>
    </header>

    <div class="content">
        <div class="section" id="challenges-section">
            <h2>Retos Diarios</h2>
            <p>Completa estos retos diarios para reducir tu impacto ambiental:</p>
            <ul id="daily-challenges" class="challenges"></ul>
        </div>

        <div class="section" id="videos-section">
            <h2>Videos Educativos</h2>
            <p>Aprende más sobre el cambio climático y cómo puedes ayudar:</p>
            <div id="video-container"></div>
        </div>

        <div class="section" id="recommendations-section">
            <h2>Recomendaciones</h2>
            <p>Consejos para vivir de manera más sostenible:</p>
            <ul id="recommendations" class="challenges"></ul>
        </div>
    </div>

    <footer>
        <p>&copy; 2024 Green Quest | Todos los derechos reservados</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
    body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f0f9f4;
    color: #333;
}

header {
    background-color: #4CAF50;
    color: white;
    padding: 20px;
    text-align: center;
}

header img#logo {
    width: 80px;
    height: auto;
    display: block;
    margin: 0 auto 10px;
}

h1 {
    margin: 0;
    font-size: 2.5em;
}

.content {
    margin: 20px;
}

.section {
    background-color: white;
    padding: 20px;
    margin-bottom: 20px;
    border-radius: 10px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.section h2 {
    color: #4CAF50;
    font-size: 1.8em;
}

.section p {
    font-size: 1.1em;
    line-height: 1.6;
}

.challenges li {
    background-color: #f0f4f7;
    padding: 10px;
    margin-bottom: 10px;
    border-radius: 5px;
    font-size: 1.2em;
}

footer {
    background-color: #4CAF50;
    color: white;
    text-align: center;
    padding: 10px;
    position: fixed;
    bottom: 0;
    width: 100%;
}

#video-container iframe {
    width: 100%;
    height: 315px;
    border: none;
    border-radius: 8px;
    margin-top: 10px;
}
// Datos para los retos diarios
const dailyChallenges = [
    "🌳 Planta un árbol en tu comunidad.",
    "🚴‍♀️ Usa la bicicleta o camina en lugar de conducir.",
    "♻️ Separa y recicla tus desechos correctamente.",
    "🌱 Reduce el consumo de carne por un día.",
    "💡 Cambia a bombillas LED de bajo consumo en tu hogar."
];

// Datos para los videos educativos
const educationalVideos = [
    {
        title: "Cambio Climático Explicado en 2 Minutos",
        url: "https://www.youtube.com/embed/GLTCiS6hOT4"
    },
    {
        title: "¿Qué es la Biodiversidad y por qué es Importante?",
        url: "https://www.youtube.com/embed/1yz0-bEqKLY"
    }
];

// Datos para las recomendaciones
const recommendations = [
    "💧 Ahorra agua cerrando el grifo mientras te cepillas los dientes.",
    "🌍 Compra productos locales para reducir la huella de carbono.",
    "🔌 Desconecta los aparatos electrónicos cuando no los uses.",
    "🛒 Lleva bolsas reutilizables cuando vayas de compras.",
    "🍽️ Aprovecha los restos de comida para evitar desperdicios."
];

// Función para renderizar la lista de retos diarios
function renderChallenges() {
    const challengesList = document.getElementById("daily-challenges");
    dailyChallenges.forEach(challenge => {
        const listItem = document.createElement("li");
        listItem.textContent = challenge;
        challengesList.appendChild(listItem);
    });
}

// Función para renderizar los videos educativos
function renderVideos() {
    const videoContainer = document.getElementById("video-container");
    educationalVideos.forEach(video => {
        const iframe = document.createElement("iframe");
        iframe.src = video.url;
        iframe.title = video.title;
        videoContainer.appendChild(iframe);
    });
}

// Función para renderizar la lista de recomendaciones
function renderRecommendations() {
    const recommendationsList = document.getElementById("recommendations");
    recommendations.forEach(recommendation => {
        const listItem = document.createElement("li");
        listItem.textContent = recommendation;
        recommendationsList.appendChild(listItem);
    });
}

// Llamar a las funciones para renderizar contenido cuando la página cargue
window.onload = function() {
    renderChallenges();
    renderVideos();
    renderRecommendations();
};
