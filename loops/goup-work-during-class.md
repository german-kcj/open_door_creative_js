# Goup Work During Class

### Loop Art - Attempting to recreate Vera Molnar's art

{% hint style="danger" %}
**Current Challenge**

Complete the recreation of Vera's art.  Replace the rect function to include vertex.  Check the reference for more information.
{% endhint %}

#### Inspiration

<figure><img src="../.gitbook/assets/Screen Shot 2023-10-04 at 8.43.37 PM.png" alt="" width="375"><figcaption></figcaption></figure>

### Work Completed in Class

<figure><img src="../.gitbook/assets/Screen Shot 2023-10-04 at 8.44.49 PM.png" alt="" width="375"><figcaption></figcaption></figure>

### Code

```javascript
let space = 80;
function setup() {
  createCanvas(400, 400);
  background(255);
  stroke("teal");
  noFill();
}

function draw() {
  for (let x = 0; x < 400; x += space) {
    for (let y = 0; y < 400; y += space) {
      for (let z = 0; z < 80; z += 15) {
        rectMode(CENTER);
        if (random() > 0.3) {
          // Don't use rectangles
          // Use vertex
          rect(x + space / 2, y + space / 2, z);
        }
      }
      rectMode(CORNER);
      rect(x, y, space);
    }
  }
  noLoop();
}

```

### Link to Project in p5js

[**https://editor.p5js.org/Garcila/sketches/7eCphtsTA**](https://editor.p5js.org/Garcila/sketches/7eCphtsTA)
