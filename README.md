
Face à l’accélération des usages de l’IA et la diffusion massive de ces outils dans la vie publique, la commission numérique commune aux Interconnectés*, France urbaine et Intercommunalités de France s’est engagée en juillet 2023 à déployer la stratégie des « Intelligences Associées des territoires ». Elle vise à inscrire l’IA dans les exigences d’un numérique responsable.

Trois orientations complémentaires sont alors développées. 

- L’IA au service des politiques publiques ; cet axe vise au recensement et à la documentation des projets portées par les collectivités. L’association travaille au développement d’une bibliothèque d’IA territoriale et à l’animation d’une communauté d’acteurs en partenariat avec Ecolab.

- IA éthique et vie publique ; l’objectif est de mettre en débat les conditions de déploiement de ces systèmes et de faire remonter les attentes, points de vigilances, propositions à l’échelle des territoires. L’association a lancé le 18 septembre 2024 les concertations territoriales de l’IA qui encouragent le débat local et permettront de consolider une vision nationale commune.

- IA et transformation des métiers de la fonction publique territoriale ; nourri par l’élaboration d’études, cet axe vise à identifier les impacts et à encadrer les usages de l’IA afin de s’assurer que l’humain reste au cœur du fonctionnement des collectivités. 

## Collecte et valorisation des usages de l’IA par les collectivités territoriales 

Cette bibliothèque s’inscrit pleinement dans la feuille de route de la commission qui permet de :

1. Recenser et qualifier les cas d’usages de systèmes d’IA dans les collectivités territoriales
2. Documenter les méthodes et les moyens déployés
3. Cartographier les acteurs et les solutions ressources
4. Documenter et partager des ressources techniques (codes, bases de données, modèles d’entraînement, …)
5. Répondre au besoin de transparence et d’explicabilité des algorithmes déployés au sein des collectivités territoriales

## Méthodologie

Un travail collectif, regroupant l’Ecolab du CGDD et la Banque des Territoires ainsi qu’un noyau d’agents et d’élus de collectivités territoriales, a permis de préciser les besoins et les usages de cette bibliothèque. 

Un premier cahier des charges a été produit en 2023 pour anticiper les usages types et les rôles nécessaires au maintien de cette bibliothèque. Ensemble, nous avons ainsi élaboré au dernier trimestre 2024 un modèle de données visant à structurer la documentation des projets ayant recours à l’IA.

Pour nourrir ce travail, nous avons croisé plusieurs travaux réglementaires mais aussi de recensement de projets d’IA territoriales que nous avons identifiés en France mais aussi à l’international. Aussi, dans une logique de convergence entre les ressources existantes, nous avons pris soin de reprendre des nomenclatures déjà utilisées par nos partenaires, à l’instar des critères d’identification des thèmes de cas d’usages notamment. 

Les cas d’usages documentés s’articulent autour de 6 thématiques principales. 

* Transformation écologique et énergétique
* Attractivité et développement
* Citoyenneté, santé, et solidarité
* Mobilités
* Gouvernance et socles technologiques
* Administration et organisation interne


En complément de déploiements de services ayant recours à l’IA et d’expérimentations, le sujet de l’IA s’installe avant tout pour les territoires dans les enjeux de gouvernance et d'évaluation de ces usages. Les collectivités territoriales sont nombreuses à développer, au-delà de critères d’évaluation et d’arbitrages techniques du recours à l’IA, des chartes et des stratégies IA/Data, qui viennent outiller les questions éthiques, juridiques et organisationnelles de ces usages. Cette bibliothèque d’IA territoriale permet aussi de les identifier et de les valoriser. 


## A propos des Interconnectés

*Les Interconnectés est la première association nationale de collectivités centrée sur les politiques publiques numériques. Créée en 2009 par Intercommunalités de France et France urbaine, sa mission est d’accompagner les collectivités locales et leurs groupements pour mettre l’innovation et le numérique au service des territoires. Elle est aussi un interlocuteur de référence de l’État. Elle mobilise différents acteurs afin de faire émerger des solutions concrètes fondées sur le partage, l’intelligence collective et la proximité de l’usager.

