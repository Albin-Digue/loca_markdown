# Tâches de SimpleText@CLEF-2022

Accueil | Appel à contributions | Dates importantes | Tâches | Outils Programme | Publications | Organisateurs | Contact | CLEF-2023


---

## Directives pour les tâches SimpleText

Nous vous invitons à soumettre aussi bien des parcours automatiques que manuels ! Les interventions manuelles doivent être signalées.

---

Accès | Tâche partagée 1 | Tâche partagée 2 | Tâche partagée 3| Tâche non partagée 4

<br>

## Tâche 2 : Qu'est-ce qui n'est pas clair ? Étant donné un passage et une requête, classez les termes/concepts qui doivent être expliqués pour comprendre ce passage (définitions, contexte, applications,...).

Le but de cette tâche est de décider quels termes (jusqu'à 5) nécessitent une explication et une contextualisation pour aider un lecteur à comprendre un texte scientifique complexe - par exemple, en ce qui concerne une requête, les termes qui doivent être contextualisés (avec une définition, un exemple et/ou un cas d'utilisation). Pour chaque passage, les participants doivent fournir une liste classée des termes difficiles avec les notes correspondantes sur l'échelle 1-3 (3 pour les termes les plus difficiles, tandis que le sens des termes notés 1 peut être déduit ou deviné) et sur l'échelle 1-5 (5 pour les termes les plus difficiles). Les passages (phrases) sont considérés comme indépendants, c'est-à-dire que la répétition de termes difficiles est autorisée. Le regroupement des termes et des métriques automatiques (précision de la classification binaire des termes, NDCG pour le classement des termes, statistiques de kappa...) seront utilisés pour évaluer ces résultats.

**Format d'entrée :** Les données de formation et de test sont fournies dans les formats JSON et CSV avec les champs suivants : * snt\_id : un identifiant unique de passage (phrase) * source\_snt : texte du passage * doc\_id : un identifiant unique du document source * query\_id : un identifiant de requête * query\_text : termes difficiles à extraire des phrases par rapport à cette requête

*Exemple de saisie :*

``` {"snt_id" : "G06.2_2548923997_3", "source_snt" : "Ces systèmes de communication rendent les véhicules à conduite autonome vulnérables à de nombreux types d'attaques malveillantes, telles que les attaques Sybil, les dénis de service (DoS), les trous noirs, les trous gris et les trous de ver.", "doc_id":2548923997, "query_id" : "G06.2", "query_text" : "self driving"} ```

**Format de sortie :** 

Liste des termes à contextualiser dans un format JSON ou un fichier tabulé TSV (pour les runs manuels) avec les champs suivants : * run\_id : ID d'exécution commençant par team\_id\_task\_id_ * manuel : Si l'exécution est manuelle {0,1} * snt\_id : un identifiant unique de passage (phrase) du fichier d'entrée * term : Terme ou autre expression à expliquer * term\_rank\_snt : rang de difficulté du terme dans la phrase donnée * score\_5 : score de difficulté du terme sur une échelle de 1 à 5 (5 étant le terme le plus difficile) * score\_3 : score de difficulté du terme sur une échelle de 1 à 3 (3 étant le terme le plus difficile)

Exemple de sortie :

\`\`\`{json} {"run\_id" : "NP\_task\_2\_run1", "manual":1, "snt\_id" : "G06.2\_2548923997\_3", "term" : "black hole attack", "term\_rank\_snt":1, "score\_5":5, "score\_3":3},

{"run\_id" : "NP\_task\_2\_run1", "manual":1, "snt\_id" : "G06.2\_2548923997\_3", "term" : "grey hole attack", "term\_rank\_snt":2, "score\_5":5, "score\_3":3},

{"run\_id" : "NP\_task\_2\_run1", "manual":1, "snt\_id" : "G06.2\_2548923997\_3", "term" : "Sybil attack", "term\_rank\_snt":3, "score\_5":5, "score\_3":3},

{"run\_id" : "NP\_task\_2\_run1", "manual":1, "snt\_id" : "G06.2\_2548923997\_3", "term" : "wormhole attack", "term\_rank\_snt":4, "score\_5":5, "score\_3":3},

{"run\_id" : "NP\_task\_2\_run1", "manual":1, "snt\_id" : "G06.2\_2548923997\_3", "term" : "Denial of service attack", "term\_rank\_snt":5, "score\_5":4, "score\_3":3} \`\`\`

*Vérificateur du format de sortie*

Vous pouvez utiliser ce script python3 pour vérifier le format de sortie. Le script nécessite Python 3 et la bibliothèque Pandas : [Télécharger python output checker](../check_format.py)

**Avis de non-responsabilité :** En téléchargeant et en utilisant ces données, vous acceptez les conditions d'utilisation. Toute utilisation des données à des fins autres que la recherche universitaire constituerait une violation de l'utilisation prévue de ces données. 

Par conséquent, en téléchargeant et en utilisant ces données, vous donnez les assurances suivantes concernant les données SimpleText : 1\. Vous n'utiliserez ni ne permettrez à d'autres d'utiliser les données des ensembles de données SimpleText de quelque manière que ce soit, sauf pour les cours et la recherche universitaire. 2\. À aucun moment vous ne divulguerez, ne donnerez ou ne transmettrez (de quelque manière, sous quelque forme ou à quelque fin que ce soit) les données (ou toute partie de celles-ci) à quelque endroit ou personne que ce soit, y compris, mais sans s'y limiter, en rendant les données disponibles sur Internet et en copiant les données sur tout système de stockage en nuage. 3\. Vous ne divulguerez pas et ne permettrez pas à d'autres de divulguer l'ensemble de données ou toute partie de celui-ci à quiconque. 

En cas de violation des conditions d'accès aux données à des fins scientifiques, cet accès peut être retiré à l'entité de recherche et/ou au chercheur. L'entité de recherche peut également être tenue de payer des dommages et intérêts à des tiers ou être invitée à prendre des mesures disciplinaires à l'encontre du chercheur fautif. 


### Évaluation
Le regroupement des termes et des métriques automatiques (précision de la classification binaire des termes, NDCG pour le classement des termes, statistiques de kappa...) seront utilisés pour évaluer ces résultats.

### Soumission des résultats :
Les participants doivent placer leurs résultats d'exécution dans le dossier Documents créé pour leur utilisateur et les soumettre par e-mail à contact@simpletext-project.com.

L'objet de l'e-mail doit être au format \[CLEF TASK 2] TEAM\_ID. 

Les séries doivent être soumises sous la forme d'un dossier ZIP contenant les fichiers JSON correspondants. Les passages manuels peuvent être soumis en format CSV. 

Un courriel de confirmation sera envoyé dans les deux jours suivant la date limite de soumission. 

## Comment citer
Si vous étendez ou utilisez ce travail, veuillez citer l'article où il a été présenté : ``` Liana Ermakova, Eric SanJuan, Jaap Kamps, Stéphane Huet, Irina Ovchinnikova, Diana Nurbakova, Sílvia Araújo, Radia Hannachi, Elise Mathurin et Patrice Bellot. 2022\. Aperçu du laboratoire SimpleText de CLEF 2022 : Simplification automatique de textes scientifiques. Dans Experimental IR Meets Multilinguality, Multimodality, and Interaction : 13e conférence internationale de l'association CLEF, CLEF 2022, Bologne, Italie, 5-8 septembre 2022, Actes. Springer-Verlag, Berlin, Heidelberg, 470-494\. https://doi.org/10.1007/978-3-031-13643-6\_28 Paper

[Télécharger le fichier .BIB](../../BibTeX/ermakova_overview_2022.bib)
