# Ingénierie des micro-réseaux neuronaux

| Métadonnée | Valeur |
|---|---|
| Projet | Dirty Studyo — Micro Neural Lab — titre de travail proposé |
| Version | 0.1.0 |
| Statut documentaire | SOURCE_READY |
| Rôle | Référence technique subordonnée aux Instructions et à la gouvernance du projet |
| Date | 2026-10-20 — America/Toronto |
| Portée | Concevoir, entraîner, évaluer, réduire et intégrer des réseaux spécialisés compacts |

SOURCE_READY signifie que cette référence est préparée. Aucun entraînement, benchmark, modèle, export ou test d’intégration n’a été exécuté pour sa rédaction. Les chemins, architectures et seuils illustratifs ne constituent pas des choix approuvés. Aucun framework, jeu de données, modèle, licence ou premier cas d’usage n’est adopté globalement par ce document.

## 1. Définir le problème avant le réseau

Un micro-réseau est ici un réseau spécialisé conçu sous des contraintes explicites. Le terme ne fixe aucun seuil universel de paramètres. L’objectif est une fonction utile avec un coût compatible avec sa cible. Le projet peut étudier des architectures minuscules, sans promettre qu’elles résoudront une tâche mal définie ou dépourvue de données pertinentes.

Pour chaque expérience, renseigner cette fiche dans son dossier existant, sans créer un registre parallèle :

| Champ | Contenu attendu |
|---|---|
| Tâche et propriétaire | Fonction précise, utilisateur, responsable de l’acceptation |
| Entrées | Variables, ordre, types, unités, plages, fréquence, valeurs absentes |
| Sorties | Classes, valeurs, scores ou actions admissibles et leur signification |
| Données | Provenance, disponibilité, droits, population et limites |
| Cible | Appareil, système, architecture CPU, langage et environnement vérifiés |
| Qualité | Métrique principale, erreurs critiques, seuils à fixer avant le test final |
| Ressources | Taille, mémoire, latence, fréquence d’appel et budget d’entraînement |
| Référence | Règle, constante, modèle linéaire ou autre solution de comparaison |
| Repli | Comportement défini si l’entrée, le modèle ou le résultat est invalide |
| Fin de l’expérience | Critères observables, preuves attendues et décision à rendre |

Qualifier chaque champ : fourni, observé, ASSUMED ou UNKNOWN. Une inconnue bloque uniquement ce qui en dépend. Des données synthétiques peuvent vérifier une chaîne technique ; elles ne démontrent pas sa qualité sur un usage réel.

## 2. Choisir une famille adaptée

| Famille | Emploi possible | Point à contrôler |
|---|---|---|
| MLP compact | Variables numériques, classement, régression, classification | Normalisation, interactions utiles et comparaison simple |
| Petit CNN | Images réduites, spectrogrammes, motifs locaux | Résolution, extraction des caractéristiques et mémoire des activations |
| CNN temporel | Fenêtres de signaux ou d’événements | Longueur de fenêtre et absence de fuite depuis le futur |
| Petit RNN ou GRU | Séquences et contexte limité | Taille de l’état, remise à zéro et limites des séquences |
| Autoencodeur | Compression ou étude d’anomalies | Validation du seuil ; erreur de reconstruction distincte d’une probabilité |
| Réseau de politique | Score ou sélection parmi des actions bornées | Masque des actions, contraintes déterministes et repli |
| Réseau distillé | Étudiant entraîné à partir d’un enseignant | Provenance, coûts, droits et qualité propre de l’étudiant |

Un modèle de langage reste une option motivée par une tâche de langage. Il n’est ni la définition ni le point de départ obligatoire du projet. Évaluer également une référence non neuronale : un réseau plus complexe doit justifier son intérêt mesuré, ou être présenté comme une expérience pédagogique.

## 3. Exemple calculé : 844 paramètres

Considérons un MLP entièrement connecté, avec un biais par unité hors entrée : **16 → 32 → 8 → 4**.

\[
P=(16\times32+32)+(32\times8+8)+(8\times4+4)=844.
\]

Il contient 800 poids et 44 biais. Le stockage brut en FP32 représente 844 × 4 = **3 376 octets**, environ 3,30 Kio. Une représentation illustrative avec 800 poids INT8 et 44 biais INT32 représente **976 octets**, avant les échelles, points zéro et autres métadonnées. Ce format précis n’est pas garanti par tous les convertisseurs.

Le calcul dense comporte 800 multiplications-accumulations par passage, hors activations et autres traitements. Ces nombres décrivent une architecture fictive, pas un modèle entraîné. Le fichier exporté, la RAM totale, le moteur d’inférence et la latence sont des grandeurs distinctes. Aucun temps d’exécution ne peut être déduit de ce seul décompte.

## 4. Mesurer le système complet

Fixer les budgets nécessaires à la tâche ; conserver UNKNOWN pour les mesures absentes. Une cible proposée ne devient pas une observation.

