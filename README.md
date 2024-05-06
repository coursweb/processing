# Processing et P5.JS

## Termes principaux

**Variable :** définir une variable, c'est définir un mot-clé, comme p.ex. "vitesse", qui contiendra un nombre pouvant changer.

Dans P5, `width` et `height` sont des variables par défaut (indiquent la hauteur et largeur du canevas).

D'autres variables sont: `mouseX` et `mouseY`, qui correspond à la valeur x et y de la position de la souris.

**Nommer une variable :** on peut définir librement une variable, mais il faut éviter les termes déjà utilisés par P5.js (voir [référence](https://p5js.org/reference/)) ou [les mots-clés réservés du javascript](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Lexical_grammar#mots-cl%C3%A9s) (reserved names).

Pour éviter des conflits avec les mots-clés réservés, on va souvent préfixer ses variables, comme: My_vitesse, ProjectName_vitesse, etc.



Thèmes en vrac:

- Formes et dessin
- Couleurs
- Les variables mouseX & mouseY
- Les boucles, while & for

## Exemples de P5.JS:

Voici le code de l'exemple Hello_P5:_shapes

```javascript
function setup() {
  // Create the canvas
  createCanvas(720, 400);
  background(200);

  // Set colors
  fill(204, 101, 192, 127);
  stroke(127, 63, 120);

  // A rectangle
  rect(40, 120, 120, 40);
  // An ellipse
  ellipse(240, 240, 80, 80);
  // A triangle
  triangle(300, 100, 320, 100, 310, 80);
}
```

<iframe width="100%" style="aspect-ratio: 4/3" src="https://editor.p5js.org/p5/full/hhu8mAXJpQ7"></iframe>

## Commandes de base

Dessiner une ligne:

```javascript
line(15, 25, 70, 90);
```

Couleur de fond:

```javascript
background(192, 64, 0);
```

Changer la couleur du trait:

```javascript
stroke(255);                // le trait sera blanc
stroke(255, 255, 255);      // blanc, mais en RVB
stroke(255, 128, 0);        // orange clair
stroke(#FF8000);            // toujours orange clair
stroke(255, 128, 0, 128);   // orange avec 50% de transparence
```
