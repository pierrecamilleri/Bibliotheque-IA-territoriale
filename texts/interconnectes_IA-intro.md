# Introduction

**LES PROJETS DOCUMENTES ICI SONT FICTIFS ET SERVENT A L'ELABORATION D'UN TRAVAIL EN COURS.**

Face à l’accélération des usages de l’IA et la diffusion massive de ces outils dans la vie publique, la commission numérique commune aux Interconnectés*, France urbaine et Intercommunalités de France s’est engagée en juillet 2023 à déployer la stratégie des « Intelligences Associées des territoires ». Elle vise à inscrire l’IA dans les exigences d’un numérique responsable.

Trois orientations complémentaires sont alors développées. 

•	L’IA au service des politiques publiques ; cet axe vise au recensement et à la documentation des projets portées par les collectivités. L’association travaille au développement d’une bibliothèque d’IA territoriale et à l’animation d’une communauté d’acteurs en partenariat avec Ecolab.

•	IA éthique et vie publique ; l’objectif est de mettre en débat les conditions de déploiement de ces systèmes et de faire remonter les attentes, points de vigilances, propositions à l’échelle des territoires. L’association a lancé le 18 septembre 2024 les concertations territoriales de l’IA qui encouragent le débat local et permettront de consolider une vision nationale commune.

•	IA et transformation des métiers de la fonction publique territoriale ; nourri par l’élaboration d’études, cet axe vise à identifier les impacts et à encadrer les usages de l’IA afin de s’assurer que l’humain reste au cœur du fonctionnement des collectivités. 

## Collecte et valorisation des usages de l’IA par les collectivités territoriales 

Cette bibliothèque s’inscrit pleinement dans la feuille de route de la commission qui permet de :

1.	Recenser et qualifier les cas d’usages de systèmes d’IA dans les collectivités territoriales
2.	Documenter les méthodes et les moyens déployés
3.	Cartographier les acteurs et les solutions ressources
4.	Documenter et partager des ressources techniques (codes, bases de données, modèles d’entraînement, …)
5.	Répondre au besoin de transparence et d’explicabilité des algorithmes déployés au sein des collectivités territoriales

## Méthodologie

Un travail collectif, regroupant plusieurs agents et élus de collectivités territoriales, a permis de préciser les besoins et les usages de cette bibliothèque. Ensemble, un modèle de données visant à structurer la documentation des projets ayant recours à l’IA a été produit.  

## A propos des Interconnectés 

*Les Interconnectés est la première association nationale de collectivités centrée sur les politiques publiques numériques. Créée en 2009 par Intercommunalités de France et France urbaine, sa mission est d’accompagner les collectivités locales et leurs groupements pour mettre l’innovation et le numérique au service des territoires. Elle est aussi un interlocuteur de référence de l’État. Elle mobilise différents acteurs afin de faire émerger des solutions concrètes fondées sur le partage, l’intelligence collective et la proximité de l’usager.

## Modèle de données

