# Tâches de SimpleText@CLEF-2022


Accueil | Appel à contributions | Dates importantes | Tâches | Outils Programme | Publications | Organisateurs | Contact | CLEF-2023


---

## Directives pour les tâches SimpleText

Nous vous invitons à soumettre aussi bien des parcours automatiques que manuels ! Les interventions manuelles doivent être signalées.

---

Accès | Tâche partagée 1 | Tâche partagée 2 | Tâche partagée 3| Tâche non partagée 4

<br>

## Tâche 1 : Qu'est-ce qui est dedans (ou dehors) ? Sélectionner les passages à inclure dans un résumé simplifié, à partir d'une requête.

La tâche vise à trouver des références en informatique qui pourraient être insérées comme citations dans des articles de presse originaux d'audience générale à des fins d'illustration, de vérification des faits ou d'actualisation. Pour chacune des références sélectionnées, des phrases plus pertinentes doivent être extraites. Ces passages peuvent être complexes et nécessitent une simplification supplémentaire à effectuer dans les tâches 2 et 3. La tâche 1 se concentre sur la récupération du contenu.

**Corpus : DBLP + résumés**

Nous utilisons le Citation Network Dataset : DBLP+Citation, réseau de citations ACM. Un index ElasticSearch est mis à la disposition des participants, accessible via une API GUI. Un dump json de l'index est également disponible pour les participants.

**Sujets : Articles de presse**

Les sujets sont une sélection de 40 articles de presse. 20 provenant d'un grand journal international grand public et 20 de Tech Xplore, enrichis de requêtes extraites manuellement du contenu de l'article. Il a été vérifié qu'au moins 5 résumés pertinents peuvent être trouvés pour chaque requête.

**Format de sortie :**
 
Les résultats doivent être fournis dans un format tabulé de type TREC (avec une extension ".csv"). Les colonnes suivantes sont obligatoires (elles doivent figurer sur la première ligne) :

1. run\_id : ID de l'exécution commençant par teamid, suivi par "task1" et run\_name
2. manuel : Si l'exécution est manuelle {0,1}
3. topic\_id : ID du sujet
4. query\_id : ID de la requête utilisée pour récupérer le document (si l'une des requêtes fournies pour le sujet a été utilisée ; 0 sinon)
5. doc\_id : ID du document récupéré (à extraire de la sortie json)
6. passage : Texte du passage sélectionné
 
Pour chaque sujet, le nombre maximum de références DBLP distinctes (champ \_id json) est de 100 et la longueur totale des passages ne doit pas dépasser 1000 tokens.

Exemple de sortie :

| run\_id | manual | topic\_id | query\_id | doc\_id | passage | |:-------|:-------|:---------|:-------|:--------|:-----| | ST1\_task1\_1 | 0 | G01 | G01.1 | 1564531496 | Un CDA est un appareil mobile pour l'utilisateur, similaire à un assistant numérique personnel (PDA). Il aide le citoyen dans ses relations avec les autorités publiques et prouve ses droits - si on le souhaite, même sans révéler son identité. | ST1\_task1\_1 | 0 | G01 | G01.1 | 3000234933 | Les gens sont de plus en plus à l'aise avec les assistants numériques (AN) pour interagir avec des services ou des objets connectés | | ST1\_task1\_1 | 0 | G01 | G01.2 | 1448624402 | Comme l'ont montré de nombreuses recherches expérimentales, les individus souffrent de divers biais dans la prise de décision. |

*Vérificateur du format de sortie*

Vous pouvez utiliser ce script python3 pour vérifier le format de sortie. Le script nécessite Python 3 et la bibliothèque Pandas : [Télécharger python output checker](../check_format.py)

**Avis de non-responsabilité :** En téléchargeant et en utilisant ces données, vous acceptez les conditions d'utilisation. Toute utilisation des données à des fins autres que la recherche universitaire constituerait une violation de l'utilisation prévue de ces données. 

Par conséquent, en téléchargeant et en utilisant ces données, vous donnez les assurances suivantes concernant les données SimpleText : 1\. Vous n'utiliserez ni ne permettrez à d'autres d'utiliser les données des ensembles de données SimpleText de quelque manière que ce soit, sauf pour les cours et la recherche universitaire. 2\. À aucun moment vous ne divulguerez, ne donnerez ou ne transmettrez (de quelque manière, sous quelque forme ou à quelque fin que ce soit) les données (ou toute partie de celles-ci) à quelque endroit ou personne que ce soit, y compris, mais sans s'y limiter, en rendant les données disponibles sur Internet et en copiant les données sur tout système de stockage en nuage. 3\. Vous ne divulguerez pas et ne permettrez pas à d'autres de divulguer l'ensemble de données ou toute partie de celui-ci à quiconque. 

En cas de violation des conditions d'accès aux données à des fins scientifiques, cet accès peut être retiré à l'entité de recherche et/ou au chercheur. L'entité de recherche peut également être tenue de payer des dommages et intérêts à des tiers ou être invitée à prendre des mesures disciplinaires à l'encontre du chercheur fautif. 


### Évaluation  
Le regroupement de phrases et les métriques automatiques seront utilisés pour évaluer ces résultats. La pertinence du document source sera évaluée ainsi que les éventuels problèmes d'anaphore non résolus.

### Soumission des résultats :
Les participants doivent placer leurs résultats d'exécution dans le dossier Documents créé pour leur utilisateur et les soumettre par e-mail à contact@simpletext-project.com.

Le sujet de l'email doit être dans le format \[CLEF TASK 1] TEAM\_ID. 

Les parcours doivent être soumis sous forme de fichier au format TSV. 

Un courriel de confirmation sera envoyé dans les deux jours suivant la date limite de soumission. 

## Comment citer
Si vous étendez ou utilisez ce travail, veuillez citer l'article où il a été présenté : ``` Liana Ermakova, Eric SanJuan, Jaap Kamps, Stéphane Huet, Irina Ovchinnikova, Diana Nurbakova, Sílvia Araújo, Radia Hannachi, Elise Mathurin et Patrice Bellot. 2022\. Aperçu du laboratoire SimpleText de CLEF 2022 : Simplification automatique de textes scientifiques. In Experimental IR Meets Multilinguality, Multimodality, and Interaction : 13e conférence internationale de l'association CLEF, CLEF 2022, Bologne, Italie, 5-8 septembre 2022, Actes. Springer-Verlag, Berlin, Heidelberg, 470-494\. https://doi.org/10.1007/978-3-031-13643-6\_28 Paper

[Télécharger le fichier .BIB](../../BibTeX/ermakova_overview_2022.bib)
