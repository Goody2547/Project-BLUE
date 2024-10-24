# Project-BLUE
There are 3 types of color blindness tests in my A2 project. This is the 2nd one (BLUE).

//Add project details (BLUE)
let x = 100;
let y = 100; 
let z = 0;
let a = 240;
let b = 380;
let c = 520;
let goLeft = false;

function setup() {
  createCanvas(600, 600); 
}

function draw() {
  background(220); // Set the background color
  
  // Make the color bars with rectangle shapes
  fill("#001134"); noStroke(); rect(0, 0, 100, height);
  fill("#001b56"); noStroke(); rect(100, 0, 100, height);
  fill("#002a84"); noStroke(); rect(200, 0, 100, height);
  fill("#0034a4"); noStroke(); rect(300, 0, 100, height);
  fill("#0042d0"); noStroke(); rect(400, 0, 100, height);
  fill("#0051ff"); noStroke(); rect(500, 0, 100, height);
  
  // Fill color for "B" based on position X
  if (x > 50 && x <= 240) {
    fill("#ffdf41"); // Light yellow for "B"
  } else if (x > 240 && x <= 380) {
    fill("#f8cf00"); // Yellow for "B"
  } else if (x > 380 && x <= 520) {
    fill("#bf9f00"); // Dark yollow for "B"
  } else if (x > 520 && x <= 550) {
    fill("#877100"); // Darkest yellow for "B"
  } else{
    fill("#ffed94"); // Lightest yellow for "B"
  }
  textSize(300);
  textFont("IMPACT");
  textAlign(CENTER);
  text("B", x, y, z); // Make latter "B" with position X
  
  // Fill color for "L" based on position A
  if (a > 240 && a <= 380) {
    fill("#f8cf00"); // Yellow for "L"
  } else if (a > 380 && a <= 520) {
    fill("#bf9f00"); // Dark yellow for "L"
  } else if (a > 520 && a <= 550) {
    fill("#877100"); // Darkest yellow for "L"
  } else if (a > 100 && a <= 240){
    fill("#ffdf41"); // Light yellow for "L"
  }
  text("L", a, y, z,); // Make latter "L" with position A
  
  // Fill color for "U" based on position U
  if (b > 380 && b <= 520) {
    fill("#bf9f00"); // Dark yellow for "U"
  } else if (b > 520 && b <= 550) {
    fill("#877100"); // Darkest yellow for "U"
  } else if (b > 100 && b <= 240) {
    fill("#ffdf41") // Light yellow for "U"
  } else if (b > 240 && b <= 380) {
    fill("#f8cf00"); // Yellow for "U"
  }
  text("U", b, y, z); // Make latter "U" with position B
  
  // Fill color for "E" based on position E
  if (c > 520 && c <= 550) {
    fill("#877100"); // Darkest yellow for "E"
  } else if (c > 100 && c <= 240) {
    fill("#ffdf41") // Light yellow for "E"
  } else if (c > 240 && c <= 380) {
    fill("#f8cf00"); // Yellow for "E"
  } else if (c > 380 && c <= 520) {
    fill("#bf9f00"); // Dark yellow for "E"
  }
  text("E", c, y, z); // Make latter "E" with position C
  
  // Move the letters from left to right
  if (goLeft === false) {
    x = x + 20;
    a = a + 20;
    b = b + 20;
    c = c + 20;
  } else {
    x = x - 20;
    a = a - 20;
    b = b - 20;
    c = c - 20;
  }
  
  // Bounce when the letters hit the screen edges
  if (x > 600 || a > 600 || b > 600 || c > 600) {
    goLeft = true;
  }
  
  if (x < 0 || a < 0 || b < 0 || c < 0) {
    goLeft = false;
  }
}
