<h1>COURSE CONTENT</h1>

[<h2>1. Course Description</h2>](#one)

[<h2>2. Variables & Datatypes(primitive & non-primitive) & Type Casting</h2>](#two)

[<h2>3. Expressions and Operators</h2>](#three)

[<h2>4.Control Statement & Loop</h2>](#five)

[<h2>5. Functions </h2>](#six)


<h1>Modern Javascript</h1>

[<h2>6. ECMAScript</h2>](#seven)

<li>Introduction of ECMS Script</li>

<li>ECMS SCript 2015()</li>

<li>ECMS SCript 2016()</li>

<li>ECMS SCript 2017()</li>

<li>ECMS SCript 2018()</li>

<li>ECMS SCript 2019()</li>

<li>ECMS SCript 2020()</li>

[<h2>7. Math Function  </h2>](#eight)

[<h2>8. DOM </h2>](#nine)

[<h2>9. BOM </h2>](#ten)

[<h2>10. Window Object </h2>](#eleven)

[<h2>11. Event Listener & Onclick </h2>](#twelve)

<h1>Advance Javascript</h1>

[<h2>12. Promise </h2>](#thirteen)

[<h2>13. Async / Await </h2>](#fourteen)


-----------------------------------------------------------------------------------------------------------------------
<a name="one"><h1>1.1 Course Description</h1></a><br>
<h3>Why javascript</h3>
<p>Javascript improve user experience of the web page by converting it from a static page into an interactive one. OR javascript adds behaviours to the web page</p>
<b>JavaScript is a dynamically typed language</b>
<pre>
It means that JS does not require the explicit declaration of the variables before they're used. Just like python.

We can use typeof() to check the types, just like type() function in python.
</pre>

<a name="two"><h1>2. Variables & Datatypes</h1></a><br>
<h1>Variables</h1>
<pre>
Naming variables: rules and best practices:
1)must start with (letter),(_),($). Can't use (number) as first character.
2)no limit of the length of the variable.
3)can't use reserved words as variable name.
</pre>

<h1>Data types</h1>
<pre>
6 data types are primitives
1)undefined
2)Boolean
3)Number
4)String
5)BigInt
6)Symbol

non-primitives(array etc)
</pre>

<h1>Type casting</h1>
<pre>
1) (+) : end result string
1+'fareen' = '1fareen'
2) (-) : end result number
1-'fareen' = NaN
1-'1' = 0

This will always be false:
0, "", undefined, null, NaN 
</pre>

<h3>Null VS Undefined(interview)</h3>
<pre>
Null is when the values is nothing
Undefined is when we did'nt defined it
var x=null;		//meaning x is nothing
var x;			//did'nt defined it
</pre>

<h3>NaN(Interview)</h3>
<pre>
NaN is not a number, returns a boolean value
isNaN is useful in user form when we check the user entered value is number or not
as in user form:
var phone = 'abc';
if(isNaN(phone)){
	valid number;
}
</pre>

<h3>= VS == VS ===</h3>
<pre>
= in JavaScript is used for assigning values to a variable. 

== in JavaScript is used for comparing two variables, but it ignores the datatype of variable. 

=== is used for comparing two variables, but this operator also checks datatype and compares two values. === called as strict equality comparison operator.

a=10;
b='10';

a==b; 		//true(ignore the type)
a===b; 	//false(check the type also)
</pre>

<a name="three"><h1>3. Expressions and Operators</h1></a><br>

<h1></h1>
<pre>
1)Assignment:
2)Arithmetic
3)Comparison
4)Logical
5)String
6)Conditional(ternary)

Syntax: var_name = (condition) ? value1:value2
Example: 
var age=18;
(age >= 18) ? "u can vote" : "u cant vote";

------------------------------------------------------------------
Increment(x++, ++x) and Decrement(x--, --x) operator

prefix operator means the variable is incremented first and then the expression is evaluated using the new value of the variable.
Example:
var num = 15;
var newNum = ++num;
console.log(num);
console.log(newNum);

O/P:
16
16

