#Tenon.io
---

@@@
#Introduction
---

<div class="citation">Simplifier votre accessibilité</div>

Une API de test pour mesurer l'accessibilité des pages

Une vue dashboard sexy pour analyser les résultats

note:
Comme je l'ai dit j'aime bien quand un outil me fait gagner du temps, et c'est le cas de Tenon. Il ne coute presque rien à mettre en oeuvre (???H pour faire ma chaine d'IC pour Rennes.JS)

@@@
#Pourquoi Tenon.io
---

![headless](img/headless.jpg)
<!-- .element: style="zoom:2;margin:auto;" -->
<!-- .slide: class="center;" -->

note:
- La grande force de Tenon.io c'est qu'il est lance le site dans un navigateur headless qui permet au JavaScript de s'executer là où les autres font un travail sur la ressource statique qui est un problème pour nos SPA.

@@@
#Ce que couvre Tenon.io
---

Tenon testera à terme tout ce qui est automatisable dans les spécifications Section508 et WCAG 2.0

140 scenarios de test validant 1200 assertions

La liste exhaustive point par point des spec couvertes est disponible sur le site en toute transparence : https://tenon.io/documentation/what-tenon-tests.php

@@@
#Ce que ne couvre pas Tenon.io
---

Toutes les recommandations d'accessibilités qui sont soumises à interprétation et donc non testéble automatiquement

Toutes les recommandations d'accessibilité non testable automatiquement 

Certaines recommandation dure à tester, mais que Tenon couvrira dans une version future

note:
- Les ordinateurs sont des machines, ils n'ont pas de libre arbitre.
- Difficile aussi de juger tous les contraste sont-ils suffisants ou non
- C'est facile de dire : Votre vidéo n'a pas de sous-titre externe plus dur de dire s'ils sont enregistré directement dans le flux
- C'est facile de dire que les images n'ont pas de titre mais plu sdifficile de voir qu'elles contiennent du texte et donc du contenu inaccessible à un aveugle, mais avec un bon OCR ça deviendra possible


@@@
#l'API
---

* Prendre un jeton d'acces à Tenon
* Récupérer la clé dédiée à votre compte
* Requêter le service
* Analyser les résultats

note:
- Your client application submits a request against the API
- Tenon receives the request and validates it
- If the request passes validation, Tenon runs its tests against the URL or document source
- Tenon returns a JSON response.
- Possible de tester soit un code source (chaine de caractère soit une page web accessible par url)

@@@
#la requête
---

* POST uniquement
* 2 paramètres obligatoires :
  * key pour le pricing
  * src ou url à analyser
* 11 autres paramètres : 
  * fragment
  * certainty, priority
  * level, store 
  * projectID, docId
  * waitFor, uaString
  * viewPortHeight, viewPortWidth

note:
- Recommandation d'utiliser des urls plutot que src
- fragment en combinaison avec src, simule le test d'un fragment versus page complète 0 ou 1 (0) 
- /!\  do not set fragment to '1' if you're sending over a complete document. You will get weird results.
- certainty : Filtre sur le degré de certitute d'infraction de l'outil (exclusion de faux positif potentiel) Valid values: '0','20','40','60','80','100'
- priority : ordre arbitraire donnée par Tenon, (default 0 tout est affiché)
- level : niveau d'accessibilité A, AA, AAA (defaut)
- store : sauvegarder les résultats 0 ou 1 (0)
- projectID : chaine pour tests multi-projets
- docID : id de la page testée (généré par défaut)  
- waitFor : délai en ms gare au timeout de tenon !
- uaString : user-agent arbitraire (google chrome par défaut)
- viewPortHeight / viewPortWidth :  entre 0 et 9999 (768 /1024 par défaut)

@@@
#la réponse
---

![response](img/response.png)
<!-- .slide: style="text-align: center;zoom: 0.85;" -->

@@@
#Tester un site public
---

* Lister les URL (sitemap.xml)
* Requêter le Web Service avec chaque URL
* Sauvegarder les résultats (JSON)

note:
- Opérations à faire dans un script, j'ai personnellement fait une version node.js parce que JS, mais n'importe quel langage de script (et même pas de script) peut faire le taf
- tenon fournit des connecteurs dans la plupart des langages

@@@
#Tester localhost ou intranet
---

* Récupérer le script précédent
* Transformer la partie requête à Tenon pour utiliser src plutot que url
* Scripter la récupération des template HTML
* Sauvegarder les résultats

note:
- j'ai également fait une version node.js
- tenon est une API à ce titre il peut tout à fait  faire partie de votre chaine de tests e2e en y ajoutant lesappels adéquats.

@@@
#Tenon Site Monitor
---

Dernière née des features du site

Permet de scanner intégralement votre application aussi simplement qu'en ajoutant Google Analytics

/!\ peux rapidement vider votre quota mensuel d'utilisation de Tenon

note:

@@@
#Pricing
---

<iframe src="https://tenon.io/pricing.php"></iframe>

note:
Le seul inconvénient de Tenon c'est qu'il n'est pas gratuit. Mesurer son apport par rapport à son coût n'est pas une mince affaire. Le nombre d'utilisateur n'est pas vraiment limitant puisque vous utiliserez un utilisateur CI dédié. Le nb de calls mensul par contre dépend des besoins de votre compagnie.

@@@
#Un cas concrêt
---

<iframe src="http://lafrenchtech-rennes.fr/"></iframe>
<!-- .element: class="fragment" -->

note:
[https://cedriclegallo.fr/](https://cedriclegallo.fr/)
