<h1>Why javascript</h1>
<p>Javascript improve user experience of the web page by converting it from a static page into an interactive one. OR javascript adds behaviours to the web page</p>
<b>JavaScript is a dynamically typed language</b>
<pre>
It means that JS does not require the explicit declaration of the variables before they're used. Just like python.

We can use typeof() to check the types, just like type() function in python.
</pre>

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

<h1>Expressions and Operators</h1>
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

<h1>Control Statement & Loop</h1>
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

<h1>Functions</h1>
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
<h1>ECMAScript</h1>
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









