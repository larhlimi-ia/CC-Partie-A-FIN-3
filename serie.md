── LARHLIMI.jpg
├── CC-Partie A Consignes_29_Algorithmes_Machine_Learning.md (1600 tokens)
├── Consignes_ML.md (1600 tokens)
├── enonce_TP_ML_finance_S7.md (9900 tokens)
└── CC-Partie A.ipynb (35200 tokens)


/LARHLIMI.jpg:
--------------------------------------------------------------------------------
https://raw.githubusercontent.com/larhlimi-ia/CC-Partie-A-FIN-3/HEAD/LARHLIMI.jpg


--------------------------------------------------------------------------------
/CC-Partie A Consignes_29_Algorithmes_Machine_Learning.md:
--------------------------------------------------------------------------------
 1 | # Travail demandé — Étude et expérimentation de 29 algorithmes de Machine Learning
 2 | 
 3 | **Public :** S7 — **Organisation :** Individuel — **Support :** ce notebook Google Colab.
 4 | 
 5 | ## Objectif général
 6 | 
 7 | À partir des **29 algorithmes présentés dans ce notebook**, compléter la partie théorique et enrichir les expériences pratiques afin de comprendre **le principe de chaque algorithme, son fonctionnement, les contextes dans lesquels il est pertinent et ses performances sur des données réelles**.
 8 | 
 9 | > **Important :** les cellules Python déjà présentes constituent des **exemples de démonstration**. Plusieurs utilisent des **données synthétiques** : elles ne suffisent donc pas à satisfaire l'exigence finale de tests sur données réelles. Vous devez conserver les exemples, ajouter vos propres explications et réaliser ensuite les expérimentations demandées.
