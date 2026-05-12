#What is Hoisting ?

Hoisting is a mechanism in which function declaration  or variable declartion is move to the top during the memory creation.

Ex :

console.log(a);

var a = 10;

// Output: undefined

#what is Closure 

A closure is created when an inner function remembers variables from its outer function even after the outer function has finished execution.

function outer() {
  let count = 0;

  return function inner() {
    count++;
    console.log(count);
  };
}

const counter = outer();

counter();
counter();

#Use Cases
    Data hiding
    Private variables
    Memoization
    Callbacks

#What is Scoping 

Scope determines where variables can be accessed in the code.

Types : 

Global Scope
Function Scope
Block Scope
Lexical Scope


Global Scope : The Variable can be accessed in the whole program.

Ex: 

let name = "Adarsh";

function greet() {
  console.log(name);
}

greet();

Function Scope : The Variable can be accessed only with in the Function code.

function test() {
  let age = 24;
  console.log(age); // 24
}



Block Scope : The Variable can be accessed only with in the particular Block code.

{
  let city = "Delhi";
  console.log(city); // city
}

Lexical Scope : Lexical scope means inner functions can access variables from their parent functions.

Ex: 

function outer() {
  let username = "Adarsh";

  function inner() {
    console.log(username);
  }

  inner();
}

outer();
