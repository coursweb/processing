---
layout: page
title: Setup & Draw
permalink: setup-draw.html
---

Exemple de code 

Dessiner des cercles 
C'est l'exemple 2-2 : 

```javascript
function setup() { 
  createCanvas(480, 120);
}
function draw() {
  if (mouseIsPressed) {
    fill(0); }
  else{
    fill(255); 
  }
  ellipse(mouseX, mouseY, 80, 80);
}
```