---
name: doubt-driven-dev
description: Pendant le développement, identifier les hypothèses incertaines et vérifier les comportements avec des tests proportionnés avant de les déclarer validés.
---
# Doubt-driven-dev
Appliquer cette méthode tout au long de la réalisation.
Distinguer faits observés, hypothèses et inconnues. Vérifier en priorité les hypothèses qui pourraient invalider le projet.
Avant une étape incertaine, définir le résultat attendu et choisir la vérification la plus courte qui peut le confirmer ou le réfuter.
Pour n8n, consulter les paramètres réels des nœuds, vérifier les données entre étapes et tester le chemin nominal ainsi que les erreurs pertinentes : champs absents, valeurs invalides et doublons selon le projet.
Une validation de schéma ou un test simulé ne prouve pas le fonctionnement des connexions réelles. Dire précisément ce qui a été testé et ce qui reste incertain.
Après un échec, examiner sa cause, effectuer une correction ciblée et retester le comportement concerné. Après deux tentatives infructueuses sur la même cause, changer d'approche ou expliquer le blocage.
Limiter les appels et éviter les vérifications répétitives quand le comportement est déjà établi. Conserver une trace concise : hypothèse, test, résultat, correction éventuelle.
Utiliser des données fictives pour les essais et respecter les autorisations avant toute action externe.
Pour ce bootcamp, vérifier l'absence de nœuds HTTP Request et Code.
