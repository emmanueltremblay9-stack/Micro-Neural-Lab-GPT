# Décisions — Micro Neural Lab

**Version :** 0.1.1  
**Rôle :** DECISION_REGISTER  
**État documentaire :** SOURCE_READY  
**Date :** 2026-10-20 — America/Toronto

Les identifiants MNL-DEC sont des identifiants documentaires de ce dossier, pas une inscription de projet au registre HQ. Ils sont conservés lors des révisions. Le statut d’une décision reste indépendant de son enregistrement dans GitHub.

## MNL-DEC-001 — Créer le projet spécialisé

- **Statut :** APPROVED — portée du mandat utilisateur uniquement.
- **Décideur :** utilisateur.
- **Base :** message « New gpt project with is government on git hub entirely about : Making micro neural network ».
- **Décision :** préparer un nouveau Project ChatGPT dont le domaine est la création de micro-réseaux neuronaux.
- **Portée :** définition du projet, instructions, sources, validation et avancement de l’installation accessible.
- **Ne prouve pas :** création réelle du Project, entraînement, choix d’application, acceptation de tout le corpus rédigé.
- **Remplace :** aucune décision antérieure.

## MNL-DEC-002 — Gouvernance dans GitHub

- **Statut :** APPROVED — exigence exprimée dans le même mandat.
- **Décideur :** utilisateur.
- **Décision :** conserver la gouvernance du projet dans GitHub : instructions maîtres, règles, décisions, file de travail et références des preuves.
- **Portée :** GitHub comme source canonique après intégration vérifiée ; champ ChatGPT et pièces jointes comme copies contrôlées.
- **Limites :** ne prouve pas l’existence du dépôt, un commit, une connexion automatique ni un droit de publication publique.
- **Remplace :** aucune.

## MNL-DEC-003 — Identité de travail et destination

- **Statut :** PROPOSED.
- **Auteur :** HQ, pendant la préparation.
- **Proposition :** nom `Dirty Studyo — Micro Neural Lab` ; dépôt `Micro-Neural-Lab-GPT` sous le compte connecté `emmanueltremblay9-stack` ; visibilité privée ; branche initiale `main`.
- **Justification :** nom descriptif, projet autonome et séparation du code des applications clientes.
- **Fait historique de préparation v0.1.0 :** la destination n’avait pas encore été identifiée. Les détails d’inventaire du compte restent hors de cette version publique.
- **UNKNOWN lors de la préparation v0.1.0 :** existence future, URL canonique, branche réelle, SHA, ID officiel de portefeuille, adoption du nom. La destination est maintenant résolue par MNL-DEC-007 ; le nom du Project et son ID de portefeuille restent distincts.
- **SUPERSEDED_BY :** MNL-DEC-007 pour la destination GitHub uniquement. Le nom du Project ChatGPT reste PROPOSED ; aucune adoption générale du fonctionnement détaillé n’en découle.

## MNL-DEC-004 — Socle technique

- **Statut :** PROPOSED.
- **Proposition :** privilégier les petits réseaux spécialisés et comparer une baseline simple ; choisir les architectures selon les entrées, la tâche, les données et l’appareil.
- **Départs suggérés :** démonstration CPU, inférence hors ligne lorsque pertinente, ressources cloud autorisées déjà disponibles pour le développement.
- **Pas de choix arrêté :** framework, runtime, seuil de paramètres, langage d’intégration, précision numérique, GPU, dataset, cible EGO ou musique.
- **Services :** ne pas introduire API payante, Ollama ou nouveau service par défaut. Une exception doit répondre à un besoin et rester dans une portée autorisée.
- **Acceptation :** préciser ces choix dans la spécification de la première expérience avant d’y engager des ressources.

## MNL-DEC-005 — Première expérience

- **Statut :** PROPOSED.
- **Proposition :** une démonstration de pipeline pour micro-MLP, avec données identifiées ou synthétiques déclarées, baseline, entraînement, export, équivalence et rapport.
- **Critère proposé :** reproduction possible des commandes, résultats tracés et vérification de l’artefact exporté ; aucun seuil arbitraire de précision métier.
- **Limite :** l’exemple 16 → 32 → 8 → 4 dans le guide est un calcul illustratif ; il n’est pas un modèle sélectionné ou entraîné.
- **Exécution actuelle :** NOT_RUN.

## MNL-DEC-006 — Timestamp

- **Statut :** PROPOSED pour une adoption future ; inclusion documentaire requise par les règles HQ de construction.
- **État actuel :** NOT_TESTED ; adoption et écritures non établies pour cette cible.
- **Décision non prise :** activation, identité officielle, calendrier, dépôt/branche/chemin de récupération.
- **Restriction :** la gouvernance GitHub du projet n’accorde aucun de ces droits par elle-même. Le protocole partagé reste inchangé.

## MNL-DEC-007 — Dépôt désigné pour l’intégration

- **Statut :** APPROVED — sélection explicite de la destination dans la portée du mandat existant.
- **Décideur :** utilisateur.
- **Base :** message fournissant `https://github.com/emmanueltremblay9-stack/Micro-Neural-Lab-GPT` après remise du dossier et demande de destination accessible.
- **Décision :** intégrer le socle documentaire préparé dans ce dépôt, puis le relire à un SHA identifié.
- **Observations GitHub :** ID `1427851195`, visibilité `public`, branche par défaut déclarée `main`, droits d’écriture disponibles, dépôt confirmé vide avant initialisation.
- **Portée :** publication des documents de ce projet dans la destination choisie. Aucun changement de visibilité ; aucun reçu privé, calendrier ou contenu privé d’un autre projet inclus.
- **SUPERSEDES :** partie destination de MNL-DEC-003 seulement. Le privé initialement proposé n’a pas été une décision acceptée.
- **Ne prouve pas :** installation du Project ChatGPT, adoption du nom ou des propositions techniques, licence de diffusion, entraînement, activation Timestamp ou autorisation de récupération TM.
- **Date exacte du message :** non fournie ; ne pas la déduire de l’heure de lecture GitHub.

## Protocole d’entretien

Pour une nouvelle décision, consigner : ID, sujet, statut, décideur, portée, version concernée, preuve d’acceptation, date connue, dépendances et remplacement éventuel. Une date de préparation n’est pas l’heure d’une décision utilisateur. Préserver l’ancienne entrée et les liens SUPERSEDES/SUPERSEDED_BY.

Les statuts possibles sont PROPOSED, APPROVED, LOCKED, SUPERSEDED et REVOKED. LOCKED exige une protection explicite ; aucun nouveau verrou métier n’est inventé dans cette livraison. Une consigne utilisateur claire peut réviser une décision de son autorité si elle vise explicitement le point protégé. Ni « next » ni une fusion technique ne suffisent.
