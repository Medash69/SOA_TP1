# SOA_TP1
TP1 : Introduction aux APIs RESTful
Weather App est une application développée en Node.js qui permet de récupérer et d’afficher les données météorologiques d’une ville en temps réel, en utilisant l’API OpenWeatherMap.

Fonctionnalités principales

Récupération des données météo en temps réel

Affichage de la température actuelle, minimale et maximale

Affichage du taux d’humidité et de la pression atmosphérique

Informations sur la vitesse et la direction du vent

Heures de lever et de coucher du soleil

Affichage du pays correspondant à la ville

Gestion des erreurs (ville introuvable, problème de connexion, quota API dépassé, etc.)

Utilisation d’axios et d’async/await pour une meilleure performance

Affichage des données dans des unités standards (Celsius, m/s, hPa)

Prérequis

Node.js installé sur votre machine

Clé API valide obtenue sur OpenWeatherMap

Installation et exécution

bash
Copy
Edit
git clone https://github.com/Arijbettaib/weather-app.git
cd weather-app
npm install
Ajoutez votre clé API dans le fichier index.js, puis lancez l'application avec :

bash
Copy
Edit
node index.js
Utilisation
Vous pouvez modifier la ville directement dans le fichier index.js :

js
Copy
Edit
getWeatherData("Sousse");
Ou bien permettre la saisie d’une ville par l’utilisateur via la console :

js
Copy
Edit
const readline = require("readline");
const rl = readline.createInterface({ input: process.stdin, output: process.stdout });
rl.question("Entrez une ville : ", (ville) => {
    getWeatherData(ville);
    rl.close();
});
Structure du code

Importation du module axios pour les requêtes HTTP

Fonction getWeatherData(city) pour interroger l’API

Affichage détaillé des informations météo

Conversion des timestamps Unix en heure locale

Bloc try/catch pour capturer et afficher les erreurs éventuelles

Exemple de sortie

yaml
Copy
Edit
Ville: Sousse, TN
Description: ciel dégagé
Température actuelle: 22°C
Température max: 25°C
Température min: 18°C
Humidité: 65%
Pression: 1015 hPa
Vent: 3.2 m/s, direction 180°
Lever du soleil: 06:30
Coucher du soleil: 18:45
Dépendances

axios : pour les appels HTTP

readline : pour les interactions via la ligne de commande

Améliorations prévues

Ajout d’un affichage sur plusieurs jours

Détection automatique de la localisation par adresse IP

Développement d’une interface web plus visuelle
