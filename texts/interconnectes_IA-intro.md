# Introduction

**LES PROJETS DOCUMENTES ICI SONT FICTIFS ET SERVENT A L'ELABORATION D'UN TRAVAIL EN COURS.**

Face à l’accélération des usages de l’IA et la diffusion massive de ces outils dans la vie publique, la commission numérique commune aux Interconnectés*, France urbaine et Intercommunalités de France s’est engagée en juillet 2023 à déployer la stratégie des « Intelligences Associées des territoires ». Elle vise à inscrire l’IA dans les exigences d’un numérique responsable.

Trois orientations complémentaires sont alors développées. 

•	L’IA au service des politiques publiques ; cet axe vise au recensement et à la documentation des projets portées par les collectivités. L’association travaille au développement d’une bibliothèque d’IA territoriale et à l’animation d’une communauté d’acteurs en partenariat avec Ecolab.

•	IA éthique et vie publique ; l’objectif est de mettre en débat les conditions de déploiement de ces systèmes et de faire remonter les attentes, points de vigilances, propositions à l’échelle des territoires. L’association a lancé le 18 septembre 2024 les concertations territoriales de l’IA qui encouragent le débat local et permettront de consolider une vision nationale commune.

•	IA et transformation des métiers de la fonction publique territoriale ; nourri par l’élaboration d’études, cet axe vise à identifier les impacts et à encadrer les usages de l’IA afin de s’assurer que l’humain reste au cœur du fonctionnement des collectivités. 

## Collecte et valorisation des usages de l’IA par les collectivités territoriales 

Cette bibliothèque s’inscrit pleinement dans la feuille de route de la commission qui permet de :

1. Recenser et qualifier les cas d’usages de systèmes d’IA dans les collectivités territoriales
2. Documenter les méthodes et les moyens déployés
3. Cartographier les acteurs et les solutions ressources
4. Documenter et partager des ressources techniques (codes, bases de do nées, modèles d’entraînement, …)
5. Répondre au besoin de transparence et d’explicabilité des al orithmes déployés au sein des collectivités territoriales

## Méthodologie

Un travail collectif, regroupant plusieurs agents et élus de collectivités territoriales, a permis de préciser les besoins et les usages de cette bibliothèque. Ensemble, un modèle de données visant à structurer la documentation des projets ayant recours à l’IA a été produit.  

## A propos des Interconnectés 

*Les Interconnectés est la première association nationale de collectivités centrée sur les politiques publiques numériques. Créée en 2009 par Intercommunalités de France et France urbaine, sa mission est d’accompagner les collectivités locales et leurs groupements pour mettre l’innovation et le numérique au service des territoires. Elle est aussi un interlocuteur de référence de l’État. Elle mobilise différents acteurs afin de faire émerger des solutions concrètes fondées sur le partage, l’intelligence collective et la proximité de l’usager.

## Modèle de données