| Grandeur | Mesure ou calcul à conserver |
|---|---|
| Paramètres | Total, poids, biais, types numériques et méthode de comptage |
| Artefact | Taille réelle du fichier et de ses éventuels fichiers associés |
| Distribution | Dépendances embarquées, bibliothèques natives, prétraitement |
| Mémoire | Mémoire des poids, activations, buffers, état et pic mesuré selon une portée explicitée |
| Latence | Initialisation séparée, appels à chaud, distribution et coût de bout en bout |
| Charge | Taille de lot, concurrence, fréquence d’appel et nombre d’instances |
| Entraînement | Durée, mémoire, matériel, nombre d’essais et coût connu |
| Énergie | Mesure instrumentée ou UNKNOWN ; aucune estimation présentée comme mesure |

Le protocole précise matériel, système, versions, threads, échauffement, répétitions et conditions de charge. Définir si la mesure inclut préparation des entrées, chargement, inférence et post-traitement. Publier les percentiles pertinents avec la taille de l’échantillon. Un percentile calculé sur quelques appels n’établit pas un comportement robuste.

Pour un jeu ou une application interactive, mesurer aussi l’effet cumulé de la fréquence d’appel. Une inférence acceptable isolément peut devenir coûteuse pour de nombreuses entités. Le choix événementiel, périodique ou par lot dépend du besoin, avec un plafond explicite.

## 5. Préparer des données et des séparations fiables

Documenter origine, permission d’utilisation, version, transformations et méthode d’identification des données. Une licence de code ne couvre pas automatiquement les données ou les poids. Ne pas introduire d’informations privées inutiles dans un dépôt. Un lien et une empreinte peuvent identifier des données stockées ailleurs lorsque cela est autorisé.

Séparer entraînement, validation et test avant les transformations apprises. Ajuster normalisation, sélection de variables, imputation et autres transformations sur l’entraînement seulement ; réutiliser ensuite ces paramètres. Réserver la validation aux choix et le test final à l’évaluation du candidat choisi. Une consultation répétée du test pour optimiser le modèle exige une nouvelle stratégie d’évaluation déclarée.

