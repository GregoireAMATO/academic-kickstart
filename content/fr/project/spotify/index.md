---
title: Aliments
summary: Optimisation sous contrainte
tags:
- Python
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: "http://pydathon.pythonanywhere.com/"

image:
  # caption: Photo by rawpixel on Unsplash
  focal_point: Smart



# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---

## Utilisation de l'application

Cette application permet de concevoir un repas selon deux contraintes : 
 
- Le régime alimentaire suivi : Omnivore, Végétarien, Vegan, Sans Lactose

- Un objectif fixé : 
  - minimisation du prix seul
  - minimisation du prix et ne pas dépasser les objectifs à plus de 10%
  - minimisation du prix et atteindre ses objectifs à plus ou moins 10%

Après avoir renseigné ces contraintes, vous pouvez, si vous le souhaitez, modifier vos objectifs d'apports nutritionnels par repas en modifiant la valeur des sliders. 

Ensuite, le repas recommandé s'affiche dans le tableau interactif en bas à gauche, dont vous pouvez déplacer les colonnes afin d'avoir une meilleure visibilité, et un résumé de vos objectifs s'affiche sur le diagramme en barres interactif, dont la ligne rouge indique le/les seuil(s) à atteindre/ne pas dépasser en fonction de l'objectif fixé.

L'application est disponible [ici](http://pydathon.pythonanywhere.com/).  