postfix operator means the variable is incremented later first the expression is evaluated using the new value of the variable.
Example:
var num = 15;
var newNum = num++;
console.log(num);
console.log(newNum);

O/p:
16
15
</pre>

<a name="four"><h1>4. Control Statement & Loop</h1></a><br>
<pre>
1)If..Else, If..Else if..ELse
2)Switch Statemet
3)While Loop
4)Do-While Loop
5)For Loop
6)For in Loop
7)For of Loop
8)forEach
9)Conditiona(ternary) operator


2)<b>Switch stmt: WAP to check the week in numbers</b>
var week='sunday';
switch(week){
	case 'monday':
		console.log('1');
	break;
	case 'tuesday':
		console.log('2');
	break;
	case 'wednesday':
		console.log('3');
	break;
	case 'thursday':
		console.log('4');
	break;
	case 'friday':
		console.log('5');
	break;
	case 'saturday':
		console.log('6');
	break;
	case 'sunday':
		console.log('7');
	break;
	default:
		console.log('invalid week')
}

3)<b>While VS Do-While</b>
While(jab tak true hai run karte jao, jaisehe false aaya stop karo):
Example:

var num=0;
while(num <= 10){
	console.log(num);
	num=num++;
}

Here if the condition if false meaning if var num=11 then we'll get no output
to atleast run it once if the condition is false in tht case we use do while
it run once if the condn is false

Do-While()

var num=11;
do{
	console.log(num);
	num++;
}while(num <= 10);

Unlike while here we don't get blank output cuz loop will run atleast once.

4)<b>for loop</b>
syntax:
	fro(initializer; condition; iteration)
	{
		//code
	}

Example:
for(var i=0; i<=10; i++){
	console.log(i)
}

--------------------------------------------------------------------
6)For in Loop(in ECMA 2015) : used to iterate the index
this is kind of like python for loop:

var ele = [1,2,'fareen',false]
for(let i in ele){
	console.log(i);
}

---------------------------------------------------------------------	

7)For of Loop(in ECMA 2015) : used to iterate the values
var ele = [1,2,'fareen',false]
for(let i of ele){
	console.log(i);
}

--------------------------------------------------------------------
8)forEach

i) we cannot use break in this forEach.
ii) cannot use this when working with forEach.

var ele = [1,2,'fareen',false]
ele.forEach(function(element, index, array){
	console.log(`${element} has index ${index} from which array it belongs to ${array}`)
});

array=tells us on which array we're working on

same using fat arrow function:

var ele = [1,2,'fareen',false]
ele.forEach((element, index, array) => {
	console.log(`${element} has index ${index} from which array it belongs to ${array}`)
});
</pre>

<a name="five"><h1>5. Functions</h1></a><br>
<pre>

Anonymouse Function: a function with no name
var sum = function(a,b){
	return total=a+b;
}

console.log(sum(10,20));


<b>Function parameter VS function argument(interview)</b>
function sum(a.b)		//(a,b) is called parameter
{
	var total=a+b;
	console.log(total);
}

sum(10,20)		//(10,20) is called argument

</pre>

-----------------------------------------------------------------

<h1>Modern Javascript</h1>

<a name="six"><h1>6. ECMAScript</h1></a><br>
<pre>
Javascript was first introduced in 1996
then in 1997: 2 ECMA internationa came
2015: 3 ES6 (which made javascript very easy)
2016: ES7
2017: ES8 also called ECMA Script 2017
2018: ES9
2019: ES10
2020: ES11


ECMA Script 2015 brings:
LET & CONST
TEMPLATE STRING
DEFAULT ARGUMENT
REST OPERATORS
DESTRUCTURING
OBJECT PROPERTIES
ARROW FUNCTION
SPREAD OPERTAOR

-------------------------------------------------------------------
LET VS CONST VS VAR(Interview)

var = function scope
let = block scope
const = use for constant value, value cannot be modified once declare usng const.

Using var: it has function scope it overwite the data and changed it to