| NOM | CHAMP | CATEGORIE | TYPE | REQUIS | DESCRIPTION |
|-------------|-------|-------|---|---|---------------------------------------------------------------|
| Porteur| coll_nom| INFORMATION ADMINISTRATION | string | yes| Nom de la collectivité ou de l'organisation porteuse du projet|
| Projet | nom_projet| INFORMATION ADMINISTRATION | string | yes| Nom du projet ou du service déployé |
| Identifiant SIRET de la collectivité | coll_siret| INFORMATION ADMINISTRATION | number | yes| Identifiant du Système d’Identification du Répertoire des Etablissements (SIRET) de la collectivité qui a adopté la délibération, composé de 9 chiffres SIREN + 5 chiffres NIC d’un seul tenant |
| Type de collectivité | coll_type | INFORMATION ADMINISTRATION | enum | yes| Commune, EPCI, département, région, syndicat mixte, opérateur |
| Date de démarrage du projet| projet_date | INFORMATION ADMINISTRATION | date | yes| Date de démarrage du projet (JJ/MM/AAAA) ou (MM/AAAA) |
| Maturité | projet_status | INFORMATION ADMINISTRATION | enum | yes| Sélectionner un item : en réflexion, en construction, POC, en déploiement, terminée, abandonné|
| Description d'un projet abandonné| status_abandon| INFORMATION ADMINISTRATION | string | no | Si échec du projet, expliquer les barrières |
| Partenaires associés | partenaires | INFORMATION ADMINISTRATION | string | yes| Liste des autres partenaires académiques, experts, techniques, financeurs associés|
| Contact du service en charge | projet_contact| INFORMATION ADMINISTRATION | email| yes| Indiquez l'email du contact ou du service en charge du service (DPO, etc.)|
| Description gobal du service et de ses usages| usage_service | CAS D'USAGE| string | yes| A quoi sert ce service ? Quels bénéfices attendus ? |
| Politique publique visée | theme | CAS D'USAGE| enum | yes| quelle grande politique publique est adressée par ce cas d'usages (voir thèmes BDT) |
| Sous-thèmes de politique publique visée| sous_theme| CAS D'USAGE| enum | no | sélectionner un ou deux items dans la liste proposée (voir sous-thèmes BDT) |
| Cible du service | cible_service | CAS D'USAGE| enum | yes| grand public, bénéficiaire, agent, association, élu, entreprises, collectivités, établissement scolaire, établissement santé|
| Evaluation des risques | risque| CAS D'USAGE| string | no | Indiquez quelle évaluation des risques a été utilisée et donnez un aperçu des risques et des mesures d'atténuation. |
| Type de risque | risque_categorie| CAS D'USAGE| enum | yes| Classification de la catégorie de risque pour cette utilisation de l'algorithme |
| Proportionnalité | proportionalite | CAS D'USAGE| string | no | Expliquer pourquoi l'utilisation de l'algorithme est nécessaire. Évaluation du bénéfice par rapport à une solution alternative sans Intelligence Artificielle |
| Portée de la décision| decision| CAS D'USAGE| string | yes| Préciser si la décision a une portée externe (par exemple : pour un usager) ou concerne une procédure interne (par exemple : traitement de la mobilité des agents). Voir nombre de décisions|
| Public concerné par la décision| audience_decision | CAS D'USAGE| string | no | Qui est affecté par cette décision ? Est‑ce que la décision emporte des effets importants sur ce public ? |
| Hébergement du service | herbergement| CAS D'USAGE| string | yes| Indiquez comment sont hébergée les données : cloud chez un tiers, en interne de l'administration|
| Nom de l’algorithme| nom_algorithme| ALGORITHME | string | yes| S’il n’en a pas, indiquer la décision mise en oeuvre. Exemple : réservation et accès crèche.|
| Description gobal de l'algorithme| description | ALGORITHME | string | yes| Pourquoi une décision administrative est‑elle prise? Qui sont les acteurs de la décision? Quelles sont les tâches à accomplir?|
| Finalité de l'algorithme | usage_algorithme| ALGORITHME | string | yes| À quoi sert cet algorithme?Cette catégorie peut également comporter des éléments dejustification : pourquoi un algorithme a‑t‑il été utilisé dans ce processus? |
| Impact de l'algorithme sur la décision | impact_algorithme | ALGORITHME | string | no | Pour effectuer lesdites tâches, à quel moment s’insère l’algorithme dans le processus de décision ? Quel est le processus complet et quelle(s) partie(s) l’algorithme prend‑il en charge ?|
| Niveau d’automatisation de la décision | automatisation_decision | ALGORITHME | enum | no | Préciser si la décision est entièrement automatisée ou s’il s’agit d’un outil d’aide à la décision; automatisation complète, assistée, aide à la décision)|
| Opérations effectuées par l’algorithme | operations| ALGORITHME | string | no | Donnez des détails sur les opérations techniques effectuées par l’algorithme. Cette catégorie peut être simple ou complexe, en fonction du type d’algorithme mobilisé.|
| Type d'algorithme| type_algorithme | ALGORITHME | enum | yes| Machine Learning, Traitement Automatique du langage, IA générative, Computer vision, Réseaux de neurones|
| Source des données | donnees_source| DATA | string | yes| Qui fournit les données (l’usager, une autre administration, etc.)? Comment sont elles fournies (un dossier, une API, etc.)? Exemple : “dossier rempli par le demandeur sur une plateforme en ligne” ou “revenu fiscal de référence fourni par la DGFIP”. |
| Mode de collecte des données traitées| donnees_collecte| DATA | string | yes| Comment les données sont‑elles initialement collectées ? Exemple : “Les inscriptions sont très majoritairement prises en charge au sein d’un portail virtuel dédié aux familles, plus exceptionnellement par voie papier”.|
| Biais de traitement| monitoring_biais| SURVEILLANCE | string | no | Indiquez si les données mobilisées comportent des biaiset si des procédures sont déployées pour les compenser |
| Evaluation de l'impact social et environnemental | monitoring_impact | SURVEILLANCE | string | yes| Indiquez le score ou impact environnemental de l'algorithm (GreenAlgorithm) et social du service et quels mesures sont déployées pour les compenser (comité de surveillance, etc.)|
| Réversibilité des traitements et des services| reversibilite | SURVEILLANCE | string | no | Indiquez s'il est possible d'annuler complètement les effets de l'algorithme si nécessaire ? Que faut-il pour cela ?|
| Procédure d'objection| objection | SURVEILLANCE | string | no | Décrivez de quelle manière les personnes peuvent s'opposer à l'utilisation ou au résultat de l'algorithme.|
| Date de mise à jour des informations | date| METADATA | date | yes| date de mise à jour des informations (JJ/MM/AAAA) |
