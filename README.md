# Assistant de prospection B2B — TenderStrike

Projet de bootcamp réalisé avec n8n Cloud, n8ncli et Codex. Il prépare la liste quotidienne des prospects BTP à appeler et propose des accroches téléphoniques avec Gemini.

## Présentation vidéo

Les deux parties sont à regarder dans cet ordre :

1. [Première partie — présentation et démonstration](https://www.loom.com/share/91980c9c73a3445c8f6fd217339e200e)
2. [Deuxième partie — suite de la présentation](https://www.loom.com/share/86a15a645f7147d998b1b7aa05149f51)

Les vidéos sont hébergées sur Loom et ne sont pas fusionnées dans un fichier local.

## Fonctionnement

1. Déclenchement du lundi au vendredi à 9h, fuseau Europe/Paris, ou lancement manuel pour les tests.
2. Lecture des prospects dans Google Sheets.
3. Sélection des appels prévus aujourd’hui ou en retard, hors prospects clôturés et dates invalides.
4. Tri par date croissante.
5. Génération d’une accroche et d’une question par prospect avec Gemini Flash-Lite Latest.
6. Envoi d’un seul récapitulatif Gmail. Si la liste est vide, envoi du message « Aucun appel prévu aujourd’hui ».

Le workflow quotidien ne modifie pas Google Sheets. Il n’utilise aucun nœud HTTP Request ni Code. Les données de démonstration sont fictives et les suggestions IA doivent être relues.

## Méthode de travail

- **Interview** : cadrer le besoin avant la construction.
- **Doubt-driven-dev** : tester les hypothèses pendant le développement.
- **Hostile-review** : rechercher les erreurs, les corriger et retester avant publication.

## Vérifications réalisées

- Lecture réelle : 12 prospects, dont 7 retenus lors du test initial, triés et réunis dans un seul e-mail.
- Simulation sans appel éligible : message alternatif envoyé.
- Simulation d’indisponibilité de Gemini : conservation du récapitulatif avec une mention de repli.
- Comparaison du tableau avant et après les tests : aucune modification.
- Revue des suggestions IA : correction du prompt après une supposition injustifiée sur une réunion commune.

Les dates du jeu de démonstration sont fixes autour du 22 octobre 2026 : le nombre de prospects éligibles évolue avec la date d’exécution.

## Commandes n8ncli utilisées

| Commande | Rôle |
|---|---|
| `projects` | Retrouver le projet et vérifier la connexion |
| `import-skill` | Récupérer le skill n8ncli |
| `nodes types` / `nodes doc` | Consulter les paramètres des nœuds |
| `push` | Envoyer les workflows vers n8n |
| `pull` | Récupérer la version distante |
| `validate` | Vérifier structure et paramètres |
| `exec` | Lancer une exécution réelle |
| `test` | Tester des scénarios avec données simulées |
| `execution` | Examiner les résultats |
| `publish` | Publier le workflow |

Certaines opérations ont utilisé directement le même serveur MCP pour les options non prises en charge par la version de n8ncli installée. La configuration initiale a été créée directement : `init` n’a pas été utilisé.