function simpleData(){
	var myName = 'fareen';
	console.log(myName);
	
	if(true){		//anothe block
		var myName = 'annu';
		console.log(myName);
	}
	//outside if block	
	console.log(myName);
}

simpleData();

O/p: 
fareen
annu
annu

Using let: here myName has block scope that is why it still print fareen on last console.

function simpleData(){
	let myName = 'fareen';
	console.log(myName);
	
	if(true){		//anothe block
		let myName = 'annu';
		console.log(myName);
	}
	//outside if block	
	console.log(myName);
}


simpleData();

O/p:
fareen 
annu
fareen
--------------------------------------------------------------------
TEMPLATE STRING

this is same as f string in python
to print multiple data we need to use + operator again and again
so better we'll template string which uses ``

Example:
var myName='fareen'
var myAge=24
var mySibling=2

console.log('My name is:'+ myName + 'age is:' + myAge + 'no. of siblings i have' + mySibling)

//Better way(template string)
console.log(`My name is: ${myName} age is ${myAge} no. of siblings i have ${mySibling}`)

-----------------------------------------------------------------------------
DEFAULT ARGUMENT

function mult(a,b=5){
	return a*b;
}

console.log(mult(5));

if we give something like this function mult(a=5,b)
so in python above stmt will give default argument follows non default or somethig like this
but here we'll get NaN cuz a=5 already defined and againg we pass 5 for a value by default it starts giving value from first paramater so default argument should be at last.

------------------------------------------------------------------------
FAT ARROW FUNCTION
=>(is called as fat arrow)

It works when:
const sum = () => {
	let a=5, b=5;
	return `addition is ${a+b}`;
}
console.log(sum())

It works when:
const sum = () => {
	return `addition is ${(a=5)+(b=5)}`;
}
console.log(sum())

It works when:
const sum = () => `addition is ${(a=5)+(b=5)}`;
console.log(sum())
</pre>

<h1>Non-primitive data type(Array)</h1>
<pre>
Array and its function
</pre>

<h1>map, filter, reduce</h1>
<pre>
map: 
1)does'nt touch the existing function instead it creates new array.
2)ability to chain other methods:
Example after using map we can use reduce and filter and other methods with it
Example:
var n = [1,2,3,4,5];
var num = n.map(n => n * 2).filter(
	num => num % 3==0
	)
</pre>

<h1>Date</h1>
<pre>
4 methods to create date:
new Date()
Example:
let x=new Date()
----------------------------------------------

new Date(year, month, day, hours, minutes, seconds, milliseconds)
Example: let y=new Date(2021, 1, 07)
here i)if there is year there month argument is must else it'll print 1/1/1970 

------------------------------------------------

new Date(milliseconds)
Example:
let y=new Date(2021, 1, 07)

will return the date time, takes parameter in milliseconds
--------------------------------------------------

new Date(date string)


Date & Time Methods:

</pre>

<a name="seven"><h1>7. Math Function</h1></a><br>
<pre>
1)Math.PI: returns the pi value

2)Math.abc : return absolute value (basically converts negative value into positive).

3)Math.ceil: consides the ceil value if the value is 5.01 then it'll return 6
Example: will always increment with 1 if decimal comes.
Math.ceil(5.01) -> 6

4)Math.floor: return floor value
Example: gives the same value before dot
Math.floor(5.9) -> 5

5)Math.round: return round value
Math.round(5.5) -> 6

6)Math.min()
Math.min(2,36,1,6,30) ->1

7)Math.max()

8)Math.random: return random number which always starts with 0.some value
Math.random() -> 0.7397596168978735

9)Math.random()*10: to make it return integer value, can return value from 0.some value or integernumber.somevalue
Math.random()*10 ->  9.6397596168978735

10)To make it only return integer value:
Math.floor(Math.random()*10) : return random number between 0 & 9

11)Math.trunc : returns the integer part of a number
Math.trunc(4.6) -> 4
Math.trunc(-99.6)  -> -99
</pre>

