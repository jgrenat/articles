

Paris Web est l'un des grands rassemblements annuels et se définit comme étant "le rassemblement francophone de ceux qui font le web". Ayant eu la chance d'y assister cette année grâce à Viseo, je fais part ici de mon expérience durant ces deux journées.

## Impressions générales

Difficile de décrire l'ambiance Paris Web à quelqu'un qui n'y a pas été. J'en ai d'ailleurs fait l'expérience le vendredi soir, en essayant de décrire ce que j'avais *vécu* (n'ayons pas peur des mots) ces deux jours au Beffroi de Montrouge ! Je vais pourtant essayer une nouvelle fois de le faire, sans virer à la mièvrerie débordante.

Se rendre à Paris Web, c'est un peu comme abandonner son quotidien pour plonger pendant deux jours dans un bain bouillonnant de connaissances, de savoir, d'énergie, d'empathie, d'optimisme et de bonne humeur. (Oui, pour la mièvrerie, c'est raté...) 

Chacun vient ici sans a priori (non nous ne sommes pas au pays des bisounours, il y a bien évidemment des exceptions) pour partager autour d'une même passion : le web. Les angles d'approches et les sujets sont bien plus diversifiés que dans les autres conférences auxquelles j'ai pu assister et tournent autour de thème comme la technologie, le design numérique, les standards ouverts, l'accessibilité web et les valeurs morales. Et ce sont bien ces deux dernières thématiques qui caractérisent le plus cette expérience Paris Web !

L'accessibilité web est en effet le cheval (ou plutôt la licorne) de bataille de ce rassemblement ; l'intégralité des conférences étaient traduites en Langue des Signes Française -- ou LSF (sponsorisé par Ekino) et la moitié était même transcrite par vélotypie (sponsorisée par Globalis). Le fait de mettre en avant ces valeurs -- et de les respecter ! -- est certainement pour beaucoup dans cette avalanche de bon sentiments guimauvesques !

On en ressort plein d'une énergie nouvelle, avec l'envie de mettre en pratique tout ce qu'on a pu découvrir et une volonté nouvelle de *bien faire*. Car bien au-delà des découvertes techniques, Paris Web nous offre l'occasion d'explorer des aspects connexes très complémentaires à notre métier. Et ce, qu'on soit développeur web, graphiste, ou tout autre profession du web.

Un regret cependant, celui de n'avoir pu assister à toutes les conférences. Celles-ci sont en effet réparties entre deux salles, ce qui nous laisse parfois devant des choix cornéliens. Heureusement, les vidéos sont accessibles par la suite sur le [compte vimeo de Paris Web](https://vimeo.com/parisweb). Pour plus de détails, je ne peux que vous orienter sur le [programme complet des conférences](https://www.paris-web.fr/2015/conferences/). Loin de pouvoir être exhaustif sur cet article, je vais aborder essentiellement les conférences qui se sont démarquées à mes yeux et je reviendrai dans de prochains articles sur celles que je souhaite développer.

## [Le dev front à Mach 1 au quotidien](http://tdd.github.io/parisweb-2015-talk/#/)

On le voit partout, et Paris Web ne fait pas exception, [Christophe Porteneuve](http://tddsworld.com/fr/) nous a présenté une conférence sur les outils web aujourd'hui à notre disposition pour développer toujours plus rapidement sur une stack front. On voit ces derniers temps émerger -- en référence directe à l'UX ou *User Experience* -- une tendance vers la DX -- *Developer Experience*. 

Et plus qu'une tendance, c'est une réalité. On constate en effet une explosion des outils pour développeurs directement dans nos navigateurs. Mozilla Firefox, Chrome, Internet Explorer et maintenant Edge, tous les principaux navigateurs ont compris l'enjeu de proposer des outils pour les développeurs. Et pourtant -- comme le fait remarquer Christophe Porteneuve -- on voit encore trop de développeurs tributaires de leur chaîne de build, attendre d'interminables secondes afin de tester le moindre changement dans leur code.

Les navigateurs proposent dans leurs outils des solutions pour directement éditer son code sans repasser par son éditeur favori. Nombreux sont ceux qui le savent pour l'édition du code CSS et HTML, mais beaucoup ignorent encore qu'on peut également le faire directement sur notre code JavaScript à la volée, tout en laissant des *breakpoints* si le besoin s'en fait sentir. C'est également possible sur mobile puisque les navigateurs proposent ces outils pour leurs équivalent mobiles connectés à l'ordinateur. On peut également dans Chrome (et sûrement dans les autres navigateurs via des extensions) lier directement notre *workspace* pour que ces changements soient répercutés directement dans nos fichiers !

Cette présentation des outils navigateurs s'achève sur un cri du coeur du conférencier qui nous enjoint à consulter les portails développeurs de Chrome, Mozilla ou Edge qui détaillent toutes les fonctionnalités et raccourcis claviers qu'ils offrent pour nous faciliter la vie : "*Les Dev Tools, c’est comme MS Office :
tout le monde s’en sert… à 5%.*" Il ne faut pas hésiter également à explorer les extensions, qui permettent souvent de débugger plus spécifiquement des frameworks front comme AngularJS, Ember, React...

Pour ceux qui préfèrent rester dans leurs éditeurs favoris, il existe également des solutions pour voir ses modifications en temps réel dans le navigateur. Beaucoup fonctionnent selon un principe très simple : détecter les changements dans la base de code et recharger la page dans le navigateur. Eh bien il existe mieux : beaucoup permettent maintenant le *hot swaping*, c'est-à-dire le remplacement du code sans rechargement dans vos pages. Pour le CSS, le déjà très connu [*browserSync*](http://www.browsersync.io/) le permet très facilement, en plus de proposer une synchronisation des actions sur plusieurs devices. On peut ainsi tester des actions utilisateurs sur plusieurs navigateurs ou devices en ne les effectuant qu'une seule fois (remplissage de formulaire, navigation, ...) Pour le JavaScript, c'est plus compliqué ; il existe cependant [*fb-flo*](https://facebook.github.io/fb-flo/) -- une extension chrome -- qui le permet, ou encore [*Webpack*](https://webpack.github.io/) avec [*monkey-hot-loader*](https://github.com/jlongster/monkey-hot-loader) qui permet de le faire sur tous les moteurs V8. 

Pour la fin de sa présentation, Christophe Porteneuve s'intéresse davantage aux chaînes de build. Aujourd'hui, il existe de nombreux outils bien plus performants que *browserify* ou *requireJS*. [*Webpack*](https://webpack.github.io/) et surtout [*JSPM*](http://jspm.io/) (qui est -- de mon point de vue -- la meilleure solution actuellement) permettent de gérer des *workflows* complexes et de compiler nos applications en *bundles*. Cela ne doit d'ailleurs pas gêner les phases de *debug* grâce aux fichiers [*source map*](http://www.html5rocks.com/en/tutorials/developertools/sourcemaps/) qui permettent de lier votre code compilé et minifié au code initial.

Il préconise également l'utilisation de *post-compilers*, c'est-à-dire des compilers permettant d'utiliser les nouvelles syntaxes (JavaScript, CSS, ...) qui ne sont pas encore supportées par les navigateurs. On pense ainsi à [*Traceur*](https://github.com/google/traceur-compiler), [*cssnext*](https://github.com/cssnext/cssnext) et [*Babel*](https://babeljs.io/). Ce dernier est merveilleux et je l'utilise dans tous mes nouveaux projets avec JSPM, mais je recommande néanmoins de rester prudent et de n'émuler que les fonctionnalités dont la syntaxe a été finalisée. Certaines propositions sont encore sujettes à trop de changement pour se permettre de les utiliser en production aujourd'hui. Enfin, pour automatiser ces chaînes de *build*, le conférencier nous recommande d'utiliser [*Gulp*](http://gulpjs.com/).

Si cette conférence peut sembler un simple rappel pour ceux qui se tiennent au courant de l'évolution des outils web, elle permet aux autres de se rattraper très facilement sur les dernières tendances en offrant un panorama global de l'écosystème actuel.

## [OpenID Connect, le nouveau standard d'authentification sur le web : mise en oeuvre sur FranceConnect](http://fr.slideshare.net/fpetitit/paris-web-2015-france-connect-et-openid-connect)

Tout le monde connaît aujourd'hui plus ou moins OpenID	 ; pour les autres, je vais tout de même le décrire. OpenID est un système d'authentification décentralisée qui permet de s'authentifier sur différent site le proposant en utilisant un seul et même identifiant (et souvent sans avoir à remplir un long formulaire d'inscription). Ce qu'on sait moins en revanche -- et c'est là le propos de [François Petitit](https://twitter.com/francoispetitit), c'est que OpenID est considéré comme obsolète et qu'on doit maintenant utiliser son successeur, OpenID Connect.
Il s'agit d'une surcouche du protocole OAuth2, ce qui lui permet d'offrir en plus du service d'authentification d'OpenID un service de gestion des autorisations. Il offre une interface HTTP RestFul utilisant JSON comme format de données.

Frédéric Petitit nous fait un retour d'expérience sur la mise en oeuvre de cette technologie sur FranceConnect. Mais qu'est-ce que FranceConnect ? Eh bien, c'est une surcouche sur OpenID Connect, qui va bien nous simplifier la vie en tant que français. Qui n'a pas déjà souffert de l'administration française, où chaque démarche réclame un nombre incalculable d'informations et de pièces à fournir ? Que ce soit pour la Caisse d'Allocation Familiale, pour les impôts ou pour toute autre démarche, les outils en ligne laissent aujourd'hui à désirer.

FranceConnect offre (ou offrira) un accès universel à toutes les adminstrations françaises. Plus besoin de s'inscrire individuellement à chacun des sites concernés, un même identifiant pourra être utilisé partout. Et ça, c'est une sacrément bonne nouvelle ! La plupart des informations seront pré-remplies, nous permettant de gagner un temps précieux. Cela va même plus loin, puisqu'en y connectant des services comme EDF ou notre offre internet, ces services pourront fournir automatiquement des pièces comme un justificatif de domicile lorsque c'est nécessaire. Et cela, simplement en autorisant l'accès (seulement lorsque nécessaire) aux sites concernés. Plus besoin de manuellement aller chercher tous les documents dont on a besoin, FranceConnect le fera pour nous, tout en nous laissant le contrôle total sur les informations personnelles qu'on souhaite fournir.

Via cet exemple, Frédéric Petitit nous montre clairement quels sont les avantages de l'utilisation de la technologie OpenID Connect, surtout quand on sait que beaucoup de grands acteurs l'ont d'ores et déjà adopté (qui a dit Google ?) Ci-dessous, un schéma résume l'implémentation qu'ils ont réalisé pour FranceConnect.

INSÉRER SCHEMA ICI

## [Webperf 2.0](http://stefounet.github.io/webperf2.0/#/)

## Panorama des solutions hybrides mobiles


## [CSP : Content Security Policy](http://www.nicolas-hoffmann.net/content-security-policy-parisweb-2015/#/)

[Nicolas Hoffmann](www.nicolas-hoffmann.net) nous présente dans cette conférence une technologie permettant de sécuriser très simplement et très efficacement son front-end. Il s'agit de Content Security Policy, dont la première spécification est plutôt bien supportée par les navigateurs actuels (avec quelques précautions pour IE 10-11). Pour les navigateurs ne la supportant pas, cela ne pose cependant aucun inconvénient puisque ceux-ci ignorent simplement les directives qu'on leur envoie.

Mais en quoi consiste cette technologie ? Il s'agit tout simplement d'envoyer via les headers HTTP des directives au navigateur pour lui indiquer strictement ce qu'il est autorisé de faire. Attention, on ne peut pas seulement refuser ce qui ne nous convient pas, il faut autoriser tout ce dont a besoin notre front-end sous peine de se le voir interdire ! Cela peut paraître contraignant, mais c'est la seule façon d'être certain de ne pas oublier des restrictions, ce qui serait potentiellement dangereux.

Mais de quoi nous protège CSP ? Il permet principalement d'éviter les failles *cross-site scripting* (XSS), c'est-à-dire l'inclusion et l'exécution d'un code malveillant dans notre page. Pour cela, on peut décider de n'autoriser que les scripts ou contenus issus du même nom de domaine que notre site, ou bien interdire les scripts dits *inline* pouvant être ajoutés dans des contenus utilisateurs, ... Les directives sont à insérer dans le header HTTP `Content-Security-Policy:` et se présentent par exemple sous cette forme : `script-src 'self' 'unsafe-inline' ;`

De par son expérience, Nicolas Hoffmann nous recommande cependant d'être prudent sur la mise en place en utilisant deux headers supplémentaires. Le premier, `Content-Security-Policy-Report-URI`, permet de spécifier une adresse sur laquelle le navigateur pourra envoyer des alertes pour chaque contenu bloqué. Cela permet ainsi au webmaster de suivre très exactement ce qui est bloqué et donc de pouvoir repérer facilement des autorisations oubliées. La seconde, `Content-Security-Policy-Report-Only`, permet d'indiquer au navigateur de seulement simuler les directives, c'est-à-dire de ne pas bloquer effectivement les contenus, mais de soulever quand même des alertes. Cela permet donc d'effectuer ses tests en toute sérénité sans que l'utilisateur en pâtisse.

## [Vorlon.JS : un outil pour simplifier le debug web sur toutes les plateformes]()

## [Découper son application monolithique : Pourquoi ? Comment ?](https://speakerdeck.com/odolbeau/slicing-up-a-monolithic-application-why-and-how)

Benjamin Fraud et Olivier Dolbeau nous font ici un retour sur la mise en place d'une architecture micro-services chez [Blablacar](https://www.blablacar.fr/). Avant cela, leur site web était une application monolithique, c'est-à-dire une grosse application rassemblant tous les services REST et toutes les couches métiers de l'écosystème Blablacar. Tant que celui restait relativement petit, cette organisation fonctionnait très bien, mais avec l'augmentation de la base de code, de nombreux problèmes ont fini par se poser. 

Pour commencer, avec leur processus de déploiement continu, leur workflow de livraison prenait une vingtaine de minutes, voire parfois bien plus. Cela peut sembler peu, mais lorsqu'on problème se pose en production, vingt minutes représente de très nombreuses pertes pour Blablacar.

De même, une application monolithique se révélait très compliquée à *scaler* facilement et à répliquer pour permettre de cibler les utilisateurs géographiquement.

Au niveau de la *developper experience* (j'en parlais plus haut), la base de code était devenue trop importante pour s'y retrouver facilement. L'interdépendance des modules provoquait des effets *boule de neige* lorsqu'on ne vérifiait pas assez les conséquences de certains changements ; un effet qu'Olivier résume par "*With minor changes comes major bugs.*" Au niveau de la gestion de version, il fallait régler de nombreux conflits, plusieurs personnes intervenant régulièrement sur les mêmes parties du code, entraînant des `rebase` conséquents et pénibles.

Pour toutes ces raisons, Blablacar a donc choisi de s'orienter sur une architecture en micro-services : un ensemble de projets spécialisés chacun sur une seule brique métier. L'un prend par exemple en charge les utilisateurs, un autre la modération, un troisième les réservations... Tous ces services communiquent via un *broker* de messages.

Chez Blablacar la règle est simple : un service ne peut en aucune cas demander à un autre service d'effectuer des actions métier. Il peut uniquement demander les données qui lui sont nécessaires pour ses traitements. Par contre, un service peut émettre des évènements lorsqu'il réalise certaines opérations pour notifier d'autres services.

Les avantages sont nombreux. Avec ce système, les livraisons en production sont très rapides et surtout ciblées. Une déficience d'un service ne peut pas faire tomber les autres. L'application est plus facilement *scalable* et plus rapidement au moment des pics de charge. La base de code reste raisonnable car répartie entre de nombreux projets. Enfin, le nombre de conflits entre codeurs durant le développement a beaucoup diminué. Mais comme le précise les deux *speakers*, les micro-services ne sont pas une solution miracle, et apportent leur lot d'inconvénients.

En effet, l'initialisation d'une nouvelle brique métier est beaucoup plus longue, même en ayant des *pattern* d'applications. De même, un projet a dû être spécifiquement créé pour gérer la configuration de tous ces projets. La durée d'apprentissage d'un nouveau développeur sur le projet est également beaucoup plus longue. Enfin, du côté *devops*, la gestion est devenue bien plus complexe.

Si pour Blablacar les avantages surpassent de loin les inconvénients, les deux intervenants nous enjoignent donc à réfléchir très sérieusement avant de choisir de faire évoluer son architecture.