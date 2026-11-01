---
name: hostile-review
description: À la fin du projet, rechercher les erreurs et les cas oubliés, corriger les défauts démontrés et vérifier les corrections avant livraison.
---
# Hostile-review
Déclencher cette revue à la fin de la réalisation, avant de déclarer le projet terminé. Être critique envers le résultat, respectueux envers son auteur.
Relire le besoin et les critères convenus, puis examiner le résultat comme si ses hypothèses étaient fausses.
Chercher les défauts pertinents : branches inaccessibles, champs mal reliés, données absentes, doublons, erreurs de connexion, effets externes répétés et résultats trompeurs.
Pour n8n, examiner les nœuds, leurs connexions, les expressions et les preuves d'exécution. Vérifier l'interdiction des nœuds HTTP Request et Code pour ce bootcamp.
Pour chaque défaut, donner une preuve ou un scénario reproductible, son impact et sa priorité. Distinguer un défaut confirmé d'un risque non testé. Ne pas inventer de critiques pour remplir un rapport.
Corriger les défauts dans le périmètre autorisé et retester le cas qui les révèle, ainsi que le chemin nominal si la correction peut l'affecter.
Arrêter lorsque les défauts bloquants sont résolus ou expliquer précisément ceux qui restent. Fournir un bilan court des corrections et limites, sans prétendre garantir l'absence de toute erreur.
Ne pas ajouter de fonctionnalités étrangères au projet pendant la revue.
