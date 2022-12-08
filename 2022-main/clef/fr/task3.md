# Tâches de SimpleText@CLEF-2022

Accueil | Appel à contributions | Dates importantes | Tâches | Outils Programme | Publications | Organisateurs | Contact | CLEF-2023


---

## Directives pour les tâches SimpleText

Nous vous invitons à soumettre aussi bien des parcours automatiques que manuels ! Les interventions manuelles doivent être signalées.

---

Accès | Tâche partagée 1 | Tâche partagée 2 | Tâche partagée 3| Tâche non partagée 4

<br>

## Tâche 3 : Réécris ça ! En fonction d'une requête, simplifier des passages de résumés scientifiques. 

Le but de cette tâche est de fournir une version simplifiée de passages de texte (phrases) par rapport à une requête. Les participants recevront des requêtes et des résumés d'articles scientifiques. Les résumés peuvent être divisés en phrases. Les passages simplifiés seront évalués manuellement avec l'utilisation éventuelle de métriques d'agrégation.

**Format d'entrée :** Les données de formation et de test sont fournies dans les formats JSON et CSV avec les champs suivants : * snt\_id : un identifiant unique de passage (phrase) * source\_snt : texte du passage * doc\_id : un identifiant unique de document source * query\_id : un identifiant de requête * query\_text : simplification à faire par rapport à cette requête

*Exemple de saisie :*

*{"snt\_id" : "G11.1\_2892036907\_2", "source\_snt" : "Avec le nombre croissant de véhicules aériens sans pilote participant à des activités dans le domaine civil et commercial, il existe un besoin accru d'autonomie dans ces systèmes également.", "doc\_id":2892036907, "query\_id" : "G11.1", "query\_text" : "drones"}*

**Format de sortie :** Liste des termes à contextualiser dans un format JSON ou un fichier tabulé TSV (pour les runs manuels) avec les champs suivants : * run\_id : ID d'exécution commençant par team\_id\_task\_3_ * manuel : Si l'exécution est manuelle {0,1} * snt\_id : un identifiant unique de passage (phrase) du fichier d'entrée * simplified\_snt : Texte du passage simplifié 

Exemple de sortie : {"run\_id" : "BTU\_task\_3\_run1", "manual":1, "snt\_id" : "G11.1\_2892036907\_2", "simplified\_snt" : "Les drones sont de plus en plus utilisés dans le domaine civil et commercial et doivent être autonomes."}

*Vérificateur du format de sortie*

Vous pouvez utiliser ce script python3 pour vérifier le format de sortie. Le script nécessite Python 3 et la bibliothèque Pandas : [Télécharger python output checker](../check_format.py)

**Avis de non-responsabilité :** En téléchargeant et en utilisant ces données, vous acceptez les conditions d'utilisation. Toute utilisation des données à des fins autres que la recherche universitaire constituerait une violation de l'utilisation prévue de ces données. 

Par conséquent, en téléchargeant et en utilisant ces données, vous donnez les assurances suivantes concernant les données SimpleText : 1\. Vous n'utiliserez ni ne permettrez à d'autres d'utiliser les données des ensembles de données SimpleText de quelque manière que ce soit, sauf pour les cours et la recherche universitaire. 2\. À aucun moment vous ne divulguerez, ne donnerez ou ne transmettrez (de quelque manière, sous quelque forme ou à quelque fin que ce soit) les données (ou toute partie de celles-ci) à quelque endroit ou personne que ce soit, y compris, mais sans s'y limiter, en rendant les données disponibles sur Internet et en copiant les données sur tout système de stockage en nuage. 3\. Vous ne divulguerez pas et ne permettrez pas à d'autres de divulguer l'ensemble de données ou toute partie de celui-ci à quiconque. 

En cas de violation des conditions d'accès aux données à des fins scientifiques, cet accès peut être retiré à l'entité de recherche et/ou au chercheur. L'entité de recherche peut également être tenue de payer des dommages et intérêts à des tiers ou être invitée à prendre des mesures disciplinaires à l'encontre du chercheur fautif. 

### Évaluation
Les passages simplifiés seront évalués manuellement avec l'utilisation éventuelle de métriques d'agrégation.

### Soumission des résultats :
Les participants doivent placer leurs résultats d'exécution dans le dossier Documents créé pour leur utilisateur et les soumettre par e-mail à contact@simpletext-project.com.

L'objet de l'e-mail doit être dans le format \[CLEF TASK 3] TEAM\_ID. 

Les séries doivent être soumises sous la forme d'un dossier ZIP contenant les fichiers JSON correspondants. Les passages manuels peuvent être soumis en format CSV. 

Un courriel de confirmation sera envoyé dans les deux jours suivant la date limite de soumission. 

## Comment citer
Si vous étendez ou utilisez ce travail, veuillez citer l'article où il a été présenté : ``` Liana Ermakova, Eric SanJuan, Jaap Kamps, Stéphane Huet, Irina Ovchinnikova, Diana Nurbakova, Sílvia Araújo, Radia Hannachi, Elise Mathurin et Patrice Bellot. 2022\. Aperçu du laboratoire SimpleText de CLEF 2022 : Simplification automatique de textes scientifiques. Dans Experimental IR Meets Multilinguality, Multimodality, and Interaction : 13e conférence internationale de l'association CLEF, CLEF 2022, Bologne, Italie, 5-8 septembre 2022, Actes. Springer-Verlag, Berlin, Heidelberg, 470-494\. https://doi.org/10.1007/978-3-031-13643-6\_28 Paper

[Télécharger le fichier .BIB](../../BibTeX/ermakova_overview_2022.bib)