<a name="eight"><h1>8. DOM</h1></a><br>
<pre>
<b>Difference between Window and Document</b>
The tabs and bookmarks and those other section including our website is Window
and only our website is Document(excluding those tabs, bookmark section etc).

So document is part of windows and document is only used to work with html tags.

For working with html elements we use document, rest for all other stuff history, navigation etc we'll use BOM

Html is the root of document(entire DOM is created using html)
we can check that using document.documentElement
and then comes body etc -> see diagram.
</pre>

DIagram:

<a name="nine"><h1>9. BOM</h1></a><br>
<pre>
alert, confirm, prompt
This are not part of DOM but part of Browser that is why it is BOM
</pre>

<a name="ten"><h1>10. Windows Object</h1></a><br>
<pre>
Document is part of windows object
and by default everything is a part of windows so we dont ned to write windows. as in
innerHeight and window.innerHeight both will return the same output 
here windows is optional cuz everything is part of windows by deafult.

</pre>


<h1>querySelector</h1>
<pre>
we can change css style using the querySelector(to select class or id and then change color etc) 

Example:
document.querySelector('#myclass')
x.style.color = "red";
</pre>

<h1>Array Destructuring(ECMA 2015)</h1>
<pre>
let arr = ['fareen','ansari',24]

old way:
myFirstName = arr[0];
myLastName = arr[1];
myAge = arr[2];

using destructuring:
let [myFirstName, myLastName, myAge] = arr;
console.log(myAge); 		//24

adding data using array destructuring
let [myFirstName, myLastName, myAge, myDegree='MCA'] = arr;

</pre>

<h1>Object Destructuring</h1>
<pre>
const myData = {
	myFirstName : 'Fareen',
	myLastName : 'Ansari',
	myAge : 23
};

old way:
let myFirstName = myData.myFirstName;
let myLastName = myData.myLastName;
let myAge = myData.myAge;
console.log(myAge);

using destructuring:
let {myFirstName, myLastName, myAge, myDegree='MCA'} = myData;
console.log(myAge);
console.log(myDegree);
</pre>

<h1>Object Properties</h1>
<pre>
1) using [] for dynamic data
This is same like dynamic data we passing in angular so that is javascript ES6 property.

i) we can perform addition and pass dynamic values inside it:

let myName = 'fareen';
const myData = {
	[myName] : "Hello!!",
	[20+20] : "is my age"
}
console.log(myData);

2)if key and value are same then we can write like this, no need to write seperate key.
let myName = "fareen"
let myAge = 24
const myData = {
	myName,
	myAge
}
console.log(myData);

O/p:
{myName: 'fareen', myAge: 24}
</pre>

<h1>Spread Operator</h1>
<pre>
If in case we need entire array we can use spread operator:
let color = ['red','pink','blue'];
let newcolor = [...color, 'white','yellow'];
console.log(newcolor);

O/p:
['red', 'pink', 'blue', 'white', 'yellow']
</pre>

<h1>ECMAScript 2016/ES7</h1>
<pre>
1)Array.prototype.includes
2)Exponential Operator


1)Array.prototype.includes
To find the particular data is present or not we can use array include
let color = ['red','pink','blue'];
const isPresent = color.includes('pink');
O/p:
true

const isPresent = color.includes('cyan');
O/p:
false

------------------------------------------------------------------------
2)Exponential Operator(**)/power
2**3
meaning 2 power 3, 2x2x2 = 8
</pre>

<h1>ECMAScript 2017/ES8</h1>
<pre>
1)String padding: to give padding to string
let myName = "Fareen".padStart(7);	//Fareen contains 6 chars so 6+1 space, so we'll get 1 space in start

let myName = "Fareen".padEnd(7);
o/p:
' Fareen'

--------------------------------------------------------------------
2)Object.entries(): convert each object in seperate array.
const person = {
	name:'fareen',
	age:23
}

console.log(Object.entries(person));

o/p:
['name', 'fareen']
['age', 23]

</pre>

<h1>ECMAScript 2018</h1>
<pre>
Introduced spread operator for objects as well

