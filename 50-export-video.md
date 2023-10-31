---
layout: page
title: Export Vidéo
permalink: export-video.html
---

Pour exporter les visuels de processing, il existe différentes méthodes:

### avec Processing (Java)

Pour processing 4 il faut une nouvelle version du bibliothèque export video, ici:

https://github.com/hamoid/video_export_processing/tree/kotlinGradle#using-the-library

Suivre le processus pour installer le dossier library.

Un exemple pour tester si ça marche.
L'enregistrement débute automatiquement. Pour le terminer et exporter le fichier, il faut presser la touche «q».

```
import com.hamoid.*;
VideoExport videoExport;


void setup() {
  /* - - - - - - - - - - - - */
  // options animation 
  size(1920, 1080);
  frameRate(25);
  // options vidéo
  videoExport = new VideoExport(this, "prenom-nom.mp4");
  videoExport.setQuality(70, 0); // qualité video, audio – 0 = pourri, 100 = top
  videoExport.setFrameRate(25);  
  videoExport.setLoadPixels(false);
  videoExport.setDebugging(false);
  videoExport.startMovie();
  /* - - - - - - - - - - - - */

  // setup de votre animation si besoin…

}

void draw() {
  /* - - - - - - - - - - - - */
  // votre animation…
  
  for(int x = 0; x < width; x++){
    stroke( /*R*/random(255), /*G*/random(255), /*B*/random(255) );
    line(x, 0, x, height);
  }


  /* - - - - - - - - - - - - */
  // enregistrement vidéo:
  loadPixels();  
  videoExport.saveFrame();
  updatePixels();
}

void keyPressed() {
  if (key == 'q') {
    videoExport.endMovie();
    exit();
  }
}
```

### avec P5.JS

Une méthode utilisant la librairie [CCapture.js](https://github.com/spite/ccapture.js/), documentée dans deux vidéos:

* [Vidéo de Stubborn Code](https://www.youtube.com/watch?v=bVlIFf-hffY)
* [Vidéo de Colorful Coding](https://www.youtube.com/watch?v=-JkGPCQVYf0)

Le format Webm peut être converti en MP4 par différents moyens: 

* Site web: [https://cloudconvert.com/](https://cloudconvert.com/)
* Logiciel: [HandBrake](https://handbrake.fr/downloads.php)

Code d'exemple:

[Site archivé de StubbornCode](https://web.archive.org/web/20201203193530/https://stubborncode.com/posts/how-to-export-images-and-animations-from-p5-js/)

```
const letters = ["C", "D", "E", "O"];

const capturer = new CCapture({
  framerate: 25,
  format: "webm",
  name: "movie",
  quality: 100,
  verbose: true,
});

let p5Canvas;

function setup() {
  p5Canvas = createCanvas(1080, 1080);
  frameRate(25);
}


function draw() {
  if (frameCount === 1) capturer.start();
  background(20);
  for (let y = 0; y <= height; y += 40) {
    for (let x = 0; x <= width; x += 40) {
      push();
      translate(x, y);
      fill(random(255), random(255), random(255), random(255));
      text(random(letters), 0, 0);
      pop();
    }
  }
  capturer.capture(p5Canvas.canvas);
  if (frameCount === 125) {
    noLoop();
    capturer.stop();
    capturer.save();
    }
}
```