10 | 
11 | 
12 | ## Partie A — Questions à traiter pour **chaque algorithme** (1 à 29)
13 | 
14 | **Q1. Présentation de l'algorithme.** Rédigez une présentation synthétique (8 à 12 lignes) précisant :
15 | - son **nom** en français et en anglais, sa **famille** (régression, classification, clustering, réduction de dimension, détection d'anomalies ou renforcement) et l'objectif poursuivi ;
16 | - son **intuition** et les étapes principales : données en entrée → apprentissage / calcul → prédiction, regroupement ou décision en sortie ;
17 | - **une formule ou un critère mathématique essentiel** lorsque cela est pertinent, en **définissant tous les symboles** et en distinguant paramètres et hyperparamètres ;
18 | - deux avantages et deux limites.
19 | 
20 | **Q2. Schéma explicatif.** Créez **au moins un schéma original, lisible et légendé** montrant son principe (diagramme de flux, arbre, frontière de décision, nuage de points, mise à jour de centroïdes, agrégation d'arbres, boucle agent–environnement, etc.). Insérez-le dans le notebook, avec **un commentaire expliquant comment le lire**. Vous pouvez utiliser Matplotlib ou intégrer une image créée par vos soins. Indiquez la source si vous adaptez une figure publiée.
21 | 
22 | **Q3. Contexte d'utilisation.** Identifiez :
23 | - **deux cas d'usage concrets**, dont au moins un en **finance, gestion, commerce international, marketing ou logistique** ;
24 | - la nature des données et les prérequis techniques ;
25 | - un cas dans lequel l'algorithme serait **peu approprié**, en expliquant pourquoi ;
26 | - les métriques adaptées pour juger ses résultats.
27 | 
28 | **Q4. Commentaire du code.** Exécutez le code fourni, expliquez en quelques lignes les entrées, les hyperparamètres, la sortie obtenue et **ce que la sortie permet — ou ne permet pas — de conclure**. N'inventez aucune métrique ni aucun résultat.
29 | 
30 | **À insérer sous chaque titre d'algorithme :** quatre sous-sections Markdown `Présentation`, `Schéma explicatif`, `Contextes d'utilisation`, `Analyse de l'expérience Python`.
31 | 
32 | 
33 | ## Partie B — Expérimentation finale sur des **données réelles**
34 | 
35 | **Q5. Choix et traçabilité des données.** Sélectionnez des jeux de données **publics et réels**, adaptés aux différentes familles ; notez pour chacun **nom, organisme source, URL exacte, licence/conditions d'accès, taille, colonnes, cible éventuelle et date de consultation**. Un même dataset peut servir à plusieurs algorithmes **compatibles**, mais pas à des tâches artificiellement différentes. **Ne pas utiliser de données inventées ou simulées pour cette partie.**
36 | 
37 | Sources possibles (vérifiez l'accès effectif et la correspondance avec la tâche) :
38 | - [UCI Machine Learning Repository](https://archive.ics.uci.edu/) — ex. [Default of Credit Card Clients](https://archive.ics.uci.edu/dataset/350), [Online Retail](https://archive.ics.uci.edu/dataset/352) ;
39 | - [OpenML](https://www.openml.org/) ;
40 | - [Banque mondiale, indicateurs](https://data.worldbank.org/) ;
41 | - [UN Comtrade](https://comtradeplus.un.org/) — données de commerce international, extraction à documenter.
42 | 
43 | **Q6. Préparation.** Chargez les données dans Pandas ; expliquez les valeurs manquantes, types, doublons, valeurs extrêmes et éventuel déséquilibre de classes. Évitez la fuite d'information en ajustant tout prétraitement appris **sur l'entraînement uniquement**.
44 | 
45 | **Q7. Expériences.** Testez **chaque algorithme applicable sur un jeu de données réel approprié**. Pour les algorithmes supervisés, séparez entraînement, validation et test ; pour les séries temporelles, utilisez une **validation chronologique**. Pour les méthodes non supervisées, expliquez les critères internes et, si des étiquettes réelles existent, utilisez-les seulement pour une évaluation externe. Pour les bandits, Q-learning, SARSA et DQN, utilisez des **environnements publics Gymnasium** plutôt qu'un CSV fixe : les trajectoires observées sont générées par l'interaction ; distinguez cette simulation d'un dataset réel. Le DQN du notebook est **conceptuel** : une expérience DQN complète est facultative et doit être signalée comme telle.
46 | 
47 | **Q8. Comparaison et interprétation.** Pour chaque famille, comparez au moins une **méthode de référence** et une méthode avancée :
48 | - régression : MAE, RMSE, R² ;
49 | - classification : F1, rappel, précision, ROC-AUC ou PR-AUC selon la tâche ;
50 | - clustering : silhouette, stabilité et interprétation ;
51 | - réduction de dimension : variance expliquée (ACP), conservation des voisinages (t-SNE/UMAP) ;
52 | - anomalies : qualité des alertes, et précision/rappel uniquement si des étiquettes fiables sont disponibles ;
53 | - renforcement : récompense cumulée, taux de réussite et variation entre graines.
54 | 
55 | Présentez vos résultats dans des **tableaux comparatifs** et des **figures légendées**, puis discutez performance, coût de calcul, interprétabilité et limites. Fixez les graines (`random_state=42` lorsque possible), donnez les versions des bibliothèques et évitez de régler les paramètres sur le test final.
56 | 
57 | 
58 | ## Partie C — Livrables et critères de réussite
59 | 
60 | **À remettre par chaque binôme :**
61 | 1. Ce notebook `.ipynb` complété avec **les réponses Q1–Q4 pour les 29 algorithmes**, des schémas et les sorties d'exécution ;
62 | 2. Les expériences supplémentaires **Q5–Q8**, avec jeux de données publics cités et comparaisons reproductibles (ou justification claire des incompatibilités / limites pour les méthodes de renforcement) ;
63 | 3. Un **rapport de synthèse** (5 à 8 pages) présentant les principales conclusions, le tableau comparatif final et les références ;
64 | 4. Une **courte démonstration orale** où les deux membres expliquent leurs contributions.
65 | 
66 | **Barème indicatif /20 :** présentation et exactitude scientifique (5), schémas originaux et pédagogiques (4), pertinence des contextes d'utilisation (3), rigueur des essais réels et des métriques (5), reproductibilité et qualité de restitution (3).
67 | 
68 | **Points de vigilance :** ne pas recopier les définitions sans les comprendre ; ne pas inventer de résultats ; ne pas appeler « données réelles » les jeux synthétiques du notebook ; ne pas évaluer des algorithmes incompatibles sur la même cible ; citer vos sources et documenter l'éventuel usage d'une IA.
69 | 
70 | ---
71 | 
72 | ## Support d'expérimentation — exemples Python existants
73 | 
74 | Les 29 exemples qui suivent sont conservés. **Insérez vos réponses sous le titre de chaque algorithme**, puis ajoutez une partie finale de tests sur données réelles à la suite du notebook.
75 | 

