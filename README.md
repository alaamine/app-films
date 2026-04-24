#  Application web de films

> Projet réalisé en 2025 à **Supinfo Paris**

##  Description

Site web dynamique utilisant une API de films pour récupérer et afficher des informations en temps réel : titres, notes, descriptions, affiches, etc.

##  Fonctionnalités

 Recherche de films via une API externe
-  Récupération des données au format JSON
-  Affichage dynamique des films (titre, note, description, affiche)
-  Interface responsive

##  Technologies utilisées

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

##  Structure du projet

```
app-films/
├── index.html
├── style.css
├── script.js
└── README.md
```

##  Exemple de code

```javascript
// Récupération des films via l'API
async function fetchFilms(query) {
  const response = await fetch(`https://api.example.com/search?q=${query}`);
  const data = await response.json();
  afficherFilms(data.results);
}

// Affichage dynamique des résultats
function afficherFilms(films) {
  films.forEach(film => {
    const card = document.createElement('div');
    card.innerHTML = `
      <h3>${film.title}</h3>
      <p>⭐ ${film.vote_average}/10</p>
      <p>${film.overview}</p>
    `;
    document.getElementById('results').appendChild(card);
  });
}
```

##  Ce que j'ai appris

- Utilisation d'une API REST externe
- Manipulation du format JSON en JavaScript
- Affichage dynamique du DOM
- Gestion des requêtes asynchrones avec `fetch` et `async/await`

---

*Projet académique — Supinfo Paris 2024*
