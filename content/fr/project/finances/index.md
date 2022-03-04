---
title: Spotify
summary: Optimisation sous contrainte
tags:
- Python
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
#external_link: "http://pydathon.pythonanywhere.com/"

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

# Objectifs
Lorsque vous possédez plusieurs comptes d'investissements différents, il peut être compliqué de gérer son portefeuille. C'est pourquoi cette application vous permet d'importer directement vos exports csv, de les nettoyer/enrichir, puis de les fusionner automatiquement. L'application a été développée dans une optique d'investissement "DCA" (Dollar Cost Averaging), et donc dans une optique d'investissement régulier long terme, les prix sont donc actualisés tous les jours, et non pas en temps réel. 

## Guide d'utilisation
### Nettoyage des données 

Dans un premier temps, il vous faut nettoyer et enrichir les données que vous souhaitez étudier. Pour cela, utilisez la première partie tout en haut à gauche de l'application, sélectionnez la provenance des données si connue, sinon sélectionnez "Standard", puis lancez le nettoyage. Celui-ci peut prendre quelques minutes, surtout si votre portefeuille contient de nombreuses lignes. Attention, si vous utilisez un export connu, vérifiez qu'aucune information autre que relative à vos placements ne s'y trouve, cela pourrait affecter l'importation et le nettoyage du fichier. Les seules information nécessaires sont :

- L'ISIN **ET/OU** le Symbole du produit obligatoirement, si vous avez les deux vous pouvez les renseigner cela raccourcira le nettoyage. Par exemple, l'ISIN d'Apple est US0378331005 et son symbole est AAPL. Attention, l'ISIN d'un produit est unique mais il peut exister des confusions entre symboles donc soyez vigilents si vous n'entrez que le symbole d'un titre. Par exemple, L'Oreal, a pour symbole OR (qui correspond également à Osisko Gold Royalties Ltd.) ou OR.PA en fonction des bases de données, soyez vigilents et vérifiez bien que le résultat du nettoyage correspond bien à ce que vous avez entré, et modifiez le symbole si cela n'est pas le cas. L'application utilise l'API Yahoo Finance, donc n'hésitez pas à vous rendre sur le site si une ligne ne correspond pas afin de trouver le symbole qui lui est associé.
- Le prix moyen d'achat du/des titres
- La quantité de titres détenus

Les autres informations (symbole, prix...) sont déduites à partir de l'ISIN ou du symbole, il n'est donc pas nécessaire de les spécifier. Afin de vous aider, vous aurez à votre disposition un template à télécharger. Concernant les cryptomonnaies, l'application n'est pas encore compatibles avec celles-ci puisqu'elles n'ont pas de numéro ISIN, cela fera l'objet d'un ajout futur. 

L'accès aux données par connexion API est en cours de développement et sera bientôt disponible. 

## Exemple d'utilisation

Lorsque vous importez votre premier fichier, une liste déroulante apparaît, contenant les noms de tous les fichiers importés dans l'application. Vous pourrez alors les sélectionner pour faire apparaître un tableau récapitulatif. Si vous sélectionnez plusieurs fichiers (par exemple si vous possédez plusieurs comptes-titres sur différentes plateformes), ceux-ci seront automatiquement fusionnés.

Les informations et documents sont stockés dans l'application et sont supprimés à chaque fin de session. Si vous actualisez la page, tous les documents disparaitrons.

L'application est disponible [ici](http://pydathon.pythonanywhere.com/).  
