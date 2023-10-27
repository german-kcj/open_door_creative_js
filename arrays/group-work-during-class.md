# Group Work During Class

**Array Introduction**

```javascript
let vehicles = [7, "🚕", "🚚", "🚜", "🚒"];

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(255);
  textSize(50);
  
  for(let i = 0; i < vehicles.length; i++){
    text(vehicles[i], 20, 50 * i +50);
  }
}

```

p5.js [LINK](https://editor.p5js.org/Garcila/sketches/R8Sn1xVCJ)

***

**Bank Account**

```javascript
let account = [];
let balance = 0;

function setup() {
  createCanvas(400, 400);
  for(let i = 0; i < 10; i++){
    account.push(round(random(-100,100),2));
  }
  console.log(account);
  
  account.push(100);
  
  for(let i = 0; i < account.length; i++){
    balance = balance + account[i];
    console.log(balance);
  }
  
  
}

function draw() {
  background(220);
}
```

p5.js [LINK](https://editor.p5js.org/Garcila/sketches/gynL5z\_N1)

***

**Another way of writing a for-loop**

```javascript
let things = [1, 4, 7, 4, 'cat', true, false, '🚁'];

function setup() {
  createCanvas(400, 400);
  
  for(let thing of things){
    console.log(thing);
  }
  
  for(let i = 0; i < length; i++){
    console.log(things[i]);
  }
  
}

function draw() {
  background(220);
}
```

p5.js [LINK](https://editor.p5js.org/Garcila/sketches/XP-SAeFbn)
