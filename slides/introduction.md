#Tenon l'accessibilité à bout de bras
---

Présentation d'outils disponibles aux développeurs pour rendre le monde meilleur
<!-- .slide: data-background-image="img/cover.png" data-background-position="top" data-background-size="50%" style="padding-top: 25%;" -->

---

note:
- Sondages 
- DevAccessible
- Formation
- Contrainte

@@@
#Cédric Le Gallo
---

![Bloody Bear](img/grumly.jpeg)
![Bloody Bear](img/cedric.jpg)

<div><span class="fa fa-twitter">&nbsp;@legallocedric</span></div>
<div><span class="fa fa-github">&nbsp;cedric-legallo</span></div>
<div><span class="fa fa-globe">&nbsp;https://cedriclegallo.fr</span></div>

<!-- .slide: class="green" style="text-align:center;"-->

note:
- Consultant / Formateur freelance
- Angular, Polymer, Vue.js, Vanilla.
- Développeur qui aime ses outils, un outil c'est fait pour gagner du temps
- L'intégration continue est un gain de temps

@@@
#Sommaire
---
* Introduction
* Tenon.io
* Chrome Accessibility Dev Tool
* Conclusion

@@@
#Qu'est ce que l'accessibilité
---

<div class="citation">La loi 2005-102 du 11 février 2005 pour «l'égalité des droits et des chances, la participation et la citoyenneté des personnes handicapées», fixe le principe d'une accessibilité généralisée, intégrant tous les handicaps, qu'ils soient d'ordre physique, visuel, auditif ou mental.</div>

note:
- ne laisser personne sur le coté
- imaginer tous les utilisateurs possible
- L'accessibiltié dans le monde réel n'est pas toujours facile à mettre en oeuvre, par contre dans l'univers des sites et applications web, on n'a aucune excuse pour ne pas le faire
- l'article 47 de la loi prévoit l'acces aux serices public sur internet
- On a tous connu des projets où l'accessibilité est devenu une contrainte parfois tardive avec un impact sur le coût projet mais ça ne devrait pas arriver
- Grands pouvoirs => Grandes Responsabilités

@@@
#Un monde meilleur
---

![info1](img/info1.png)<!-- .element: style="width:45%;"-->
![info2](img/info2.png)<!-- .element: style="width:45%;" -->

note:
- Beaucoup de bon sens
- Prémière étape : virez votre souris
- Retrouvez ces infographies et d'autres pours les autres handocap (souds/malentendant, malvoyants, aveugles, Autistes) sur le github de Home Office Digital

@@@
#Un peu d'histoire
---
<div class="timeline">
	<ul>
		<li>
			<div>
				<time>1996</time>
				le W3C crée Web Accesibility Initiative WAI
			</div>
		</li>
		<li>
			<div>
				<time>1998</time>
				Section 508 : loi US pour l'accessibilité
			</div>
		</li>
		<li>
			<div>
				<time>1999</time>
				Sortie de WCAG 1.0
			</div>
		</li><li>
			<div>
				<time>2005</time>
				Loi française sur l'accessibilité aux établissements publics & RGAA
			</div>
		</li><li>
			<div>
				<time>2006</time>
				L'ONU déclare l'accessibilité Droit universel
			</div>
		</li><li>
			<div>
				<time>2008</time>
				WCAG 2.0 prenant en compte les nouveaux usages et medias
			</div>
		</li><li>
			<div>
				<time>2014</time>
				W3C crée WAI-ARIA pour rendre les RIA accessibles
			</div>
		</li><li>
			<div>
				<time>2015</time>
				RGAA V3
			</div>
		</li>
	</ul>
</div>
<!-- .slide: style="text-align:center;"-->

note:
- Section 508 : loi americaine sur l'acces aux informations electronique et technologique pour les personnes handicapées
- WCAG : Spec sur la définition de l'accessibilité
- Loi 2005
- Référentiel général d'accessibilité pour les administrations découle de la loi 2005 : méthodes d'analyse et de test pour atteindre l'accessibilité
- Accessibilité droit universel
- ARIA : méthodes et implementation pour rendre un site accessible

@@@
#Publics ciblés
---

Des utilisateurs : 
<span><span class="fa fa-users"></span></span>
<!-- .element: class="fragment" -->
<span><span class="fa fa-wheelchair"></span></span>
<!-- .element: class="fragment" -->
<span><span class="fa fa-eye-slash"></span></span>
<!-- .element: class="fragment" -->
<span><span class="fa fa-deaf"></span></span>
<!-- .element: class="fragment" -->
<span><span class="fa fa-globe"></span></span>
<!-- .element: class="fragment" -->


Des interfaces de sortie : 
<span><span class="fa fa-desktop"></span></span>
<!-- .element: class="fragment" -->
<span><span class="fa fa-tablet"></span><span class="fa fa-mobile"></span></span>
<!-- .element: class="fragment" -->
<span><span class="fa fa-volume-up"></span></span>
<!-- .element: class="fragment" -->
<span><span class="fa fa-braille"></span></span>
<!-- .element: class="fragment" -->
<span><span class="fa fa-adjust"></span></span>
<!-- .element: class="fragment" -->
<span><span class="fa fa-search"></span></span>
<!-- .element: class="fragment" -->

Des interface d'entrées : 
<span><span class="fa fa-mouse-pointer"></span></span>
<!-- .element: class="fragment" -->
<span><span class="fa fa-hand-o-up"></span></span>
<!-- .element: class="fragment" -->
<span><span class="fa fa-keyboard-o"></span></span>
<!-- .element: class="fragment" -->
<span><span class="fa fa-microphone"></span></span>
<!-- .element: class="fragment" -->

<div><span class="fa fa-hand-peace-o">GG !</span></div>
<!-- .element: class="fragment" style="zoom:3;"-->


note:
- la majorité des utilisateurs 
- handicap physqie ou mentaux
- malvoyants / aveugles
- sourds malentendants : Sous-titre en français pour les vidéos en français
- international
- écran / responsive
- audio : Bande son audio description : aveugle
- braille
- contraste / zoom
- Souris / Gestures / Clavier 
- Voix (CES 2017 la voix est la nouvelle IHM)

@@@
# Des outils à la rescousse
---

- 508 Checker
- Paypal AATT
- Accessibility Developer Tools for Chrome
- Tenon
- Asqatasun
- ...

https://www.w3.org/WAI/ER/tools/

note:
- Ensemble des outils listés : https://www.w3.org/WAI/ER/tools/
- Aujourd'hui on va en présenter 2
- Access Dev Tool de chrome car on développe tous avec Chrome
- Tenon.io car il fournit une API simplissime à intégrer tout en validant pas mal de spec WCAG 2.0