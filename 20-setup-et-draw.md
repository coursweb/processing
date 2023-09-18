---
layout: page
title: Setup & Draw
permalink: setup-draw.html
---

Exemples de code :

Dessiner une ligne:

```javascript
function setup() {
  createCanvas(480, 120);
}
function draw() {
  background(204); 
  line(20, 50, 420, 110);
}
```


Dessiner des cercles: 

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