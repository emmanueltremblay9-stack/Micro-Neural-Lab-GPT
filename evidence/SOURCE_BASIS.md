# Sources et portée de préparation

**Version :** 0.1.1  
**Rôle :** PREPARATION_EVIDENCE ; pas une politique supplémentaire  
**Date :** 2026-10-20 — America/Toronto

## Mandat directement fourni

L’utilisateur demande un nouveau projet GPT entièrement consacré à la création de micro-réseaux neuronaux, dont la gouvernance se trouve sur GitHub. « Government » est interprété comme « gouvernance » dans ce contexte. Aucun projet gouvernemental ou institutionnel n’est inféré.

La cible est un Project ChatGPT autonome au sein du portefeuille Dirty Studyo. Le nom Micro Neural Lab, les préférences techniques et la première expérience restent proposés. La destination GitHub initialement proposée est désormais désignée par l’utilisateur ; voir MNL-DEC-007. Aucun ID officiel de portefeuille n’est alloué ; aucun registre HQ n’est modifié.

## Corpus fourni et utilisé

Les copies des pièces jointes fournies ont été consultées dans l’espace de préparation. Les noms ci-dessous sont les noms logiques fournis ; la sélection repose sur les rôles et versions déclarés. Les préfixes numériques locaux ne sont pas des versions. Le manifeste historique référencé par certaines sources n’est pas fourni : l’inventaire reste partiel.

| Source | Version | Lecture et emploi |
|---|---|---|
| HQ_CHARTER.md | 1.3.0 | Consulté : mission, autorité et distinction production/intégration |
| HQ_PROJECT_ARCHITECTURE.md | 1.0.0 | Lu : construction, TM, Codex conditionnel et livraison |
| 01_CONCEPTION_ET_GABARITS.md | 0.2.0 | Lu : cadrage et champ cible intégral |
| 02_PLANIFICATION_SOURCES.md | 0.2.0 | Consulté : sources limitées aux rôles utiles |
| 03_AUDIT_ET_VALIDATION.md | 0.2.0 | Lu : comptage, scénarios statiques et archive |
| PROJECT_REGISTRY.md | 1.3.0 | Consulté comme index historique ; pas de synchronisation live affirmée |
| OPERATING_SYSTEM.md | 1.3.0 | §14 lu : profil HQ distinct de la nouvelle cible |
| CROSS_PROJECT_DECISIONS.md | 1.3.0 | Sections pertinentes DS-DEC-013/015/016 ; aucune autre proposition promue |
| TIMESTAMP_MACHINE_SHARED_PROJECT_SOURCE_v1.3.0.md | 1.3.0 | Lu et copié à l’identique |

Finance, droit, offres, actifs et exemples historiques ne sont pas des dépendances métier de cette cible. Le workflow Codex n’est pas inclus : aucune cible Codex n’est demandée. Les préférences mémorisées servent seulement à formuler des propositions explicites, sans importer les droits d’un spécialiste.

Un autre agent a effectué une seconde revue statique des six documents initiaux. Cette séparation ne constitue pas un test exécuté du Project installé ni une certification externe.

## Historique et désignation de la destination

La préparation v0.1.0 du 2026-10-20, America/Toronto, a produit le dossier sans installation distante. L’archive remise à l’utilisateur reste inchangée : SHA-256 `6213898f254fdaddfe1c43b7adf6bf864e521199cd1d9a57a90559e3f92bc6b2`. Cette révision publique conserve le constat utile et omet les détails d’inventaire du compte et de connexion, qui ne sont pas des sources métier.

L’utilisateur a ensuite fourni l’URL `https://github.com/emmanueltremblay9-stack/Micro-Neural-Lab-GPT` pour poursuivre l’installation demandée. Lecture directe par le connecteur : ID `1427851195`, visibilité `public`, branche par défaut déclarée `main`, permissions d’écriture disponibles, aucune branche retournée et réponse GitHub « Git Repository is empty. » à la liste des commits. Ces faits préalables établissaient une destination vide accessible ; ils sont distincts de la relecture réalisée après écriture.

Le socle de 12 fichiers a ensuite été relu intégralement au commit `603384eb7ce6d029eeab9279cc2be3fc3c4206eb` ; son reçu est `evidence/GITHUB_INTEGRATION.json`. La révision qui enregistre ce reçu est relue séparément avant le compte rendu final. La création du Project ChatGPT, l’installation de son champ Instructions et sa propre lecture GitHub restent non effectuées ou non testées. Les fonctions de pages/espaces ne sont pas assimilées à un Project.

Une revue ciblée distincte a examiné les 12 fichiers préparés avant publication : aucun email, identifiant réel de calendrier, reçu privé, chemin local absolu, identifiant Library ou secret détecté. Les détails de session et le nombre de dépôts accessibles ont été retirés de cette copie publique. Cette revue ne porte pas sur des fichiers externes au dossier.

## Références techniques primaires

Consultation : 2026-10-20, America/Toronto. Ces références justifient une méthode ; elles ne prouvent aucun résultat du modèle futur.

| Référence | Usage précis | Limite |
|---|---|---|
| [LiteRT for Microcontrollers](https://developers.google.com/edge/litert/microcontrollers/overview) | Distinguer entraînement, conversion et inférence ; vérifier les opérateurs disponibles | Aucun runtime choisi ; la taille d’un noyau n’est pas celle de l’application |
| [ONNX Runtime — Quantization](https://onnxruntime.ai/docs/performance/model-optimizations/quantization.html) | Calibration, perte de précision possible, backend et opérateurs | Aucun gain garanti pour notre cible future |
| [scikit-learn — Common pitfalls](https://scikit-learn.org/stable/common_pitfalls.html) | Partition avant prétraitement appris, ajustement sur train et prévention des fuites | Aucun dataset réel évalué ici |
| [Hinton, Vinyals, Dean — Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531) | Concept de transfert vers un étudiant plus petit | Aucun enseignant ou étudiant sélectionné |
| [OpenAI — Projects and chats](https://learn.chatgpt.com/docs/projects) | Contexte partagé des fichiers, instructions et sources des Projects | Aucun accès ou quota propre au compte vérifié par cette page |

L’exemple 16 → 32 → 8 → 4 est calculé à partir des dimensions : 800 poids + 44 biais = 844 paramètres ; FP32 brut = 3 376 octets. Aucun chiffre de latence, précision ou énergie n’est déduit de ce calcul.

## Conventions

- Documents nouveaux : UTF-8, LF et LF final.
- Timestamp : copie octet pour octet, version 1.3.0 et statut propres conservés.
- Seul le champ Instructions est soumis au plafond de 8 000 points de code ; les guides sont séparés.
- `null` dans le manifeste signifie un identifiant/localisateur non établi, accompagné d’un état ; les destinations proposées ne deviennent pas des faits.
- Les empreintes de livraison prouvent l’identité des octets, pas une approbation, une licence ou une installation.
