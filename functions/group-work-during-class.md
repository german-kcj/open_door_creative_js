# Group Work During Class

### Text Functions

<div data-full-width="false">

<figure><img src="../.gitbook/assets/Screen Shot 2023-09-27 at 8.37.15 PM.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

### Code

```javascript
function setup() {
  createCanvas(500, 400);
}

function draw() {
  background(220);  
  // function excecution or calling
  sayHello(100,100, "Hello World 🌏", 255, 255, 255, 10);
  sayHello(250,220, "Hello Kitty 😻", 255, 255, 0, 20);
  sayHello(350,300, "I am Hungry 🍓", 255, 0, 255, 30);
}

/* function declaration
it is part of the same
comment
*/
function sayHello(positionX, positionY, customText, R, G, B, fs) {
  textSize(fs);
  fill(R, G, B);
  text(customText, positionX, positionY);
}
```

### Link to Project in p5js

{% embed url="https://editor.p5js.org/Garcila/sketches/xtducVRzD" %}

***

### Function Circles

<figure><img src="../.gitbook/assets/Screen Shot 2023-09-27 at 8.40.31 PM.png" alt="" width="375"><figcaption></figcaption></figure>

### Code

```javascript
function setup() {
  createCanvas(500, 400);
}

function draw() {
  background(0);
  planet(10, color(208, 0, 0), color(0, 0, 0), 200, 200, 200);
  planet(5, color(255, 286, 8), color(63, 136, 197), 100, 100, 20);
  planet(1, color(3, 43, 67), color(3, 43, 67, 120), 300, 100, 100);
  planet(10, color(19, 111, 99), color(255, 255, 255, 20), 30, 10, 200);
  
  textSize(50);
  fill(255);
  text(add(10,10), 200,200);
}

function planet(border, borderColor, fillColor, X, Y, D) {
  strokeWeight(border);
  stroke(borderColor);
  fill(fillColor);
  circle(X, Y, D);
}

function add(num1, num2){
  return num1 + num2;
}

// strokeWeight(10);
// stroke(208, 0, 0);
// fill(0,0,0);
// circle(200,200,200);

// strokeWeight(5);
// stroke(255, 186, 8);
// fill(63, 136, 197);
// circle(100,100,20);

//   strokeWeight(1);
//   stroke(3, 43, 67);
//   fill(3, 43, 67,120);
//   circle(300,100,100);

// strokeWeight(10);
// stroke(19, 111, 99);
// fill(255, 255, 255, 20);
// circle(30, 10, 200);

```

### Link to Project in p5js

[https://editor.p5js.org/Garcila/sketches/ZF2EXWkCG](https://editor.p5js.org/Garcila/sketches/ZF2EXWkCG)
