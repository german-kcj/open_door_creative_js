# Group Work During Class

### Object and Classes

<figure><img src="../.gitbook/assets/Screen Shot 2023-10-17 at 9.07.41 AM.png" alt=""><figcaption></figcaption></figure>

#### sketch.js

```javascript
let allBobs = [];

function setup() {
  createCanvas(600, 400);
  angleMode(DEGREES)
}

function draw() {
  background(25);
  for(let i = 0; i < allBobs.length; i++){
    allBobs[i].show();
    allBobs[i].move();
    allBobs[i].mutate();
  }
  
}

function mousePressed(){
  let bobby = new Bob(random(5,15),random(255), random(100), random(50));
  allBobs.push(bobby);
}
```

#### bob.js

```javascript
class Bob {
  constructor(diam, r, g, b){
    this.x = mouseX;
    this.y = mouseY;
    this.r = r;
    this.g = g;
    this.b = b;
    this.diam = diam;
  }
  show(){
    noStroke();
    fill(this.r,this.g,this.b, random(10,200));
    circle(this.x, this.y, this.diam);
  }
  move(){
    this.x += random(-5,5);
    this.y += random(-5,5);
  }
  mutate(){
    this.r += random(-50,50);
    this.g += random(-50,50);
    this.b += random(-50,50);
  }
}
```

#### index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.7.0/p5.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.7.0/addons/p5.sound.min.js"></script>
    <link rel="stylesheet" type="text/css" href="style.css">
    <meta charset="utf-8" />

  </head>
  <body>
    <main>
    </main>
    <script src="sketch.js"></script>
    <script src="bob.js"></script>
  </body>
</html>

```

#### style.css

```css
html, body {
  margin: 0;
  padding: 0;
}
canvas {
  display: block;
}

```

[p5.js LINK](https://editor.p5js.org/Garcila/sketches/2\_Mup7W36)
