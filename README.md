# Dirty Studyo — Micro Neural Lab

**Version :** 0.1.1 — GITHUB_INTEGRATED / CHATGPT_NOT_INSTALLED  
**Nom :** nom de travail proposé  
**Date de préparation :** 2026-10-20 — America/Toronto  
**Objet :** Project ChatGPT spécialisé dans la création de micro-réseaux neuronaux, avec gouvernance canonique sur GitHub.

## Le résultat recherché

Passer d’une tâche précise à un réseau suffisamment petit, utile et vérifié pour son appareil cible : définir le problème, préparer les données, concevoir, entraîner, évaluer, réduire, exporter et intégrer. Le projet sert autant à apprendre qu’à produire des composants réutilisables. Il explique ses choix et conserve les preuves nécessaires pour les reprendre.

Le domaine inclut les MLP, CNN compacts, modèles temporels, autoencodeurs et politiques bornées. Il peut étudier un modèle de langage lorsque la tâche le justifie. Il ne suppose aucun seuil universel du mot « micro ». La précision utile et les limites de stockage, mémoire et calcul sont définies pour chaque expérience.

## État de cette livraison

| Élément | État |
|---|---|
| Demande de nouveau projet et gouvernance GitHub | Mandat utilisateur reçu |
| Nom du Project ChatGPT | PROPOSED |
| Dépôt GitHub | Désigné explicitement par l’utilisateur ; MNL-DEC-007 |
| Corpus et champ Instructions | Produits ; voir le rapport de validation |
| Compte GitHub connecté | Identifié par le connecteur pendant cette préparation |
| Intégration GitHub | Socle de 12 fichiers intégré et relu au SHA consigné ; reçu ajouté dans cette révision |
| Projet ChatGPT et champ installé | NON EFFECTUÉS / non vérifiés dans la destination |
| Modèle entraîné ou benchmark | NOT_RUN ; cette livraison construit le projet |
| Timestamp de cette nouvelle cible | NOT_TESTED ; adoption et écritures non autorisées |

Historique v0.1.0 : le dossier était préparé, sans intégration distante. L’utilisateur a ensuite fourni le dépôt cible. Les détails privés de la session de préparation restent hors du dépôt public.

## Dépôt de gouvernance