La documentation officielle [scikit-learn — Common pitfalls](https://scikit-learn.org/stable/common_pitfalls.html), consultée le 2026-10-20 — America/Toronto, décrit ces risques de fuite et l’application cohérente du prétraitement. Elle ne valide pas nos données.

Respecter les dépendances entre exemples : personne, session, monde, séquence, objet d’origine ou autre groupe pertinent. Pour prédire le futur, construire une séparation temporelle appropriée. Des fenêtres chevauchantes ou des variantes quasi identiques réparties entre ensembles peuvent surestimer la généralisation. Documenter exclusions, doublons, équilibre des classes et situations rares importantes.

## 6. Entraîner et comparer de manière reproductible

Commencer par une référence simple et un petit réseau flottant. Conserver code, configuration, dépendances, identité des données, graines aléatoires, optimiseur, fonction de perte, règles d’arrêt et sélection du meilleur candidat. Fixer les limites de durée et d’essais avant une recherche coûteuse. Les graines facilitent la répétition ; elles ne garantissent pas une identité bit à bit sur tous les matériels et moteurs.

Évaluer les candidats selon le même protocole. Choisir les métriques selon la tâche : erreurs par classe et précision/rappel pour une classification, erreur absolue ou quadratique pour une régression, qualité d’ordre pour un classement. Examiner aussi les échecs qui comptent dans l’application. Une moyenne globale peut masquer une classe rare ou un contexte défaillant.

Quand la variabilité peut changer la décision, répéter les essais avec un plan borné et rapporter dispersion ou incertitude appropriée. Ne pas choisir uniquement la meilleure graine. Conserver les essais infructueux pertinents et expliquer les exclusions. Une exécution réussie démontre que la procédure s’est terminée, pas que le modèle est utile.

## 7. Scores, confiance et décisions

Distinguer logits, scores de classement, sorties normalisées et probabilités calibrées. Un softmax élevé n’est pas une garantie de fiabilité. Si l’application utilise une probabilité ou un seuil de confiance, définir et évaluer la calibration sur des données adaptées, sans ajuster ce mécanisme sur le test final.

Documenter le sens d’un seuil et ses conséquences : abstention, référence déterministe, demande de données supplémentaires ou autre comportement défini. Tester entrées manquantes, non finies, hors plage, schéma incompatible et contexte inhabituel. Ne pas prétendre détecter toutes les données hors distribution sans preuve spécifique.

Les règles obligatoires restent hors du réseau : actions interdites, contraintes physiques, permissions, limites de ressources et validation de sortie. Un score appris ne peut pas autoriser une action que l’application refuse.

## 8. Réduire, convertir et vérifier

Optimiser contre une contrainte réelle : réduire les entrées, la largeur, la profondeur ou la résolution ; étudier ensuite distillation, quantification ou élagage si utile. Un poids nul ne réduit pas automatiquement le calcul ni la taille du format choisi. Tout gain annoncé doit correspondre à une représentation et à un moteur capables de l’exploiter.

La [publication originale sur la distillation](https://arxiv.org/abs/1503.02531), consultée le 2026-10-20 — America/Toronto, décrit le transfert de connaissances d’ensembles vers un modèle plus facile à déployer. Elle ne fournit aucun résultat pour notre candidat. Conserver séparément le coût et la provenance de l’enseignant.

La [documentation ONNX Runtime sur la quantification](https://onnxruntime.ai/docs/performance/model-optimizations/quantization.html), consultée le 2026-10-20 — America/Toronto, explique la calibration statique, le coût des paramètres calculés dynamiquement et les pertes possibles de précision. Choisir la technique selon les opérateurs et le matériel réellement pris en charge. Des poids moins précis ne garantissent pas une inférence plus rapide.

Pour chaque export, enregistrer format, versions, types, formes et opérateurs. Comparer les sorties avant/après conversion avec des tolérances définies, puis réévaluer la métrique métier. Utiliser une calibration représentative autorisée et distincte du test final. Conserver un artefact antérieur récupérable.

Effectuer un chargement et des prédictions dans le runtime cible, puis un benchmark sur le matériel cible ou indiquer explicitement que cette étape reste NOT_RUN. [LiteRT for Microcontrollers](https://developers.google.com/edge/litert/microcontrollers/overview), consulté le 2026-10-20 — America/Toronto, illustre une chaîne d’entraînement puis d’inférence embarquée avec opérations limitées ; ce runtime ne prend pas en charge l’entraînement sur l’appareil. Ce constat ne sélectionne pas LiteRT pour le projet.

## 9. Fiche modèle et trace d’exécution

Une fiche modèle accompagne chaque candidat partageable :

- Identité/version, statut, propriétaire et usage prévu ; usages non évalués.
- Schéma d’entrée/sortie, unités, ordre, normalisation et pré/post-traitement.
- Architecture, paramètres, précision, format et dépendances nécessaires.
- Données, séparation, provenance et statut des droits de code/données/poids.
- Métriques, références, ressources mesurées, matériel et principales erreurs.
- Artefact exact, empreinte, limites, repli et preuve d’acceptation éventuelle.

Une trace d’exécution contient : objectif ; commit et état des modifications locales ; configuration ; versions ; données et empreintes ; commande ; graines ; environnement ; temps observés ; résultat ; logs ; sorties et empreintes ; critères ; verdict ; limites. Utiliser le mécanisme d’identification déjà adopté par la gouvernance. Ne pas inventer un identifiant distant ou un statut d’approbation.

Chaque contrôle relie entrée, critère, observation, verdict et limites. Séparer revue statique, calcul, entraînement exécuté, export testé, benchmark et intégration. NOT_RUN décrit un contrôle absent ; UNKNOWN décrit une information inconnue. Aucun tableau prérempli ne transforme une cible en preuve.

## 10. Première chaîne P0 — proposition

P0 reste PROPOSED : valider une chaîne reproductible sur une petite tâche clairement identifiée, avec référence simple, MLP flottant, export et comparaison des prédictions. Un environnement CPU autorisé peut servir au démarrage ; aucun GPU ni service d’inférence distant n’est présupposé.

Critères proposés : schéma cohérent ; données reproductibles ; commandes documentées ; exécution bornée ; résultats observés ; artefact identifiable ; équivalence numérique contrôlée ; limites explicites. Une démonstration synthétique s’arrête à cette portée. L’utilité réelle demande ensuite un cas d’usage et une évaluation représentative. La quantification n’est ajoutée que si elle répond à un objectif concret. Aucun code, téléchargement, entraînement ou installation n’est lancé par l’adoption de cette référence.

## 11. Consommateurs et reprise après échec

EGO peut être un consommateur optionnel de scores ou politiques bornées ; son propriétaire conserve code, intégration, tests et publications. Un shuffle musical peut utiliser un score de transition, avec règles explicites sur répétitions et variantes d’une composition. Évaluer sur de nouvelles compositions exige une séparation par composition ; prédire des écoutes futures peut exiger une séparation temporelle. Aucun de ces cas n’est le premier usage approuvé.

Si une étape échoue, conserver la cause, les preuves et le dernier artefact exploitable. Réduire la portée, corriger le schéma, reprendre la référence ou essayer une variante justifiée. Bloquer uniquement la conclusion ou l’action dépendante. Ne pas masquer un échec d’export derrière les scores du modèle d’origine, ni annoncer une intégration après un simple test local.

Avant une adoption applicative, vérifier comportement de repli, limites de charge, compatibilité de version et possibilité de retour à la version précédente. La réussite technique ne remplace ni l’acceptation du propriétaire ni l’autorisation de diffusion.