| NOM | CHAMP | CATEGORIE | TYPE | REQUIS | DESCRIPTION |
|---|---|---|---|---|---|
| Porteur | coll_nom | INFORMATION GENERALE | string | yes | Nom de la collectivité ou de l'organisation porteuse du projet |
| Projet | nom_projet | INFORMATION GENERALE | string | yes | Nom du projet ou du service déployé |
| Identifiant SIRET de la collectivité | coll_siret | INFORMATION GENERALE | number | yes | Identifiant du Système d’Identification du Répertoire des Etablissements (SIRET) de la collectivité qui a adopté la délibération, composé de 9 chiffres SIREN + 5 chiffres NIC d’un seul tenant |
| Type de collectivité | coll_type | INFORMATION GENERALE | enum | yes | Commune, EPCI, département, région, syndicat mixte, opérateur |
| Date de démarrage du projet | projet_date | INFORMATION GENERALE | date | yes | Date de démarrage du projet (JJ/MM/AAAA) ou (MM/AAAA) |
| Maturité | projet_status | INFORMATION GENERALE | enum | yes | En expérimentation, En déploiement, Terminée, Abandonné |
| Description d'un projet abandonné | status_abandon | INFORMATION GENERALE | string | no | Si échec du projet, expliquer les barrières |
| Partenaires associés | partenaires | INFORMATION GENERALE | string | no | Liste des autres partenaires académiques, experts, techniques, financeurs associés |
| Contact du service en charge | projet_contact | INFORMATION GENERALE | email | no | Indiquez l'email du contact ou du service en charge du service (DPO, etc.) |
| Financement | financement | INFORMATION GENERALE | string | no | Identifier le guichet de financement (interne, Fond vert, CRTE, France 2030, FEDER, DIAT, …) |
| Budget | budget | INFORMATION GENERALE | enum | no | /an : moins de 50k€ , de 50k€ à 100k€,  plus de 100k€ |
| Description gobal du service et de ses usages | usage_description | INFORMATION GENERALE | string | yes | A quoi sert ce service ? Quels bénéfices attendus ?  |
| Développement et mise en œuvre | mise_en_oeuvre | INFORMATION GENERALE | enum | yes | Projet développé en interne, projet développé en externe, mobilisation de prestataire(s), marché public |
| Thème principal  | theme | INFORMATION GENERALE | enum | yes | quelle grande politique publique est adressée par ce cas d'usages (voir thèmes feuille2) |
| Sous-thèmes  | sous_theme | INFORMATION GENERALE | enum | no | sélectionner un ou deux items dans la liste proposée (voir sous-thèmes feuille2) |
| Audience du service | audience_service | INFORMATION GENERALE | enum | yes | grand public, bénéficiaire, agent, association, élu, entreprises, collectivités, établissement scolaire, établissement santé |
| Hébergement du service | herbergement | INFORMATION GENERALE | enum | yes | Indiquez comment sont hébergée les données : cloud chez un tiers, en interne de l'administration, NSP |
| Nom de l’algorithme | nom_algorithme | ALGORITHME | string | yes | S’il n’en a pas, indiquer la décision mise en oeuvre. Exemple : réservation et accès crèche. |
| Description gobal de l'algorithme | algorithme_description | ALGORITHME | string | no | À quoi sert cet algorithme ? Quelles sont les tâches à accomplir? |
| Opérations effectuées par l’algorithme | algorithme_operations | ALGORITHME | string | no | Donnez des détails sur les opérations techniques effectuées par l’algorithme. Cette catégorie peut être simple ou complexe, en fonction du type d’algorithme mobilisé. |
| Type d'algorithme | type_algorithme | ALGORITHME | enum | yes | Machine Learning, Traitement Automatique du langage, IA générative, Computer vision, Réseaux de neurones, NSP |
| Evaluation de l'impact environnemental | impact_environnement | ALGORITHME | string | no | Indiquez le score ou impact environnemental de l'algorithme (GreenAlgorithm) |
| Source des données | donnees_source | DATA | enum | yes | Qui fournit les données nécessaires à l'entraîment et à l'utilisation du modèle (l’usager, jeu de données interne, open data, données d'un tiers , NSP) ? |
| Mode de collecte et d'accès des données traitées | donnees_acces | DATA | enum | yes | Comment les données sont‑elles initialement collectées et mise à jour ? Exemple : “par API, automatisée, par récupération manuelle, NSP”. |
| Evaluation des risques | risque | CAS D'USAGE | string | no | Indiquez quelle évaluation des risques a été utilisée et donnez un aperçu des risques et des mesures d'atténuation.  |
| Type de risque | risque_categorie | CAS D'USAGE | enum | no | Classification de la catégorie de risque pour cette utilisation de l'algorithme |
| Proportionnalité | proportionalite | CAS D'USAGE | string | no | Expliquer pourquoi l'utilisation de l'algorithme est nécessaire. Évaluation du bénéfice par rapport à une solution alternative sans Intelligence Artificielle |
| Portée de la décision | decision | CAS D'USAGE | string | no | Préciser si la décision a une portée externe (par exemple : pour un usager) ou concerne une procédure interne (par exemple : traitement de la mobilité des agents). Voir nombre de décisions |
| Efficacité du système d'IA | erreur | EVALUATION | enum | no | Ecart entre les objectifs attendus et les résultats du système d’IA 1- (faible) le système d’IA répond bien aux objectifs attendus2- (moyen) le système d’IA répond partiellement aux objectifs attendus3- (fort) le système d’IA ne répond pas aux objectifs attendus<br> |
| Niveau d’explicabilité de l’algorithme | explicabilite | EVALUATION | enum | no | 1- (faible) Facilement explicable au public 2- (moyen) Explicable mais complexe 3- (fort) Non explicable au public  |
| Réversibilité des traitements et des services | reversibilite | EVALUATION | string | no | Indiquez s'il est possible d'annuler complètement les effets de l'algorithme si nécessaire ? Que faut-il pour cela ? |
| Procédure d'objection | objection | EVALUATION | string | no | Décrivez de quelle manière les personnes peuvent s'opposer à l'utilisation ou au résultat de l'algorithme. |
| URL information | url_infos | INFORMATION GENERALE | url | no | Insérer un lien vers le projet (information ou accès au service) |
| URL ressource | url_ressources | INFORMATION GENERALE | url | no | Insérer un lien vers des ressources techniques (algorithme, base de donnée, modèle d'entraînement...) |
| image | image_url | INFORMATION GENERALE | image | yes | Insérer le logo de la collectivité porteuse du projet |
| Date de mise à jour des informations | date | METADATA | date | yes | date de mise à jour des informations (JJ/MM/AAAA) |
