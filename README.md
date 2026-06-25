<h1 align="center">
  <img src="./assets/images/github/header.gif" alt="UnderCoverDraw" />
</h1>
<img src="./assets/images/github/star.gif" alt="star" />

---

# UnderCoverDraw — Draw and find the undercover

## Aperçu
Jeu de société **dessin & déduction** inspiré d'*Undercover*. La majorité des joueurs reçoit un **mot A**, tandis que l'imposteur reçoit un **mot B** très proche visuellement. Chacun dessine son mot de façon **simple et minimaliste** (style icône / pictogramme / bonhomme-bâton) : comme les deux croquis se ressemblent énormément, l'imposteur peut se fondre dans la masse. À la fin, tout le monde vote pour démasquer celui qui n'avait pas le bon mot.

Le cœur du projet est une **base de 283 couples de mots** « qui se ressemblent en dessin », regroupés par **forme** ou **famille** pour qu'on retrouve facilement un piège visuel.

## Fonctionnalités

### Concept de jeu
- **Variante « mot caché »** : la majorité reçoit le mot A, l'imposteur reçoit le mot B (très proche). Comme les dessins se ressemblent, l'imposteur peut bluffer
- **Jeu de dessin-piège** : un joueur tire un couple, dessine *l'un* des deux mots de façon simple ; les autres doivent deviner lequel des deux c'est — le piège vient de la ressemblance
- **Échauffement Pictionary** : idéal pour des manches rapides où le croquis minimaliste suffit
- Les couples des sections **croissant**, **objets longs**, **ciel** et **formes & symboles** sont les plus « traîtres » — leur croquis est quasi identique

### Base de couples de mots
- **283 couples** dont le dessin simplifié se ressemble fortement
- Lecture : `Mot A / Mot B` — les deux donnent (à peu près) le même croquis minimaliste
- Regroupés en **19 catégories** par forme ou famille (formes rondes, croissant, objets longs, triangles & cônes, animaux, oiseaux, insectes, fruits & légumes, plantes & fleurs, météo & espace, outils, objets du quotidien, vêtements, bâtiments, transports, corps humain, formes & symboles…)
- Disponible en deux formats : `couples_de_mots.md` (lecture humaine) et `couples_de_mots.json` (exploitable par code)

### Format des données
- Format JSON simple : chaque catégorie a un `nom` et une liste de `couples`, chaque couple étant un tableau `[mot_a, mot_b]`
- Facile à parser pour tirer un couple au hasard, filtrer par catégorie ou par niveau de difficulté

## Technologies
- **JSON** — base de données de couples de mots (`couples_de_mots.json`)
- **Markdown** — version lisible et classée de la base (`couples_de_mots.md`)

## Installation

Clonez le dépôt pour récupérer la base de couples :

```bash
git clone https://github.com/Pierre-Portfolio/undercoverdraw.git
cd undercoverdraw
```

Aucune dépendance n'est requise pour consulter ou exploiter les données.

## Structure du projet
```
UnderCoverDraw/
  README.md            → Présentation du projet
  couples_de_mots.json → Base de 283 couples (format [mot_a, mot_b] par catégorie)
  couples_de_mots.md   → Base lisible, classée en 19 catégories
  assets/
    images/github/     → Images README
```

## Schéma des données (JSON)

```json
{
  "description": "Couples de mots dont le dessin simplifie se ressemble. Format: [mot_a, mot_b].",
  "categories": [
    {
      "nom": "Formes rondes (le même rond)",
      "couples": [
        ["Soleil", "Tournesol"],
        ["Pomme", "Tomate"],
        ["Orange", "Mandarine"]
      ]
    }
  ]
}
```

## Comment l'utiliser

- **Jeu de dessin-piège** : un joueur tire un couple, dessine *un* des deux mots de façon simple ; les autres devinent lequel c'est.
- **Variante « mot caché » (Undercover)** : la majorité reçoit le mot A, l'imposteur le mot B (très proche). Les dessins se ressemblant, l'imposteur peut se fondre dans la masse jusqu'au vote final.
- **Échauffement Pictionary** : parfait pour des manches rapides où le dessin minimaliste suffit.

> Astuce : piochez dans les sections **croissant**, **objets longs**, **ciel & espace** et **formes & symboles** pour les pièges les plus difficiles.

## Aperçu de l'interface
<img src="./assets/images/github/UI.png" alt="Aperçu UnderCoverDraw" />

## Auteur
- [Pierre-Portfolio](https://github.com/Pierre-Portfolio/)

---

<p align="center">Projet réalisé en 2026.</p>
