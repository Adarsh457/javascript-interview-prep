#what is javascript ?

javascript is a single threaded scripting language, Which is use to create dynamic web pages.

#Difference Between Var, let and Const

var -> 1. can be redeclared and reassign
       2. Function Scoped.
       3. Supports Hoisting.

Ex:   
    var a = 10;
    var a = 20;

    console.log(a); // 20

Let -> 1. can be redeclared  But Cannot be  reassign.
       2. Blocked Scoped.
       3. Temporal Dead Zone.

Ex:
        let age = 24;
        age = 25;

        console.log(age); // 25

Const -> 1. Cannot be redeclared and reassign.
         2. Blocked Scoped.
         3. Temporal Dead Zone.

Ex:
        const PI = 3.14;

        // PI = 4; ❌ Error


#Data Types in JS.

Js has two categories. 

Primitive Data Types.

String
Boolean
Number
Null
Undefined
Symbol
BigInt

Non - Primitive Data Types

Object
Array
Function

#Difference Between `==` and `===`

Loosely Equal(==) -> Compares the values on both the side.

Ex: console.log(5 == "5"); // true

Strictly Equal(===) -> Compares both the Values and Data Types on both the side.

Ex: console.log(5 === "5"); // false

#What is Type Coercion?

Type coercion is JavaScript's automatic conversion of one data type into another during operations.

Ex: 

console.log("5" + 2); // "52"


#Difference Between null and undefined

undefined -> means a variable has been declared but no value has been assigned.

Ex: 

let name;

console.log(name); // undefined

null -> represents an intentional empty value.

Ex: 

let user = null;

console.log(user); // null

#What is NaN?

NaN stands for "Not a Number".

It occurs when a mathematical operation fails to produce a valid number.

Ex:

console.log("hello" / 2); // NaN
