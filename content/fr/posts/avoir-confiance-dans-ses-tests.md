---
title: "Avoir confiance dans ses tests"
date: 2025-06-17T14:00:00+00:00
# weight: 1
# aliases: ["/first"]
tags: ["testing", "automated", "methods", "TDD"]
author: "Nicolas Barbey"
showToc: true
TocOpen: false
draft: true
comments: false
description: ""
canonicalURL: "https://canonical.url/to/page"
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption undercover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/nbarbey/nbarbey.github.io/blob/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---


# Est-ce que vous avez confiance dans vos tests ?

C'est une question qui peut paraitre évidente.
Bien sûr que j'ai confiance dans mes tests !
Je les ai écrits, je sais ce que je fais.
Ça fait des années que je fais des tests de la même façon.
Mes collègues sont contents pendant les revues.
Nous, on fait même 100% de couverture !

Et pourtant, est-ce que vous déployez le vendredi soir ?
Est-ce que vous seriez à l'aise d'envoyer chaque commit en production
dès qu'il est mergé ?
Est-ce que vous avez déjà eu une régression alors que tous vos tests passent ?

Je sais ce que vous allez me dire. Mais, là, tu demandes la lune. Il faut accepter
qu'il y aura des régressions. On ne peut pas prévoir tous les cas.

Et pourtant je sais que c'est possible d'aller plus loin que beaucoup dans la
façon de tester. C'est possible, car certains le font. Et ça change tout.
Aussi bien leur quotidien de développeur que la manière de progresser sur le produit.

# Une autre façon de voir les tests

Quand je vois des gens tester leur code, ça se passe comme ça la plupart du temps :
- la personne écrit sa fonction
- elle écrit un test pour sa fonction
- elle écrit une autre fonction qui appelle la première
- elle écrit un test pour la nouvelle fonction, parfois avec un mock de la première fonction pour limiter le test à une fonction.
- et ainsi de suite…

L'idée, c'est de tester des petits morceaux de code afin de ne pas avoir trop à tester d'un coup.

Le problème avec cette approche, c'est l'interaction entre les fonctions (ou les classes ou autre). Chaque test suppose de manière implicite un certain comportement des fonctions dont elle dépend. Si ces suppositions sont fausses, on peut casser la production !

Mais on n'est pas obligés de faire comme ça. Un test peut tester l'ensemble du code nécessaire à une fonctionnalité. Dans ce cas, il n'y a plus de supposition sur le comportement d'autres zones du code, donc plus de risque de faire de fausses suppositions, et ainsi moins de risque d'introduire des bugs.

En faisant cela, on peut placer le test au plus près de l'utilisateur. Le test peut alors décrire le comportement possible de l'utilisateur. Si on ne change pas le test, le comportement pour l'utilisateur ne change pas. On n'introduit donc pas de bug. Et on peut le prouver avec les tests.

Chaque nouveau test peut correspondre à un nouveau cas de comportement de notre logiciel : un cas passant, un cas d'erreur, un cas limite, une variante d'utilisation, etc.

On teste plus de code, mais l'assurance que nous donne un test est beaucoup plus grande qu'avec l'autre approche.

TODO : parler de base de données et de performance.

# Le contrat, Lagaffe

C'est bien beau tout ça, mais parfois notre code dépend du code d'une autre équipe ou
d'une autre société. C'est le cas en particulier lorsque notre code fait un appel d'API
HTTP vers l'extérieur.

Dans ce cas, on est en général obligés d'utiliser des mocks pour nos tests. C'est-à-dire
une dépendence qui va remplacer la vraie dépendence dans le cas des tests.
On retombe alors sur le problème précédent que cette fausse dépendence de test peut
potentiellement faire de mauvaises suppositions sur la manière dont fonctionne la
dépendence de production.

Cette situation est plus compliquée à tester. C'est un bon exemple de situation où les
tests peuvent guider la conception de notre code. Est-ce qu'il ne serait pas possible
de récupérer la donnée qui nécessite l'appel d'API plutôt d'une manière asynchrone en amont
de l'utilisation de notre code.
Si c'était le cas, ce nouveau design permettrait de rendre la production plus robuste
car notre service continuerait à fonction même si le service fournissant l'API que l'on appelait était indisponible.

Si l'on est malgré tout obligé de faire notre appel HTTP, il nous faut alors utiliser un mock
pour nos tests. L'idéal étant d'utiliser un fake. C'est-à-dire une sorte de dépendence de test qui ait le même comportement que la vraie dépendence.

Et on peut également garantir que le fake et la dépendence de production ait le même comportement.

Si les deux codes utilisent le même langage, les fournisseurs de l'API peuvent également
fournir le fake et exécuter la même suite de test contre les deux implémentations.
Cela permet de garantir le même fonctionnement à l'aide de tests unitaire.
C'est une forme de test que l'on appelle test de contrat (ou contract testing en anglais).

Si les deux codes n'utilisent pas le même langage, il est possible de mettre en place une
approche similaire. Il faudra alors sérialiser la description du comportement dans
un format particulier compréhensible par les deux langages.
C'est ce que propose un outil comme Pact, qui fournit un outil de gestion de ces contrats
et des bibliothèques permettant d'implémenter des tests de ce type dans de nombreux
langages.

# Explorer plus loin

Ces approches ne signifient pas qu'il est possible de se passer entièrement de tests
manuels. Elles permettent que les tests manuels n'aient pas à être fait en amont
de la mise en production de notre code tout en maximisant le niveau de garantie que
l'on peut avoir avec des tests automatiques.

Les tests manuels peuvent maintenant être faits sur la production ou sur un environement similaire afin d'explorer les zones d'ombres du fonctionnemnet de notre logiciel qui n'ont
pas été pensés par les personnes qui ont écrit les tests automatiques.
