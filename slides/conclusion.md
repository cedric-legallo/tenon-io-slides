#Conclusion
---

Il n'a jamais été aussi simple de contrôler l'accessibilité de son site, que ce soit : 
- en localhost 
- dynamiquement
- dans une chaîne CI

note:
- localhost envoi des sources ou plugin chrome
- avec Selenium, avec le tenon monitor script
- avec a11y pour jouer le plugin chrome en CLI ou avec Tenon


@@@
#Les autres
---

Tanaguru : site le plus proche de Tenon, avec un crawler mais sans API

Asqatasun (RGAA, WCAG, Open Source)

Functional Accessibility Evaluator 2.0 

note:
- Tanaguru le plus proche de Tenont, pricing similaire, tout repose sur le crawler, pas fait pour les SPA. L'audit est cependant de bonne facture et l'interface moderne RGAA
- Asqatasun est un fork de Tanaguru par ses créateurs d'origine. pas un SaaS ,s'installe sur un server ou bien dans votre chaine d'IC. container docker officiel plug and play. plus difficile à intégrer dans sa chaine mais self hosted. auteurs toujours actifs sur github, check SEO, vraiment aucun de défaut si ce n'est l'absence de navigateur headless
- FAE : interface vieillissante, audit de bonne facture, fait par des universitaires donc extremement exhaustif, impossible d'évaluer des fragments, donc online only
- les autres : soit ils étaient inutilisables, soit ils étaient trop complexe à utiliser, soit le service rendu n'était pas à la hauteur.

@@@
#Ressources
---

- https://tenon.io
- https://github.com/GoogleChrome/accessibility-developer-tools
- https://references.modernisation.gouv.fr/rgaa-accessibilite/
- https://www.w3.org pour WAI, WCAG et ARIA

@@@

<!-- .slide: data-background-image="img/merci.jpeg"   data-background-size="1600px" -->

note: 
- A vous pour m'avoir écouter
- Gregory et Nicolas pour m'avoir offert cette tribune
- Krl de Tenon pour m'avoir donné le moyen de faire cette démo
- Addy Osmani pour m'avoir fait découvrir le service l'an dernier
- Cette image est un magnifique exemple de ce qu'il ne faut pas faire (couleur, texte sur image, ...)

@@@

<!-- .slide: data-background-image="img/question.jpg"  data-background-size="900px" -->
