---
description: Activities created in class and submitted by the group
---

# Group Work During Class

### Race

<figure><img src="../.gitbook/assets/Screen Shot 2023-09-25 at 8.47.10 PM.png" alt=""><figcaption></figcaption></figure>

### Code

```javascript
let pinkX = 50;
let greenX = 50;
let peachX = 50;

function setup() {
  createCanvas(700, 400);
  textAlign(CENTER);
}

function draw() {
  background(169, 222, 249);

  noStroke();
  fill(252, 246, 189);
  rect(0, 0, 100, 400);

  fill(228, 193, 249);
  rect(600, 0, 100, 400);

  // PINK
  fill(255, 153, 200);
  circle(pinkX, 200, 60);
  
  // pinkX = pinkX + random(-2,6);
  
  if (pinkX > 600 - 30) {
    stroke(255);
    fill(255);
    textSize(30);
    text("Pink Wins!", width / 2, 200);
    noLoop();
  }

  // GREEN
  fill(208, 244, 222);
  noStroke();
  circle(greenX, 100, 60);

  // greenX = greenX + random(-2,6);

  if (greenX > 600 - 30) {
    stroke(255);
    fill(255);
    textSize(30);
    text("Green Wins!", width / 2, 200);
    noLoop();
  }
  
  
  // PEACH
  fill(250, 183, 140);
  noStroke();
  circle(peachX, 300, 60);

  // peachX = peachX + random(-2,6);

  if (peachX > 600 - 30) {
    stroke(255);
    fill(255);
    textSize(30);
    text("Peach Wins!", width / 2, 200);
    noLoop();
  }
}

function keyPressed() {
  if (key === "a" || key === 'A') {
    peachX = peachX + random(5, 20);
  }
  if (key === "h" || key === 'H') {
    greenX = greenX + random(5, 20);
  }
  if (key === "p"|| key === 'P') {
    pinkX = pinkX + random(5, 20);
  }
}
```

### Link to the project in p5

[https://editor.p5js.org/Garcila/sketches/rhmITEuWr](https://editor.p5js.org/Garcila/sketches/rhmITEuWr)
