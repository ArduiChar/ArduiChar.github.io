---
title: "Le Projet"
description: "Description du Projet"
lead: ""
date: 2022-01-07T22:19:51.911Z
lastmod: 2022-01-07T22:19:51.911Z
draft: false
images: []
menu:
  docs:
    parent: "introduction"
weight: 110
toc: true
contributors: ["GogoVega"]
---

Notre robot est un char pouvant se déplacer en avant, en arrière ainsi que latéralement. Il est composé de quatre roues motrices, d’un capteur ultrasons lui permettant de détecter des obstacles, d’un buzzer, d’un tag RFID, d’un afficheur LCD, d’un écran OLED et de LEDs. Il peut être télécommandé via une communication Bluetooth. Le robot est aussi muni d’un bras articulé composé de servomoteurs capables d’attraper des petits objets grâce à une pince.

## Fonctionnement:

### Mode Automatique

Ce mode permet au robot d’avancer de manière autonome en évitant les obstacles.
Le mode automatique fonctionne de la manière suivante : tant que le sonar (ultrason) ne détecte rien dans un rayon de 10cm, le robot avance et dès que le rayon passe sous les 10cm, le robot s’arrête et rentre en mode évitement d’obstacle. Ce mode s’exécute de la manière suivante :

1. Le robot tente un quart de tour vers la gauche
2. Le robot tente un quart de tour vers la droite
3. Le robot revient dans la position initiale
4. Le robot recule

Pour les points 1 et 2, si la distance devient inférieure à la distance minimale (5cm), le robot s’arrête et passe à l’étape suivante. De même, si la distance devient supérieure à la distance maximale (et qu’on ai au moins effectué un huitième de rotation) cela voudrait dire que le robot a trouvé un passage et sortira de ce mode pour avancer tout droit jusqu’au prochaine obstacle.
Pour le point 4, puisque les deux premières tentatives ont échouées, le robot recule de sa longueur afin de recommencer à partir du point 1.

### Mode Manuel

Le mode manuel permet de contrôler le robot grâce à une télécommande sur laquelle ce trouve un joystick qui gère l’avancement et la direction. Et quatre boutons permettant de lever/baisser le bras, serrer/desserrer la pince.
