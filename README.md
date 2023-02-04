# Test technique - EMIE - 04/02/2023

## Première étape : Ajout des composant

Uniquement en mode développeur :
`composer require --dev symfony/maker-bundle`
--> permet de gagner en efficacité

`composer require symfony/orm-pack`
--> Concerne le système d'information

`composer require api`
--> Permet l'utilisation d'API Platform

## Réalisation

J'ai donc créé un controller `FichierController`. Celui-ci définie la route suivant : `/fichier/{correction}`.
*correction* est ainsi un paramètre optionnel :
- correction === majuscule : L'ensemble du fichier est renvoyé en majuscule
- correction === minuscule : L'ensemble du fichier est renvoyé en minuscule

J'ai aussi essayé de lier ceci avec *API Platform* mais pas réussi.


J'ai fourni un petit jeu de test dans le dossier suivant : [resultats](resultats)

Nous pouvons y constater le test des deux types de corrections :
- [Correction majuscule](resultats/minToMax.png)
- [Correction minuscule](resultats/maxToMin.png)

Mais aussi la gestion d'exceptions / erreurs comme :
- [L'entrée d'un mauvais type de correction](resultats/mauvaiseCorrection.png)
- [L'erreur dans l'envoi de fichier](resultats/aucunFichier.png)