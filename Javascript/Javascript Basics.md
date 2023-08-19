**Strongly Typed vs Weekly Typed Language** :
JS-> W
Java-> S

**Statically Typed And Dynamically Typed Languages** :
static -> type is checked at compile time

String a="Test";
a=10 ; //Compiler will stops at this line or give error

dynamic-> type is checked at runtime JS, Python, Ruby, Php

var a ="test";
((String) a).toUppercase();//<-this will work fine
a=10;
((String) a).toUppercase();//<-this will crash at runtime

Which language does not have data types?
Js variables does not have data types
Js values have data types


JS boxed datatypes : boxed datatype is a primitive value that is wrapped in an object.

For example, the `toUpperCase()` method is only available to objects. If you want to call the `toUpperCase()` method on a primitive value, you need to first wrap it in an object.

const str = "hello"; const upperStr = new String(str).toUpperCase(); console.log(upperStr); // HELLO

Primitive data types in JavaScript that can be boxed :
- string
- number
- boolean
- null
- undefined

Boxed data types are useful for a variety of purposes, such as:

- Calling methods and properties that are only available to objects.
- Storing primitive values in collections, such as arrays and objects.
- Passing primitive values as arguments to functions that expect objects

There are two different types of equality comparisons: equality and sameness :
`==` : lossely equal
`===` : strictly equal 

console.log(1 `==`  '1') //true
console.log(1 `=== '1')//false
console.log(' ' `==` 0)// true -> string gets converted into string 
0 does not get converted into string

console.log((0).toString())//0 -> it is returning 0 only

console.log(Number(''))// this will give us 0

//complex object

l value and r value:
let arr1=[1,2,3]
let arr2=[1,2,3]
console.log(arr1 `===` arr2)//false because l value is not same 
console.log(arr1`==`  arr1)//false because in both the places l-value should be same

primitive : we directly check the r value
i=[1]
j=[2]
k=i -> [] new box is created first and value of i->[1] to that box and then that box is assigned to k.
k=i creates a copy of i value

non-primitive : we first check l value and the check r value

a=[1,2,3]
b=[1,2,3]

c=a here will get the address of a

**Pass by value or pass by reference** :
let a=10
function change(b){
	b=2
}
change(a)
Console.log(a) -> 10  //proof for pass by value

let x=[1,2,3]
fun changeArr(y){ //y is pointer to array x, it has the address of x j
	y.push(4)    //value is pass to the address of x and added to t 
}
changeArr(x)
console.log(x) ->[1,2,3,4] //proof for pass by value

when its primitive r - value i p


**let-const-var** :
let a=10
console.log(a) -> 10
a=20
console.log(a) -> 20 // we can reassign value of a

var b= 20
both let and are similar
const=30 // we cannot reassign value of c here as it is a const
if we try to reassign a value to a const variable we will get error :
Assignment to a constant variable.

**Hoisting**
console.log(x)
console.log(y)
var x=10  //hoisting
let y=20 //will get an error y is not defined

we minimize the use of `var` as it will be difficult to read the value of var at runtime.

let x=20
console.log(x)

function changes(){
    console.log(x)
    var x=30
    console.log(x)
}

changes()

//Output :
20
undefined
30



 



