# 1. Vocabulaire général
## KiCad
*KiCad* est un ensemble de logiciels permettant la conceptions de circuits imprimés (*EDA* en
anglais). Il se compose principalement d'un logiciel de création de schémas, d'un autre pour
produire un circuit imprimé basé sur le schéma créé. Il offre aussi quelques outils pour créer des
symboles et générer des traces. KiCad permet donc bien sûr de connecter ces différents modules
entre-eux dans des projet.

Une autre alternative à KiCad fréquemment utilisée en industrie et *Altium*. Les concepts demeurent
les mêmes à travers ces logiciels donc il vous sera facile de le prendre en main par la suite!

## *EDA* - *Electronic Design Automation*
La conception et la fabrication de PCBs ce déroule en plusieurs étapes interreliées. Ainsi, le
processus commence par analyser les requis et déterminer les pièces utilisées ainsi que la manière
dont elles sont reliées. Dans certains cas, il faut aussi définir nos propres pièces en se basant
sur leur datasheet. Ensuite, il faut importer ces pièces pour les placer sur le circuit imprimé,
ainsi que définir les traces nécessaires pour les connecter. De plus, il faut déterminer
l'emplacement des plaques de cuivre pour souder ces dernières à notre circuit imprimé. La dernière
étape pour la production consiste à exporter les différentes couches du PCB en fichiers d'assemblage
afin de les envoyer à une compagnie qui pourra imprimer et assembler nos PCBs.

Un *EDA* est un logiciel qui regroupe toutes les fonctionnalités mentionnées. C'est l'équivalents de
logiciels de CAD (*Computer-Aided Design*) pour les ingénieurs en mécanique. Certains *EDA*
permettent même la conception des circuits à l'intérieur même des circutis intégrés.

## Circuit imprimé (*PCB* - *Printed Circuit Board*)
Un circuit imprimé est une manière compacte de relier plusieurs composants électroniques entre-eux.
[Image](https://en.wikipedia.org/wiki/Printed_circuit_board#/media/File:SEG_DVD_430_-_Printed_circuit_board-4276.jpg)
Le PCB en lui même est composé d'une alternance de couches d'un conducteur (généralement du cuivre)
et d'un isolant. L'une des étapes de fabrication de ces derniers consiste à enlever le la matière
conductrice pour isoler des traces. Les traces représentent des "fils" qui permettent de connecter
les différentes puces ou composants présents sur le PCB.

## Datasheet
Les datasheet sont parfois intimidants, mais restent la meilleure manière de savoir comment utiliser
une puce électronique. Elles nous donnent des informations sur les caractéristiques électriques, les
fonctionalités, des exemples d'utilisation des puces et plus encore. Comme le format varie d'un
manufacturier à l'autre il n'y a pas de manière unique pour comprendre les informations qui s'y
trouvent. Malgré tout, avec la pratique, il devient beaucoup plus facile de trouver l'information
qu'on cherche!

## Libraires
Les librairies sont une manière d'organiser les symboles ou empreintes fréquemment utilisées à
travers un ou plusieurs PCBs. Ces dernières peuvent être globales pour être réutilisées à travers
plusieurs projets, tandis que d'autres sont spécifiques au projet. Dans notre cas, nous auront une
librairie globale pour les composantes qui seront utilisés par plusieurs PCBs, mais il se peut que
certains symboles ne soient nécessaires que pour un projet. Dans le cadre de la formation, seule une
librairie spécifique au projet sera nécessaire.

# 2. Schémas et symboles
## Schéma (*Schematic*)
Le schéma indique les composants utiles à un circuit donné ainsi que la manière dont ils doivent
être connectés. KiCad nous permet de dessiner des fils, mais aussi des regroupements de fils (des
bus) pour représenter ces connexions. De plus, il est possible d'utiliser différents type
d'étiquettes (*labels*) pour éviter d'avoir trop de fils sur le schéma.

## Symbole (*Symbol*)
Un symbole permet de représenter une puce électronique ou tout autre composante dans un schéma.
KiCad vient avec une grande librairie de symbole qu'on peut facile utiliser dans nos schémas, mais
il peut être nécessaire de créer les nôtres ou d'en importer de la page du manufacturier.

## Net(class)
Un *netclass* représente un ensemble de fils qui doivent être connectés entre-eux. Par exemple, les
PCBs ont toujours un netclass *GND* qui contient tous les fils qui doivent être connectés au *GND*.

# 3. Placement et routage
## Routage (*Routing*)
Le routage consiste à déterminer où faire passer les traces pour connecters les composants sur le
PCB. C'est une étape assez complexe, car le nombre de connexions peut grandir très vite. Il est
possible de le faire à la main, mais il existe des outils pour faire le routage automatiquement.

## Trace
Une trace est un morceau isolé dans une couche de conducteur du PCBs. Il permet de connecter deux
composants ou plus entre-eux. Les traces sont donc équivalentes à des fils. Leur épaisseur peut être
changée, notamment si l'on veut faire passer plus de courant. Il est préférable de limiter les
angles droits lorsque l'on dessine les traces.

## Plan (*Plane*)
## Empreinte (*Footprint*)
## Via
Un via est un trou passant au travers d'une ou plusieurs couches isolantes du PCB et dont les parois sont recourvertes de matériau conducteur. Cela permet de connecter les traces de différentes couches conductrices du PCB. Il est possible de changer la taille du via et l'épaisseur des parois conductrices. Il existe trois types de vias:
- Via traversant (*Through-Hole Via*): Traverse toutes les couches du PCB.
- Via borgne (*Blind Via*): Lie une couche extérieure et une ou plusieurs couches intérieures du PCB. Ce via n'est donc pas visible sur l'autre couche extérieure du PCB et doit être sur un PCB à plus de 2 couches.
- Via enterré (*Buried Via*): Lie deux couches intérieures du PCB. Ce via n'est donc pas visible vu de l'extérieur du PCB et doit être sur un PCB à plus de 2 couches.
Dans le cadre de notre projet, nous n'auront que 2 couches sur nos PCB et n'utiliseront que des vias *through-holes*.

## Pièces assemblées en surface (*Surface Mount*)
## Pièces assemblées à travers (*Through-hole*)
# 4. Impression et assemblage
## Fichiers d'impression (*Gerber Files*)
## Assemblage (*Assembly*)
# 5. Composants électroniques
## MOSFET
## Voltage regulator
