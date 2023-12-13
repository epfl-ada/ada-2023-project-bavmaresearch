# Idée Milestone 3

Avant de select 5 jours : on propose une analyse, mauvais graphes **Macro**
- Best producters: most successfull movies
- Distributions des scores (awarded/non awarded)
- Analysis H/F
- Age des acteurs dans le film (release du film - date naissance acteur)



5 producteurs viennent avec 5 idées de genre différents : 

Utiliser les données pour trouver les catégories

- Action /aventure 
- Horreur / thriller
- SF
- Family movies / comedies
- Musical

Analyses par genre : 




**Outils**: 
- ML : 
    - ML pour les langues + countries versus score + nombre oscar + runtime +  
    - DBSCAN: si on trouve un pattern cool -> cool
    - KNN/ clustering pour sortir les features : unsupervised

- NLP: sortir les champs lexicaux associés pour chaque catégorie
- Acteurs + directeurs : graphes avec les acteurs les plus connus qui ont fait pleins de movies dans la catégories + ajouter les photos des plus connus (scrapping google image)
- Trouver le best cast : 
- Causal analysis of observational data : sensitivity analysis : nominated, oscar, rating --> profitability ?? 
- mauvaises regressions linéaires



**Répartition**

| Noms | Taks 1 | Task 2 |
|--------|--------|--------|
|Aline|First analysis: refaire tout les graphes en plotly pour pouvoir export .html|Sortir les graphes en .html (demande à GPT) |
|Mathieu|Trouver le best casting par genre | |
|Val|ML : countries + runtime |Graphes de kiffeurs |
|Antoine| Utiliser Tf-Idf|Drafter l'interface|
|Ben|Aller chercher les bières  (Lupulus only)| Causal analysis|


## To do list

- Pour tout le monde : 
    - Documenter vos codes
    - Expliquer ce qu'on a fait : read me 


- Benoit : 
    - story telling (avec Aline)
        - pour chaque genre    
    - Read Me : 
        - reprendre Milestone 2 + ajouter les amélirations
        - Organisation dans la team
        
    - causality : donner une analyse pour chaque genre

- Val : 
    1) Machine learning pour les langues + les pays en focntion des genres 
        - Mettre sur le site les graphes 
        - Ajouter un paragraphe pour expliquer le so what
        - Mettre une map pour chaque genre : en fonction de si ils aiment ou pas tel theme

    2) ML sur les roles : boosted tree
        - importance de chaque rôle 
        - meuf / mec / experience de l'acteur
        - Trouve des acteurs vivants correspondant au rôle
        - Objectif maxer le score du film

- Aline : story telling 
    - + de meme + de story 
    - Remettre en page la première page
    - Répartition du runtime + profit pour chaque genre

- Antoine : 
    - Causality analysis (avec Beun) : analyse des résultats
    - Graphes films + actors : trouver les acteurs au centre du graphe --> voir slides semaine 12  : utiliser les outils et le faire pour chaque genre 

- Mathieu :  
    - Adapter le cast avec les acteurs du modèle de Val
    - Adapter pour le directeur optimal
    



**Dans les pages genres :**

- NLP
- Causality
- Geographie + langue + 
- Chaque genre : les meilleurs acteurs + producteurs
- Runtime + profit pour chaque genre