## Modèle de donnée

| NOM                                              | CHAMP                  | CATEGORIE            | TYPE   | REQUIS | DESCRIPTION                                                                                                                                                                                     | ACCES     |
|--------------------------------------------------|------------------------|----------------------|--------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Porteur                                          | coll_nom               | INFORMATION GENERALE | string | yes    | Nom de la collectivité ou de l'organisation porteuse du projet                                                                                                                                  | Public    |
| Projet                                           | nom_projet             | INFORMATION GENERALE | string | yes    | Nom du projet ou du service déployé                                                                                                                                                             | Public    |
| Identifiant SIRET de la collectivité             | coll_siret             | INFORMATION GENERALE | number | yes    | Identifiant du Système d’Identification du Répertoire des Etablissements (SIRET) de la collectivité qui a adopté la délibération, composé de 9 chiffres SIREN + 5 chiffres NIC d’un seul tenant | Public    |
| Type de collectivité                             | coll_type              | INFORMATION GENERALE | enum   | yes    | Commune,  Métropole, EPCI, département, région, syndicat mixte, opérateur                                                                                                                       | Public    |
| Date de démarrage du projet                      | projet_date            | INFORMATION GENERALE | date   | yes    | Date de démarrage du projet MM/AAAA                                                                                                                                                             | Public    |
| Maturité                                         | projet_status          | INFORMATION GENERALE | enum   | yes    | En expérimentation, En déploiement, Terminée, Abandonné                                                                                                                                         | Public    |
| Description d'un projet abandonné                | status_abandon         | INFORMATION GENERALE | string | no     | Si échec du projet, expliquer les raisons et les difficultés                                                                                                                                    | Public    |
| Partenaires associés                             | partenaires            | INFORMATION GENERALE | string | no     | Liste des partenaires (académiques, experts, techniques, financeurs,..) associés                                                                                                                | Public    |
| Contact du service en charge                     | projet_contact         | INFORMATION GENERALE | email  | no     | Indiquez l'email du contact ou du service en charge du suivi de ce projet                                                                                                                       | Restreint |
| Financement                                      | financement            | INFORMATION GENERALE | string | no     | Identifier le guichet de financement (interne, Fond vert, CRTE, France 2030, FEDER, DIAT, …)                                                                                                    | Restreint |
| Budget                                           | budget                 | INFORMATION GENERALE | enum   | no     | Indiquer le budget annuel dédié à ce service (ordre de grandeur) : moins de 50k€ , de 50k€ à 100k€,  plus de 100k€                                                                              | Restreint |
| Description gobal du service et de ses usages    | usage_description      | INFORMATION GENERALE | string | yes    | A quoi sert ce service ? Quels bénéfices attendus ?                                                                                                                                             | Public    |
| Développement et mise en œuvre                   | mise_en_oeuvre         | INFORMATION GENERALE | enum   | yes    | Projet développé en interne, projet développé en externe, mobilisation de prestataire(s), marché public                                                                                         | Restreint |
| Thème principal                                  | theme                  | INFORMATION GENERALE | enum   | yes    | Sélectionner un thème principal                                                                                                                                                                 | Public    |
| Sous-thèmes                                      | sous_theme             | INFORMATION GENERALE | enum   | no     | Sélectionner jusqu'à deux sous-thèmes                                                                                                                                                           | Public    |
| Audience du service                              | audience_service       | INFORMATION GENERALE | enum   | yes    | Sélectionner à qui s'adresse l'usage de ce service : grand public, bénéficiaire, agent, association, élu, entreprises, collectivités, établissement scolaire, établissement santé               | Public    |
| Hébergement du service                           | herbergement           | INFORMATION GENERALE | enum   | yes    | Indiquez comment sont hébergée les données : cloud chez un tiers, en interne de l'administration, NSP                                                                                           | Restreint |
| Nom de l’algorithme                              | nom_algorithme         | ALGORITHME           | string | yes    | S’il n’en a pas, indiquer la décision mise en oeuvre. Exemple : réservation et accès crèche.                                                                                                    | Restreint |
| Description gobal de l'algorithme                | algorithme_description | ALGORITHME           | string | no     | À quoi sert cet algorithme ? Quelles sont les tâches à accomplir?                                                                                                                               | Restreint |
| Opérations effectuées par l’algorithme           | algorithme_operations  | ALGORITHME           | string | no     | Donnez des détails sur les opérations techniques effectuées par l’algorithme. Cette catégorie peut être simple ou complexe, en fonction du type d’algorithme mobilisé.                          | Restreint |
| Type d'algorithme                                | type_algorithme        | ALGORITHME           | enum   | yes    | Sélectionner le type d'algorithme : Machine Learning, Traitement Automatique du langage, IA générative, Computer vision, Réseaux de neurones, NSP                                               | Restreint |
| Evaluation de l'impact environnemental           | impact_environnement   | ALGORITHME           | string | no     | Indiquer le score ou impact environnemental de l'algorithme (GreenAlgorithm)                                                                                                                    | Restreint |
| Source des données                               | donnees_source         | DATA                 | enum   | yes    | Qui fournit les données nécessaires à l'entraîment et à l'utilisation du modèle (l’usager, jeu de données interne, open data, données d'un tiers , NSP) ?                                       | Restreint |
| Mode de collecte et d'accès des données traitées | donnees_acces          | DATA                 | enum   | yes    | Comment les données sont‑elles initialement collectées et mise à jour ? Exemple : “par API, automatisée, par récupération manuelle, NSP”.                                                       | Restreint |
| URL information                                  | url_infos              | INFORMATION GENERALE | url    | no     | Insérer un lien vers le projet (information ou accès au service)                                                                                                                                | Public    |
| URL ressource                                    | url_ressources         | INFORMATION GENERALE | url    | no     | Insérer un lien vers des ressources techniques (algorithme, base de donnée, modèle d'entraînement...)                                                                                           | Restreint |
| image                                            | image_url              | INFORMATION GENERALE | image  | yes    | Insérer le lien vers le logo de la collectivité porteuse du projet                                                                                                                              | Public    |
| longitude                                        | longitude              | INFORMATION GENERALE | number | yes    | longitude du siège social de l'organisation porteuse                                                                                                                                            | Public    |
| latitude                                         | latidude               | INFORMATION GENERALE | number | yes    | latitude du siège social de l'organisation porteuse                                                                                                                                             | Public    |
| Date de mise à jour des informations             | date                   | METADATA             | date   | yes    | date de mise à jour des informations (JJ/MM/AAAA)                                                                                                                                               | Public    |

---

## To go further

### Datami

The widget is an integral part of the [Datami](https://gitlab.com/multi-coop/datami) project

### Technical documentation

A site dedicated to Datami technical documentation can be consulted here: https://datami-docs.multi.coop

---

## Mini server for local development

A mini server is writen in the `server.py` to serve this folder's files.

To install the mini-server :

```sh
pip install --upgrade pip
python3 -m pip install --user virtualenv
python3 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

or

```sh
sh setup.sh
source venv/bin/activate
```

---

### Run local server

To run the server on `http://localhost:8810`:

```sh
python server.py
```

or

```sh
sh run_server.sh
```

Files will be locally served on :

- `http://localhost:8810/content/<path:folder_path>/<string:filename>`
- `http://localhost:8810/statics/<path:folder_path>/<string:filename>`

---

## Crédits

| | logo | url |
| :-: | :-: | :-: |
| **Les Interconnectés** | ![Interconnectés](./images/interconnectes-logo.jpg) | https://www.interconnectes.com/ |
