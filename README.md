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
