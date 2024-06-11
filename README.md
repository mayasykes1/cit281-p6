# CIT281 Project 6

## Learning Objectives
<li>Gain experience creating and working classes with inheritance</li>
<li>Gain more experience creating and working with classes</li>
<li>Gain more experience debugging code</li>
<li>Gain more experience using a generic block of code to process data</li>
<li>Gain more experience interpreting functional descriptions and specifications to complete an assignment</li>
<li>Gain more experience writing and executing non-web server Node.js JavaScript code using VSCode</li>
<li>Practice using modern JavaScript syntax</li>
<li>Gain more experience working with static data</li>

## Code:
//Pt.4 Shape Class
class Shape {
    constructor(sides) {
        this.sides = sides;
    }
    perimeter = () => this.sides.length ? this.sides.reduce((acc,side) => acc, side ,0) : 0;
}

/*
console.log(new Shape([5, 10]).perimeter());  // 15
console.log(new Shape([1, 2, 3, 4, 5]).perimeter()); // 15
console.log(new Shape().perimeter()); // 0
*/
<br></br>
//Pt.5: Rectangle Class
class Rectangle extends Shape {
    constructor(length = 0, width = 0) {
        super([length, width, length, width]);
        this.length = length;
        this.width = width;
    }
    area = () => this.length * this.width;
}

/*
console.log(new Rectangle(4, 4).perimeter());  // 16
console.log(new Rectangle(4, 4).area());  // 16
console.log(new Rectangle(5, 5).perimeter()); // 20
console.log(new Rectangle(5, 5).area()); // 25
console.log(new Rectangle().perimeter()); // 0
console.log(new Rectangle().area()); // 0
*/
<br></br>
//Pt. 5: Triangle Class
class Triangle extends Shape {
    constructor(sideA = 0, sideB = 0, sideC =0) {
        super([sideA, sideB, sideC]);
        this.sideA = sideA;
        this.sideB = sideB;
        this.sideC = sideC;
    }
    area = () => {
        const side = this.perimeter() / 2;
        return Math.sqrt(side - this.sideA) * (side - this.sideB) * (side - this.sideC);
    }
}

/*
console.log(new Triangle(3, 4, 5).perimeter());  // 12
console.log(new Triangle(3, 4, 5).area());  // 6
console.log(new Triangle().perimeter()); // 0
console.log(new Triangle().area()); // 0
*/
<br></br>
//Pt. 6: Processing Array of Sides Arrays
const data = [ [3, 4], [5, 5], [3, 4, 5], [10], [] ];

for (const side of data) {
    let shape;
}
