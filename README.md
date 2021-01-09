//Main sketch

var ship;

function setup() {
  createCanvas(400, 400);
  ship = createVector(200,200);
}

function keyPressed() {
  if (keyCode === LEFT_ARROW) {
    ship.Leftupdate();
  }
}

function draw() {
  noStroke();
  background(51);
  rect(ship.x, ship.y, 50, 50);
}

//ship.js

function Ship(x,y) {
    this.pos = createVector(x,y);
    this.vel = createVector(0, 1);
    this.Leftupdate = function() {
        this.pos.add(this.vel);
    }
}