- Dépôt désigné : [emmanueltremblay9-stack/Micro-Neural-Lab-GPT](https://github.com/emmanueltremblay9-stack/Micro-Neural-Lab-GPT).
- Identifiant GitHub observé : `1427851195`.
- Visibilité observée : **publique** ; aucun changement de visibilité effectué.
- Branche canonique : `main`, créée par l’initialisation et vérifiée par lecture de sa référence.
- Socle vérifié : `603384eb7ce6d029eeab9279cc2be3fc3c4206eb` ; voir [le reçu d’intégration](evidence/GITHUB_INTEGRATION.json). Ce SHA identifie le socle antérieur relu, pas le commit contenant son reçu.

Le manifeste est l’index des sources et des états. Ce dépôt est désormais le lieu canonique de la gouvernance, après relecture du socle. Une pièce jointe au Project est un instantané identifié par sa provenance ; aucune synchronisation permanente n’est présumée. La proposition privée initiale est conservée comme historique dans les décisions.

## Contenu à utiliser

| Fichier | Usage |
|---|---|
| [PROJECT_INSTRUCTIONS.txt](PROJECT_INSTRUCTIONS.txt) | Champ Instructions complet à installer dans le nouveau Project |
| [PROJECT_MANIFEST.json](PROJECT_MANIFEST.json) | Identité, localisateurs, rôles et états d’intégration |
| [PROJECT_CHARTER.md](PROJECT_CHARTER.md) | Mission, périmètre, autonomie et règles GitHub |
| [DECISIONS.md](DECISIONS.md) | Mandat établi, propositions et historique |
| [WORK_QUEUE.md](WORK_QUEUE.md) | File unique désignée et prochaine action |
| [NEURAL_ENGINEERING.md](NEURAL_ENGINEERING.md) | Méthode technique et modèles de fiches |
| [TIMESTAMP_MACHINE_SHARED_PROJECT_SOURCE_v1.3.0.md](TIMESTAMP_MACHINE_SHARED_PROJECT_SOURCE_v1.3.0.md) | Source commune conservée à l’identique, activation séparée |
| [evidence/SOURCE_BASIS.md](evidence/SOURCE_BASIS.md) | Origine des règles et observations de préparation |
| [evidence/VALIDATION.md](evidence/VALIDATION.md) | Contrôles exécutés et limites |

Les guides HQ employés pour concevoir ce dossier ne deviennent pas les sources métier du nouveau projet. Aucun workflow Codex n’est activé : la demande vise un Project ChatGPT et GitHub.

## Intégration en deux destinations

### 1. GitHub

Le dépôt a été désigné par l’utilisateur et confirmé vide par GitHub avant l’initialisation. Le socle documentaire est intégré à sa racine, avec `evidence/`, et ses 12 fichiers ont été relus intégralement au commit consigné. Le reçu privé de traçabilité HQ et les pièces jointes HQ d’origine ne font pas partie de cette publication ; seule la source Timestamp commune, générique et inchangée, est incluse.

Le reçu ajouté dans cette révision décrit la relecture du socle de 12 fichiers. Le manifeste, ce README et la file sont rapprochés de ce résultat. Le reçu décrit le commit antérieur réellement relu : il ne prétend pas contenir le SHA du commit qui le crée. La relecture finale de cette révision de 13 fichiers est rapportée dans le compte rendu de livraison, hors de ses propres octets.

Pour les évolutions ultérieures, préparer une branche et un diff ou une PR selon le mandat, préserver les contributions existantes et vérifier la portée de fusion. Conserver les constats antérieurs comme historiques datés.

Aucune licence de diffusion n’est choisie par défaut. Les documents ont été préparés pour Dirty Studyo ; la provenance des références figure dans `evidence/SOURCE_BASIS.md`. Aucun modèle, dataset, workflow Actions, service, dépense, secret ou nouvelle permission n’est ajouté par cette initialisation. Le compte rendu de livraison sert de remise au propriétaire ; aucune annonce à un tiers n’est prévue. Les corrections de gouvernance suivent la file unique `WORK_QUEUE.md`.

### 2. ChatGPT

Créer un Project intitulé **Dirty Studyo — Micro Neural Lab** si ce nom convient, puis installer le contenu intégral de `PROJECT_INSTRUCTIONS.txt` dans son champ Instructions. Conserver le LF final du fichier lorsque le champ le permet et vérifier le contenu enregistré ; si l’interface le transforme, relever cette différence et recompter la représentation sauvegardée.

Rendre le dépôt accessible par le connecteur GitHub disponible dans ce Project. Vérifier par une vraie lecture du manifeste et d’un fichier au commit attendu. Les limites et possibilités du compte doivent être observées dans cette destination ; ce dossier n’affirme aucun quota ni accès automatique.

Ajouter la source Timestamp inchangée aux sources de la cible. Si des copies des autres fichiers sont attachées, les identifier comme instantanés, avec dépôt, branche, commit et date réellement connus. Ne pas conserver deux files de travail actives. Une mise à jour GitHub ne modifie pas automatiquement le champ Instructions installé.

La documentation officielle décrit les Projects comme un contexte partagé de conversations, fichiers, instructions et sources connectées. La disponibilité réelle des connexions reste à vérifier dans le Project : [Projects and chats](https://learn.chatgpt.com/docs/projects), consulté le 2026-10-20.

### 3. Premier contrôle dans le Project installé

Demande de démarrage proposée :

> Lis le manifeste et les sources pertinentes du dépôt de gouvernance à un commit identifié. Indique ce qui est effectivement accessible, les décisions acceptées, les propositions et la prochaine tâche admissible. Prépare ensuite la spécification d’une première démonstration reproductible d’un micro-MLP sur CPU, sans lancer d’entraînement ni d’installation. Ne revendique aucun résultat de benchmark.

La réponse doit citer la référence réellement lue, conserver les UNKNOWN et laisser Timestamp inactif. Ce contrôle teste le comportement de démarrage ; il ne valide pas un entraînement ou une intégration applicative.

## Premier parcours technique proposé

1. Une démonstration reproductible : données ou générateur identifié, baseline simple, petit MLP, export et comparaison des sorties. Des données synthétiques démontrent seulement le pipeline.
2. Un vrai cas d’usage avec données disponibles et seuils d’acceptation définis avant le test final.
3. Une optimisation justifiée par une contrainte mesurée, suivie d’une nouvelle évaluation de l’artefact exporté.

EGO peut utiliser un petit réseau pour classer des actions ; une playlist peut noter des transitions tout en gardant des règles anti-répétition explicites. Ce sont des options. Aucun accès à EGO, Suno ou leurs données n’est hérité par le nouveau projet.

## Entretien

Mettre à jour la source correspondant au fait : décisions dans `DECISIONS.md`, travail dans `WORK_QUEUE.md`, preuve dans `evidence/` ou l’expérience concernée. Éviter un deuxième tableau de tâches faisant concurrence à cette file. Recompter les Instructions après chaque révision. Préserver les IDs, les décisions protégées, les preuves anciennes et l’origine des instantanés.
