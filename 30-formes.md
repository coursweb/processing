---
layout: page
title: Formes
permalink: formes.html
---

Liste de formes disponibles dans P5.js

Les formes 2D:

```
point()
line()
triangle()

// carrés et rectangles
square()
rect()
quad()

// formes rondes
circle()
ellipse()
arc()
```

Voir [la Référence P5.js](https://p5js.org/reference/)

Explications:

![](img/line.jpg)

Exemple: `line(30, 20, 85, 75);`

![](img/triangle.jpg)

Exemple: `triangle(30, 75, 58, 20, 86, 75);`

![](img/rect.jpg)

Exemple: `rect(30, 20, 55, 55);`

![](img/quad.jpg)

Exemple: `quad(20, 20, 80, 20, 80, 80, 20, 80);`

![](img/ellipse.jpg)

Exemple: `ellipse(56, 46, 55, 55);`

Les paramètres 1 et 2 définissent le centre de l'ellipse.  
Les paramètres 3 et 4 donnent la largeur et hauteur.

![](img/arc.jpg)

Exemple: `arc(50, 55, 50, 50, 0, HALF_PI);`