const person = {
	name: 'fareen',
	age:24
}

const addData = { ...person, degree : 'MCA'}
console.log(addData);
o/p: {name: 'fareen', age: 24, degree: 'MCA'}
</pre>

<h1>ECMAScript 2019</h1>
<pre>
flat array:
const arr = ['1','2','3',['4','5'],'6',['7','8','9']];
console.log(arr.flat());

for 2 level:
console.log(arr.flat(2));

for 3 level:
console.log(arr.flat(3));

for infinity
console.log(arr.flat(Infinity));

o/p:
['1','2','3','4','5','6','7','8','9'];

----------------------------------------------------------------
flatMap
----------------------------------------------------------------
Object.fromEntries()

const person = {name: 'fareen', age:24};
const arrObj = Object.entries(person);
console.log(arrObj);
o/p:
[['name','fareen'],['age',24]];

To convert the array back to object
console.log(Object.fromEntries(arrObj));
o/p: {name: 'fareen', age: 24}
-----------------------------------------------------------------
Object.prototype.{trimStart, trimEnd}: to remove space.

------------------------------------------------------------------
Symbol.prototype.description
------------------------------------------------------------------
JSON.stringify()
-------------------------------------------------------------------
Function.prototype.toString()
</pre>

<h1>ECMAScript 2020</h1>
<pre>
1)BigInt:

let oldNum = Number.MAX_SAFE_INTEGER;
console.log(oldNum + 20);

This 9007199254740991 is javascript safenumber after this javascript cannot handle more number and start giving wrong o/p.

add n:
const newNum = 9007199254740991n + 12n;
console.log(newNum);
console.log(typeof(newNum));

o/p:
9007199254741003n
bigint
</pre>

<h1>ECMAScript 2014</h1>
<pre>
Use strict:

without use strict:
x=3.14
console.log(x)		//3.14

with use strict:
"use strict";
x=3.14
console.log(x)		//error x is not defined

solving the error:
let x=3.14;
</pre>

<h1>Advance Javascript</h1>
<pre>
1)Event Propagation: this mode determines in which order the elements receive the event.

<b>Bubbling & Capturing phase</b>
Bubbling phase: from child to parent 
Capturing phase: parent to child(parent listner and then child listner called), it is also called trickling.

To stop bubbling we can use 
event.stopPropagation();

To start capturing we can use 3rd parameter of event listner which is basically boolean value.

<pre>
<!DOCTYPE html>
<html>
<body>

    <div id="parent" style="width:800px; height:500px; background-color:cyan; padding:100px;">
            
        <div id="child" style="width:400px; height:400px; background-color:green;">
            
        </div>
    </div>

    <script>
        const parentId = document.getElementById('parent');
        const childid = document.getElementById('child');

        const parentCall = () => {
            alert('parent div is called');
        }

        const childCall = () => {
            alert('child div is called');
            // event.stopPropagation();
        }

        parentId.addEventListener('click',parentCall,true);
        childid.addEventListener('click',childCall,true);       
    </script>
</body>
</html>
</pre>

-------------------------------------------------------------------------
2)Higher Order Function/Callback Function:

Higher order function: function which taks another function as an argument is called as higher order function.

Callback function: function which get passed as an argument to another function is called as callback function.


//callback function all 3
const add = (a,b) => {
	return a+b;
}
const sub = (a,b) => {
	return a-b;
}
const mult = (a,b) => {
	return a*b;
}

const calculator = (num1, num2, operator) => {
	return operator(num1, num2);
}

//higher order function
console.log(calculator(5,2,sub));

</pre>

<h1>Asyncgronour Javascript</h1>
<pre>
1)Hoisting in js
Hoisting moves the variable defined to the top as in:

console.log(myName);
var myName;
myName="Fareen"

o/p:
undefined

Bcoz of hoisting it moves the myName at the top at run time and return the output as undefined.
In ES2015 This can be avoided by using the let keyword instead of var.

console.log(myName);
let myName;
myName="Fareen"

o/p: error
------------------------------------------------------------------
2)Scope chain & Lexical Scoping

