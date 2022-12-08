# Accueil SimpleText@CLEF-2022

---

Accueil | Appel à contributions | Dates importantes | Tâches | Outils| Programme | Publications | Organisateurs | Contact | CLEF-2023
<!--- <img src="https://github.com/simpletext-madics/2021/blob/main/clef/FR.png?raw=true" width="30">https://simpletext-project.com/2022/clef/') --->

---

<img align="left" src="https://github.com/simpletext-madics/2021/blob/main/clef/simpletext-logo-blue.png?raw=true" width="100"/>  

## SimpleText : Simplification automatique des textes scientifiques


### Sujet et objectifs du laboratoire

SimpleText relève les défis techniques et les difficultés d'évaluation en fournissant des données et des critères de référence appropriés pour la simplification des textes.
<br/>Nous proposons les tâches suivantes : * TASK 1 Qu'est-ce que le in (ou le out) ? Sélectionnez les passages à inclure dans un résumé simplifié, à partir d'une requête * TASK 2 Qu'est-ce qui n'est pas clair ? Étant donné un passage et une question, classez les termes/concepts qui doivent être expliqués pour comprendre ce passage (définitions, contexte, applications,...) * TASK 3 Réécrire ceci ! En fonction d'une requête, simplifier des passages de résumés scientifiques * TÂCHE NON SUGGÉRÉE Toute soumission utilisant nos données est la bienvenue !


Pour relever ces défis, SimpleText vise à répondre aux questions de recherche suivantes :
<br/>RQ1 - Quelle expression textuelle porteuse d'information doit être simplifiée (document et passage à inclure dans le résumé simplifié) ?
<br/>RQ2 - Quel type d'information de base devrait être fourni (quels termes devraient être contextualisés en donnant une définition et/ou une application) ? Quelles sont les informations les plus pertinentes ou les plus utiles ?
<br/>RQ3 - Comment améliorer la lisibilité d'un texte court donné (par exemple en réduisant le vocabulaire et la complexité syntaxique) avec un taux acceptable de distorsion de l'information ? 

### Importance pour le domaine et pertinence pour la CLEF

Avoir des connaissances scientifiques est une aptitude importante pour les gens. C'est l'une des clés de l'esprit critique, de la prise de décision objective et du jugement de la validité et de la signification des résultats et des arguments, qui permet de discerner les faits de la fiction. Ainsi, le fait de posséder des connaissances scientifiques de base peut également contribuer à préserver sa santé, tant physiologique que mentale. La pandémie de COVID-19 en est un bon exemple. Comprendre le problème lui-même, connaître et appliquer les règles de distanciation sociale et les politiques sanitaires, choisir d'utiliser ou d'éviter des procédures de traitement ou de prévention particulières peut devenir crucial. Dans le contexte d'une pandémie, l'information qualifiée et opportune doit atteindre tout le monde et être accessible. C'est ce qui motive des projets tels que EasyCovid.

Cependant, les textes scientifiques sont souvent difficiles à comprendre car ils nécessitent de solides connaissances de base et utilisent une terminologie délicate. Bien que des efforts aient été déployés récemment pour simplifier les textes, l'élimination automatique de ces barrières de compréhension entre les textes scientifiques et le grand public reste un défi à relever. SimpleText Lab réunit des chercheurs et des praticiens travaillant sur la génération de résumés simplifiés de textes scientifiques. Il s'agit d'un nouveau laboratoire d'évaluation qui fait suite à l'atelier SimpleText-2021. Toutes les perspectives sur la vulgarisation scientifique automatique sont les bienvenues, y compris, mais sans s'y limiter : Traitement du langage naturel (NLP), Recherche d'information (IR), Linguistique, Journalisme scientifique, etc.

### Scénarios

L'objectif est de créer un résumé simplifié de plusieurs documents scientifiques sur la base d'une requête donnée, afin de fournir à l'utilisateur un résumé simplifié instantané sur un sujet spécifique qui l'intéresse ou de générer un résumé quotidien, par exemple pour ArXiv.

### Configuration, mesures et tâches de l'évaluation 

Ensemble de données : Nous utilisons le Citation Network Dataset : DBLP+Citation, réseau de citations ACM. Un index de recherche élastique est mis à la disposition des participants, accessible via une interface graphique API. Cet indice est adéquat pour :
<br/>\- Appliquer des méthodes de base de recherche de passages basées sur des modèles de RI vectoriels ou linguistiques
<br/>\- Générer des modèles d'allocation de Dirichlet latente,
<br/>\- Former des réseaux neuronaux graphiques pour la recommandation de citations, comme le fait Stellar Graph par exemple,
<br/>\- Appliquer des transformateurs bidirectionnels profonds pour l'expansion des requêtes...

Les données sont de deux ordres : Médecine et Informatique, deux domaines parmi les plus populaires dans les forums comme ELI5.


Requêtes en anglais : Pour cette édition, les requêtes sont une sélection de titres de presse récents du Guardian enrichis de mots-clés extraits manuellement du contenu des articles. Il a été vérifié que chaque mot-clé permet d'extraire au moins 5 résumés pertinents. L'utilisation de ces mots-clés est facultative.
<br/>Format d'entrée pour toutes les tâches :
<br/>\- Les sujets sont au format MD
<br/>\- Articles en texte intégral du Guardian (lien, dossier avec textes intégraux au format MD)
<br/>\- Index ElasticSearch sur le serveur de données
<br/>\- vidage complet du DBLP au format JSON.GZ
<br/>\- Extraction des résumés DBLP pour chaque sujet dans le format MD suivant (doc\_id, année, résumé)

## Comment citer
Si vous étendez ou utilisez ce travail, veuillez citer l'article où il a été présenté : ``` Liana Ermakova, Eric SanJuan, Jaap Kamps, Stéphane Huet, Irina Ovchinnikova, Diana Nurbakova, Sílvia Araújo, Radia Hannachi, Elise Mathurin et Patrice Bellot. 2022\. Aperçu du laboratoire SimpleText de CLEF 2022 : Simplification automatique de textes scientifiques. In Experimental IR Meets Multilinguality, Multimodality, and Interaction : 13e conférence internationale de l'association CLEF, CLEF 2022, Bologne, Italie, 5-8 septembre 2022, Actes. Springer-Verlag, Berlin, Heidelberg, 470-494\. https://doi.org/10.1007/978-3-031-13643-6\_28 Paper

[Télécharger le fichier .BIB](../../BibTeX/ermakova_overview_2022.bib)

---

                 [<img src="https://github.com/simpletext-madics/2022/blob/main/clef/en/clef_logo_2022.png?raw=true" width="150">](http://www.clef-initiative.eu/)                          <img src="https://github.com/simpletext-madics/2021/blob/main/clef/logo-clef-initiative.png?raw=true" width="200">