Scope chain: is used to resolve the value of the variable name in js
Example:
var PI = 3.14

//by seeing the PI variable we can say its value.

Lexical scoping:
inner function can access the parent function but vice versa is not true.
-------------------------------------------------------------------
3)Closures in js

inner function can access data of outer/parent function with the help of closure.
cuz it gets stored in closure.
-------------------------------------------------------------------
4)use strict: seen alresy
-------------------------------------------------------------------
5)Synchronouse and Asynchronouse js
Synchronouse:
agar mere paas 2 kaam h. mera ek kaam finish hone k baad he me dustra kaam karungi.
1 work: takes 10mins
2 work: taks 5 sec
even 2nd work 5 sec le rha h fir bhi me pehle first finish karungi
and that is Synchronouse js

Example:
const fun2 = () =>{
	console.log("Function 2 is called.");
}

const fun1 = () =>{
	console.log("Function 1 is called.");
	fun2();
	console.log("Function 2 is called again.")
}
fun1();
	
Asynchronouse:
1 work: takes 10mins
2 work: taks 5 sec
Yaha work one by one hote he rahege, that means 2nd work ho ke finish ho jayega and 1 work bhi chalta rahega. so we dont have to wait. 
like in youtube we play video comment and like these works are hapenning together with the help of Asynchronouse.

Example:
const fun2 = () =>{
	setTimeout(() =>{
		console.log("Function 2 is called");
	}, 5000);
}

const fun1 = () =>{
	console.log("Function 1 is called.");
	fun2();
	console.log("Function 2 is called again.")
}
fun1();

o/p:
Function 1 is called.
Function 2 is called again.
Function 2 is called

Here setTimeout is ascynchronous function so it does'nt wait 5 sec and come back in fun1 to run that other console.

-------------------------------------------------------------------
6)Event loop in js

In js every function get its own execution context.

Example:
const fun2 = () =>{
	setTimeout(() =>{
		console.log("Function 2 is called");
	}, 5000);
}

const fun1 = () =>{
	console.log("Function 1 is called.");
	fun2();
	console.log("Function 2 is called again.")
}
fun1();

In the above program fun1 get its own execution context
and console.log get its own execution context, and it runs and its execution context destroyed

setTimeout is a Web API function so when it sees asynchronous function it gets sent to Web API -> from Web API to Message queue
And event will loop back all the function waiting to msg queue to Global Execution Context -> and then it also runs and stop 

To understand it see javascript video at 13:00:00

------------------------------------------------------------------
7)Function Currying:
When a function is calling the other function in other parameter
as in: sum(8)(3)(4);

Example:
function sum(num1){
	return function(num2){
		return function(num3){
			console.log(num1+num2+num3);
		}
	}
}
sum(8)(3)(4);

Rewriting using fat arrow:

const sum = (num1) => (num2) => (num3) => console.log(num1+num2+num3);
sum(8)(3)(4);
</pre>

Diagram:

<h3>Difference between json and javascript object</h3>
<pre>
in json for key we use double quotes and in js object we don't use double quotes

Example:
json = {"name":"fareen"}
object = {name:"fareen"}

<b>To convert js object into json</b>
var my_obj = {name: "fareen", age: 23};
var my_json = JSON.stringify(my_obj);
typeof(my_json);		//string(cuz json store data in string).

<b>To do vice versa</b>
var my_obj2 = JSON.parse(my_json);
typeof(my_obj2);	//object
</pre>

<a name="eleven"><h1>11. Event Listener and Onclick</h1></a><br>


<a name="twelve"><h1>12. Promises</h1></a><br>
<pre>
It returns yes or no(fullfill, reject)
Either API ks data milega ya to nhi milega 
90% of time we consume promise.
fetch() always returns promise.
To save us from callback hell we use promise.
</pre>

<a name="thirteen"><h1>13. Async / Await</h1></a><br>
<pre>


using async for fat function 
            const generateJokes = async () => 

with normal function
            async function generateJokes() 
</pre>

