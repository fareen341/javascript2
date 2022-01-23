<h1>COURSE CONTENT</h1>

[<h2>1. Course Description</h2>](#one)

[<h2>2. Variables & Datatypes(primitive & non-primitive) & Type Casting</h2>](#two)

[<h2>3. Expressions and Operators</h2>](#three)

[<h2>4.Control Statement & Loop</h2>](#four)

[<h2>5. Functions </h2>](#five)


<h1>Modern Javascript</h1>

[<h2>6. ECMAScript</h2>](#six)

<li>Introduction of ECMS Script</li>

<li>ECMS Script 2015(ES6)</li>

<li>ECMS Script 2016()</li>

<li>ECMS Script 2017()</li>

<li>ECMS Script 2018()</li>

<li>ECMS Script 2019()</li>

<li>ECMS Script 2020()</li>

[<h2>7. Math Function  </h2>](#seven)

[<h2>8. DOM </h2>](#eight)

[<h2>9. BOM </h2>](#nine)

[<h2>10. Window Object </h2>](#ten)

[<h2>11. Event Listener & Onclick </h2>](#eleven)

<h1>Advance Javascript</h1>

[<h2>12. Promise </h2>](#twelve)

[<h2>13. Async / Await </h2>](#thirteen)

[<h2>14. Events </h2>](#fourteen)

<li>setTimeout</li>

<li>setInterval</li>

[<h2>15. Storage </h2>](#fifteen)

<li>Cookie</li>

<li>Local Storage</li>

<li>Session Storage</li>

[<h2>16. Class & Object </h2>](#sixteen)

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
<b>1)undefined</b>

<b>2)Boolean</b>
Except these(NaN, "", 0, '', undefined, null) all are true. These are called as falsy

To check the booloean value use Boolean function or NOT operator twice
var x=55;
y=Boolean(x);   //true
y=!!x;          //true

<b>3)Number</b>
Methods in NUMBER:

    document.write(Number.MIN_VALUE+"<br>")
    document.write(Number.MAX_VALUE+"<br>")
    document.write(Number.NEGATIVE_INFINITY+"<br>")
    document.write(Number.POSITIVE_INFINITY+"<br>")
    document.write(Number.prototype+"<br>")
    document.write(Number.MIN_SAFE_INTEGER+"<br>")
    document.write(Number.MAX_SAFE_INTEGER+"<br>")

  Output:
    5e-324
    1.7976931348623157e+308
    -Infinity
    Infinity
    0
    -9007199254740991
    9007199254740991
    
<b>4)String</b>
We can use single, double, or backtick(`) for writing string

RAW STRING:
This is same as in python 'r' string:
Example:
const filePath = `C:\Development\profile\navigation.html`; 

STRING METHODS:
        1)concat():
            A new string containing the combined text of the strings provided.
            Syntax:
            concat(str1)
            concat(str1, str2)
            concat(str1, str2, ... , strN)

            Example:
            str1="hello";
            str2="world";
            str1.concat(' ',str2);
            //hello world

        2)charAt():
            An integer between 0 and str.length - 1. If the index cannot be converted to the integer or no index is provided, the default is 0, so the first character of str is returned.
            syntax: charAt()
            Example:str1.charAt(1);     //e
            if nothing is given inside the charAt first character will returned.
            if wrong input given empty string will be returned eg. charAt(99)    //""

        3)charCodeAt():
            returns the character code eg. A has code 65 etc.
            Example:"Ansari".charCodeAt(0)      //65
	   
	4)endswith(), startwith():
            syntax:
            endsWith(searchString, length) 
            startsWith(searchString, position)

            Example:
            "fareen".endsWith('n',6);       //true
            "fareen".endsWith('n');         //true

            "fareen".startsWith('f',0);     //true

        5)includes()
            The includes() method performs a case-sensitive search to determine whether one string may be found within another string, returning true or false as appropriate.
            Syntax:includes(searchString, position)
            Example:
            'fareen ansari'.includes('Fareen')             //false (because it search is case sensitive).

        6)indexOf():
            this will serach for index from start i.e left.
            Syntax:indexOf(searchValue, fromIndex)
            Example:

        7)lastIndexOf():
            this will search for the index from right. like rfind in python.
            Syntax:lastIndexOf(searchValue, fromIndex)
            Example:
            str = 'To be, or not to be, that is the question.'.lastIndexOf('be')        //17

        8)localeCompare():
	9)match():
            The match() method retrieves the result of matching a string against a regular expression.This will return an array output.
            Syntax:match(regexp)
            Example:
            const paragraph = 'The quick brown fox jumps over the lazy dog. It barked.';
            const regex = /[A-Z]/g;
            const found = paragraph.match(regex);
            console.log(found);                             //Array ["T", "I"]

        10)matchAll():
            
        11)pasEnd():
            This will add space in the end of the string or some given chars if provoded , it counts from start of the charachter.The default is space.
            Synatx:
            padEnd(targetLength, padString)
            Example:
            const str1 = 'Breaded Mushrooms';           //the length of this str is 17, so 8 '-' will be added at the end.
            str1.padEnd(25,'-');                        //"Breaded Mushrooms--------" 
            str1.padEnd(25);                            //default is space.

        12)padStart()
            The padding is applied from the start of the current string.
            Synatx:padStart(targetLength, padString)
            Example:
            str1.padStart(25,'.')                       //"........Breaded Mushrooms"

        13)repeat()
            Repeats the string.
            Syntax:repeat(count)
            Example:
            'fareen '.repeat(3)                         //"fareen fareen fareen "
	   
	14)replace():
            This will only replace the first match from LTR.
            The replace() method returns a new string with some or all matches of a pattern replaced by a replacement. 
            The pattern can be a string or a RegExp, and the replacement can be a string or a function to be called for each match. If pattern is a string, only the first occurrence will be replaced.
            Synatx:
            replace(regexp, newSubstr)
            replace(regexp, replacerFunction)

            replace(substr, newSubstr)
            replace(substr, replacerFunction)
            Example:
            x="Hello fareen";
            x.replace("Hello","ansari");                //"ansari fareen"

            replace in regex:
            x="All the time he had, had Had no effect on his work";
            x.replace('/Had/i','have');                 //"All the time he have, had Had no effect on his work"

        15)replaceAll():
            Example:
            x.replaceAll('had','have');                 //"All the time he have, have Had no effect on his work"

        16)search():
            Returns the index.
            Syntax:
            search(regexp
            Example:
            x="All the time he have, have Had no effect on his work"
            x.search('the')                             //4

        17)slice():
            This will start from the start index and go till lastindex-1.
            Synatx:
            slice(beginIndex)
            slice(beginIndex, endIndex)
            Example:
            x="The quick brown fox jumps over the lazy dog."
            str.slice(4,5)                              //"q"
            Here it will start with 4 followed by 5-1=4 so 'q' will be printed.

            Example2:
            str.slice(4,6)                              //"qu"
	    
	18)substring():
            Synatx:
            substring(indexStart)
            substring(indexStart, indexEnd)
            Example:
            s="Hello world"     
            s.substr(3);                                //"lo world"
            s.substr(0,2);                              //"He"

        19)split():
            Same as split function in python, return an array.
            Synatx:
            split()
            split(separator)
            split(separator, limit)
            Example:
            str.split(' ',10);                          //["The", "quick", "brown", "fox", "jumps", "over", "the", "lazy", "dog."]

        20)toLowerCase(), toUpperCaes()
            Example:
            "Fareen".toLowerCase();                     //"fareen"
            "Fareen".toUpperCase();                     //"FAREEN"

        21)toString():
            Converts into string.
            Example:
            x=123;
            x.toString();                               //"123"

        22)trim():
            Trim the space on either sides.
            Syntax:
            trim()
            Example:
            const greeting = '   Hello world!   ';
            greeting.trim();                            //"Hello world!"
	    
	23)trimEnd(), trimStart():
            Example:
            greeting.trimEnd();                         // "   Hello world!"
            greeting.trimStart();                       //"Hello world!   "

<b>5)BigInt</b>
Covered in ECMA script section

<b>6)Symbol</b>
Pending

<b>NON_PRIMITVE DATA TYPE:</b>
<b>7)Array</b>
    Declaration:
        var arr=[1,"javascript",false,7.8];

    Accessing using index:
        arr[1]          //"javascrip"

    Changing the value of array:
        arr[1]="python";        
        arr;                    //[1,"python",false,7.8]

    To get the length:
        arr.length;             //4

    Using for loop in array:
        x=[1,2,3]
        for(var i of x){
            console.log(i);             
        }

        Output:
        1
        2
        3

ARRAY METHODS:
Array Methods:
        1)concat:
            Syntax:
                concat(value0, value1, ... , valueN)
            Example:
                a=[1,2,3],  b=[4,5],    c=[6]
                a.concat(b,c);                      //[1,2,3,4,5,6]

        2)copyWithin():
        The copyWithin() method shallow copies part of an array to another location in the same array and returns it without modifying its length.
            Synatx:
                copyWithin(target, start, end)

            Example:
                // copy to index 0 the element at index 3
                console.log(array1.copyWithin(0, 3, 4));                //["d", "b", "c", "d", "e"]

                // copy to index 1 all elements from index 3 to the end
                console.log(array1.copyWithin(1, 3));                   //["d", "d", "e", "d", "e"]

        3)entries():
        The entries() method returns a new Array Iterator object that contains the key/value pairs for each index in the array.
            Syntax:
                entries()
            Example:
                a=['a','b','c'];
                a.entries().next().value;       //[0,'a'] 
                a.entries().next().value;       //[1,'b']
	
	4)every():
        The every() method tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.
            Syntax:
                every((element) => { ... } )
                more syntax on doc.

            Example:
                var arr1=[10,20,30];
                var x = (val) => val<40;
                arr1.every(x)                        //true  (cuz every element is less then 40)

                OR
                arr1.every((val) => val<40)

        5)fill():
        The fill() method changes all elements in an array to a static value, from a start index (default 0) to an end index (default array.length). It returns the modified array.
            Syntax:
                fill(value)
                fill(value, start)
                fill(value, start, end)

            Example:
                arr1=[1,2,3,4,5];
                arr1.fill(0);                  //[0,0,0,0,0]        fill every element with 0.
                arr1.fill(0,2);                //[1,2,0,0,0]        fill with 0 start from 2  to end.
                arr1.fill(0,1,3);              //[1,0,0,4,5]        fill with 0 start from 1 to 3-1=2

        6)filter():
        The filter() method creates a new array with all elements that pass the test implemented by the provided function.
            Syntax:
                filter((element) => { ... } )
                more syntax on doc.
            Example:
                x=[1,2,3,4,5];
                x.filter(x=>x%2==0);            //[2,4]
	
	 7)find():
        The find() method returns the value of the first element in the provided array that satisfies the provided testing function. 
        If no values satisfy the testing function, undefined is returned.
            Syntax:
                find((element) => { ... } )
                more syntax on doc.
            Example:
                x=[1,2,3,4,5];
                x.find(val => val>3);           //[4] this will return only the next value where as filter will give [4,5].

        8)findIndex():
        The findIndex() method returns the index of the first element in the array that satisfies the provided testing function. 
        Otherwise, it returns -1, indicating that no element passed the test.
            Syntax:
                findIndex((element) => { ... } )
            Example:
                x=[1,2,3,4,5];
                x.findIndex(val => val>3);          //3,  bcoz 3 is at index of 3.
            
        9)flat():
        The flat() method creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.
            Syntax:
                flat()
                flat(depth)
            Example:
                arr1 = [0, 1, 2, [3, 4]];
                arr1.flat();                    //Array[0,1,2,3,4]
                
                arr2=[0,1,2,[3,[4,5,[6,7]]]]
                arr2.flat(1);                   //Array [0, 1, 2, 3, Array [4, 5, Array [6, 7]]]
                arr2.flat(2);                   //Array [0, 1, 2, 3, 4, 5, Array [6, 7]]

        10)flatMap():
        The flatMap() method returns a new array formed by applying a given callback function to each element of the array, and then flattening the result by one level. 
        It is identical to a map() followed by a flat() of depth 1, but slightly more efficient than calling those two methods separately.
            Syntax:
                flatMap((currentValue) => { ... } )
                more syntax on doc.
            Example:
                x=[1,2,3,4]
                x.flatMap(x => [x * 2]);            //[2, 4, 6, 8]

	 11)forEach():
        The forEach() method executes a provided function once for each array element.
        Syntax:
            forEach((element) => { ... } )
        Example:
            x=[1,2,3,4];
            x.forEach(element => console.log(element));
            
            Output:
            1
            2
            3
            4

        12)from():
        The Array.from() static method creates a new, shallow-copied Array instance from an array-like or iterable object.
            Syntax:
                Array.from(arrayLike, (element) => { ... } )
            Example:
                z=[1,2,3]
                Array.from(z, x => x + x);              //[2,4,9]

            
        13)includes():
        The includes() method determines whether an array includes a certain value among its entries, returning true or false as appropriate.
            Syntax:
                includes(searchElement)
                includes(searchElement, fromIndex)
            Example:
                x=['a','b','c'];
                x.includes('a')             //true
                x.includes('a',1)           //false , cuz we gave start index 1, there is no element 'a' start from index 1.

        14)indexOf():
        The indexOf() method returns the first index at which a given element can be found in the array, or -1 if it is not present.
            Syntax:
                indexOf(searchElement)
                indexOf(searchElement, fromIndex)
            Example:
                x=['a','b','c'];
                x.indexOf('c');         //2
                x.indexOf('d');         //-1
		
	15)isArray():
        The Array.isArray() method determines whether the passed value is an Array.
            Syntax:
                Array.isArray(value)
            Example:
                Array.isArray([1,2,3]);         //true
            
        
        16)join():
        The join() method creates and returns a new string by concatenating all of the elements in an array (or an array-like object), separated by commas or a specified separator string.
        If the array has only one item, then that item will be returned without using the separator.
            Syntax:
                join()
                join(separator)
            Example:
                x = ['Fire', 'Air', 'Water'];
                x.join()            //"Fire,Air,Water"
                x.join('-')         //"Fire-Air-Water"

        17)keys():
        The keys() method returns a new Array Iterator object that contains the keys for each index in the array.
            Syntax:
                keys()
            Example:
                x = ['Fire', 'Air', 'Water'];
                y=x.keys();
                for (const key of x.keys()) {
                    console.log(key);
                }                                          

                Output:
                0
                1
                2

	18)lastIndexOf():
        It start searching from right.
            Syntax:
                lastIndexOf(searchElement)
                lastIndexOf(searchElement, fromIndex)

            Example:
                var animals = ['Dodo', 'Tiger', 'Penguin', 'Dodo'];
                animals.lastIndexOf("Dodo");                            //3

        19)map():
            Syntax:
            The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.
                map((element) => { ... } )
                more syntax on doc.
            Example:
                var array1 = [1, 4, 9, 16];
                array1.map(x => x+2);               //[3, 6, 11, 18]

        20)pop(),push():
        The pop() method removes the last element from an array and returns that element. This method changes the length of the array.
        The push() method adds one or more elements to the end of an array and returns the new length of the array. 
            Syntax:
                pop()

                push(element0)
                push(element0, element1)
                push(element0, element1, ... , elementN)

            Example:
            pop() example:
                x=[2,45,6,54,56,3];
                x.pop();                    //3

            push() example:
                x=[2,45,6,54,56,3];
                x.push(3,4,5);                      //9     cuz it returns the last index.       
                op: x=[2, 45, 6, 54, 56, 3, 3, 4, 5]
		
	21)reduce():
        The reduce() method executes a reducer function (that you provide) on each element of the array, resulting in a single output value.
            Syntax:
                reduce((accumulator, currentValue) => { ... } )
                more syntax on doc.
            Example:
                x=[1,2,3,4];
                x.reduce((x,y) => x+y);         //10

        22)reverse():
        The reverse() method reverses an array in place. The first array element becomes the last, and the last array element becomes the first.
            Syntax:
                reverse()
            Example:
                x=[1,2,3]
                x.reverse()                 //[3,2,1]

        23)shift():
        The shift() method removes the first element from an array and returns that removed element. This method changes the length of the array.
            Syntax:
                shift()
            Example:
                x=[1,2,3];
                x.shift();          //1
                op: x=[2,3]

        24)slice():
        The slice() method returns a shallow copy of a portion of an array into a new array object selected from start to end (end not included) where start and 
        end represent the index of items in that array. The original array will not be modified.
            Syntax:
                slice()
                slice(start)
                slice(start, end)
            Example:
                x=['a','b','c','d','e'];
                x.slice(2);                 //['c','d','e']     slice start from 2 to end.
                x.slice(2,4);               //['c','d']         slice start from 2 to 4-1=3.
                x.slice(-2);                //['c','d']         slice start from -2 to end.
                x.slice(2,-1);              //['c','d']         slice start from 2 to -1-1=-2

	 25)some():
        The some() method tests whether at least one element in the array passes the test implemented by the provided function. It returns true if, in the array, 
        it finds an element for which the provided function returns true; otherwise it returns false. It doesn't modify the array.
            Synatx:
                some((element) => { ... } )
                more syntax on doc.
            Example:
                x=[1,3,4];
                x.some((val) => val%2==0);             //true cuz atleast one element which divides by 2. 
                y=[1,3];
                x.some((val) => val%2==0);             //false

        26)sort():
        sort in ascending.
            Syntax:
            Example:
                x=['b','a','b','t',' '];
                x.sort();                    //[" ", "a", "b", "b", "t"]

        27)splice()
        The splice() method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place. 
        To access part of an array without modifying it, see slice().
            Syntax:
                splice(start)
                splice(start, deleteCount)
                splice(start, deleteCount, item1)
                splice(start, deleteCount, item1, item2, itemN)
            Example:
                inserts at index 1, cuz deleteCount is 0, so no deletion.
                months = ['Jan', 'March', 'April', 'June'];
                months.splice(1, 0, 'Feb');                         //Array ["Jan", "Feb", "March", "April", "June"]
                
                // replaces 1 element at index 4.
                months.splice(4, 1, 'May');                         //Array ["Jan", "Feb", "March", "April", "May"]

<b>MAP, FILTER, REDUCT</b>
map: 
1)does'nt touch the existing function instead it creates new array.
2)ability to chain other methods:
Example after using map we can use reduce and filter and other methods with it
Example:
var n = [1,2,3,4,5];
var num = n.map(n => n * 2).filter(
	num => num % 3==0
	)

Map: Returns an array.
    var numbers= [1,2,3,4,5];
    var doubled  = numbers.map(n => n * 2);

    Output:
    [2, 4, 6, 8, 10]    
Filter: filter out the record, returns an array
    var n = [1,2,3,4,5];
    var even = numbers.filter(n => n % 2==0);

    Output:
    [2,4]
Reduce:
    var numbers = [1,2,3,4,5];
    var initialVal = 0;
    let result=numbers.reduce((x, y) => x + y ,initialVal);

    Output:
    15

<b>8)Objects</b>
Mixed Object:
    emp={
        e1:{name:"A",roll:1,marks:[10,20],addr:{loc:"malad",pin:9900}},
        e2:{name:"B",roll:2,marks:[10,20],addr:{loc:"virar",pin:800}}
    }	
    Here name=str, roll=number, marks=array, addr=object:
    
    Accessing array:
    emp.e2.marks[0]         //10

    Accessing object:
    emp.e2.addr.loc         //virar
    
Writing function inside the object:
        var x={
        fname:'fareen', 
        lname:'ansari',
        rno:1, 
        age:23,
        fullname:function(){
            return "Fullname:"+x.fname+" "+x.lname;
        }
    }
    
this keyword: this keyword is use to refer object inside it's own body.
    var x={
        fname:'fareen', 
        lname:'ansari',
        rno:1, 
        age:23,
        fullname:function(){
            return "Fullname:"+this.fname+" "+this.lname;
        }
    }
   
</pre>

<h1>Type casting</h1>
<pre>
1) (+) : end result string
1+'fareen' = '1fareen'

2) (-) : end result number
1-'fareen' = NaN
1-'1' = 0

<b>To convert number into decimal,octal,hexadecimal</b>

Example:var n=17;
var bin=n.toString(2);    //10001
var oct=n.toString(8);    //021
var hex=n.toString(16);   //0x11

We can use parseInt ,parseFloat function.
parseInt("11",2);     //3
parseInt("ff",16);    //255
parseInt("077",10);   //77
parseFloat("77.9");   //77.9
parseInt("fareen");   // NaN


<b>Converting string into number:</b>
To convert number to string , two ways:

(1)subtracting 0 with the string
var a="10"
var b=a-0;
Note adding with 0 does not convert it into string rather it will do string concatination.

(2)using Number function:
Example: var b=Number(a); 
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

<a name="date"><h1>3. Date</h1></a><br>
<pre>
4 methods to create date:

<b>1)new Date()</b>
Example:
let x=new Date()

<b>2)new Date(year, month, day, hours, minutes, seconds, milliseconds)</b>
Example: let y=new Date(2021, 1, 07)

here i)if there is year there month argument is must else it'll print 1/1/1970

<b>3)new Date(milliseconds)</b>
Example:
let y=new Date(2021, 1, 07)
will return the date time, takes parameter in milliseconds
new Date(date string)

<b>4)Date & Time Methods:</b>


        Creating date object:
        d today = new Date()            //Mon Jul 19 2021 10:16:14 GMT+0530 (India Standard Time)
        let birthday = new Date(1995, 11, 17)           //Sun Dec 17 1995 00:00:00 GMT+0530 (India Standard Time)
        Here jan starts with 0, feb=1 ...so on

        But if we take hour,minute,seconds then jan=1 feb=2 ...so on:
        let birthday = new Date('1997,01,07 03:24:00')      //Tue Jan 07 1997 03:24:00 GMT+0530 (India Standard Time)
        
        To get month, year, day, minutes etc use:
        birthday.getFullYear()
        1997
        birthday.getMonth()
        1
        birthday.getDate()
        7
        birthday.getHours()
        3
        birthday.getMinutes()
        24
        birthday.getSeconds()
        0
        birthday.getTime()
        855266040000
</pre>

<a name="three"><h1>3. Expressions and Operators</h1></a><br>
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

<b>6)For in Loop(in ECMA 2015)</b>
used to iterate the index
this is kind of like python for loop:

var ele = [1,2,'fareen',false]
for(let i in ele){
	console.log(i);
}

<b>7)For of Loop(in ECMA 2015)</b>
used to iterate the values
var ele = [1,2,'fareen',false]
for(let i of ele){
	console.log(i);
}


<b>8)forEach</b>
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

<b>1)Anonymouse Function</b>
A function with no name
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

<h1>ECMS Script 2015(ES6)</h1>
<pre>
ECMA Script 2015 brings:

1)LET & CONST
2)TEMPLATE STRING
3)DEFAULT ARGUMENT
4)REST OPERATORS
5)DESTRUCTURING
6)OBJECT PROPERTIES
7)ARROW FUNCTION
8)SPREAD OPERTAOR

<b>1)LET VS CONST VS VAR(Interview)</b>

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


VAR,LET AND CONSTANT

To store value or user input we use variables
DECLARING:
var variable_name = value; //this can be reassign
const constant_name = value; //value of const won't be change
    var x=10;
    document.write(x);

    output:10

    var x=20;
    document.write(x);

    Output:20       //here the value of x is reassigned.

    for constant:
    const y=20;
    document.wtite(y)

    we cannot assign constant like this but var can be:
    const x;
    x=20;         //invalid

But we can declare the const again using the block/scope:
    const x=20;
    document.write("The value of const outside the scope:",+x)
    {
        const x=30;
        document.write("<br>The value of const inside the scope:",+x)
    }
    document.write("<br>The value of const outside the scope:",+x)

Output:
The value of const outside the scope:20
The value of const inside the scope:30
The value of const outside the scope:20


<b>2)TEMPLATE STRING</b>

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


<b>3)DEFAULT ARGUMENT</b>

function mult(a,b=5){
	return a*b;
}

console.log(mult(5));

if we give something like this function mult(a=5,b)
so in python above stmt will give default argument follows non default or somethig like this
but here we'll get NaN cuz a=5 already defined and againg we pass 5 for a value by default it starts giving value from first paramater so default argument should be at last.


<b>4)FAT ARROW FUNCTION</b>
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

<b>5)Array Destructuring</b>

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

<b>5)Object Destructuring</b>
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

<b>6)Object Properties</b>
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

<b>7)Spread Operator</b>
If in case we need entire array we can use spread operator:
let color = ['red','pink','blue'];
let newcolor = [...color, 'white','yellow'];
console.log(newcolor);
O/p:
['red', 'pink', 'blue', 'white', 'yellow']
</pre>

<h1>ECMAScript 2016(ES7)</h1>
<pre>
1)Array.prototype.includes
2)Exponential Operator

<b>1)Array.prototype.includes</b>
To find the particular data is present or not we can use array include
let color = ['red','pink','blue'];
const isPresent = color.includes('pink');
O/p:
true

const isPresent = color.includes('cyan');
O/p:
false

<b>2)Exponential Operator()/power</b>
23
meaning 2 power 3, 2x2x2 = 8
</pre>


<h1>ECMAScript 2017(ES8)</h1>
<pre>
1)String padding: to give padding to string
let myName = "Fareen".padStart(7);	//Fareen contains 6 chars so 6+1 space, so we'll get 1 space in start
let myName = "Fareen".padEnd(7);
o/p:
' Fareen'


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

<h1>ECMAScript 2018(ES9)</h1>
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
<b>1)flat array:</b>
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

<b>2)flatMap</b>

<b>3)Object.fromEntries()</b>
const person = {name: 'fareen', age:24};
const arrObj = Object.entries(person);
console.log(arrObj);
o/p:
[['name','fareen'],['age',24]];

To convert the array back to object
console.log(Object.fromEntries(arrObj));
o/p: {name: 'fareen', age: 24}

<b>3)Object.prototype.{trimStart, trimEnd}: to remove space.</b>

<b>4)Symbol.prototype.description</b>

<b>5)JSON.stringify()</b>

<b>6)Function.prototype.toString()</b>
</pre>

<h1>ECMAScript 2020</h1>
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

1)document.getElementById()
2)document.getElementsByClassName()
3)document.getElementByTagName()

<h3>querySelector</h3>
we can change css style using the querySelector(to select class or id and then change color etc) 

Example:
document.querySelector('#myclass')
x.style.color = "red";
</pre>

DIagram:

<a name="nine"><h1>9. BOM</h1></a><br>
<pre>
alert, confirm, prompt
This are not part of DOM but part of Browser that is why it is BOM

JS POPUP ALERT

    1)alert() example:
    var hello=()=>{
        alert("This is hello function")
    }

    <button onclick="hello()">Hello</button>

    2)window.confirm() example:
    In this we'll get two button alone with the alert OK and CANCEL.
    Example:
    var deleteOpt=()=>{
        window.confirm("Are you sure to delete this record?");
    }

    <button onclick="deleteOpt()">Delete</button>

    3)prompt() example:
    To take input:
    Example:
    var num=()=>{
        var x=window.prompt("Enter a number:");
        document.write("The type of number is:"+typeof(x));
    }

    <button onclick="num()">Number</button>
</pre>

<a name="ten"><h1>10. Windows Object</h1></a><br>
<pre>
Document is part of windows object
and by default everything is a part of windows so we dont ned to write windows. as in
innerHeight and window.innerHeight both will return the same output 
here windows is optional cuz everything is part of windows by deafult.

The window object is supported by all browsers. It represents the browser's window. All global JavaScript objects, functions, and variables automatically become members of the window object. Global variables are properties of the window object. Global functions are methods of the window object. Even the document object (of the HTML DOM) is a property of the window object.
Run all commands on browser console window.
    1)window.innerHeight
    the inner height of the browser window (in pixels)
        Example:
        window.innerHeight;             //150

    2)window.innerWidth;
    the inner width of the browser window (in pixels)
        Example:
        window.innerWidth;              //1536

    3)window.open()
    open a new window
        Example: window.open()          //opens a new window , with title=untitled and url=about:blank

    4)window.close()
    close the current window

    more on doc.
    
<b>JS WINDOW LOCATION</b>
The window.location object can be used to get the current page address (URL) and to redirect the browser to a new page.

    1)window.location.href 
    returns the href (URL) of the current page
    Example:
        window.location.href;               //"file:///E:/My%20stydy%20website/JavaScript/prac.html"

    2)window.location.hostname 
    returns the domain name of the web host
    Example:
        window.location.hostname;           //"developer.mozilla.org"   (mdn hostname)

    3)window.location.pathname 
    returns the path and filename of the current page
    Example:
        window.location.pathname;           //"/en-US/docs/Web/JavaScript"    (mdn pathname)

    4)window.location.protocol 
    returns the web protocol used (http: or https:)
    Example:
        window.location.protocol;           //"https:"

    5)window.location.assign() 
    loads a new document
    Example:
        window.location.assign("https://www.w3schools.com");            //will open the //www.w3schools.com

<b>JS HISTORY</b>
The window.history object contains the browsers history.
    1)window.history.back()         //will go a step back in browser.
    2)window.history.forward()      //will go a step ahead in browser.
    
<b>JS NAVIGATOR</b>
The window.navigator object contains information about the visitor's browser.
    1)navigator.appName; 
    returns the application name of the browser:
    Example:
        navigator.appName               //"Netscape"
    
    2)navigator.appCodeName             //"Mozilla"
    
    3)navigator.cookieEnabled
    property returns true if cookies are enabled, otherwise false:
    Example:
        navigator.cookieEnabled;        //true

    4)navigator.appCodeName             //"Win32"
</pre>

<a name="screen"><h1>10. Screen</h1></a><br>
<pre>
The window.screen object can be written without the window prefix.
    1)screen.width
    returns the width of the visitor's screen in pixels.
    Example:
        screen.width;           //1536

    2)screen.height
    returns the height of the visitor's screen in pixels.
    Example:
        screen.height;          //864

    3)screen.availWidth
    returns the width of the visitor's screen, in pixels, minus interface features like the Windows Taskbar.
    Example:
        screen.availWidth;          //1536

    4)screen.availHeight
    returns the height of the visitor's screen, in pixels, minus interface features like the Windows Taskbar.
    Example:
        screen.availHeight;         //824

    5)screen.colorDepth
    returns the number of bits used to display one color.
    All modern computers use 24 bit or 32 bit hardware for color resolution:
    24 bits =      16,777,216 different "True Colors"
    32 bits = 4,294,967,296 different "Deep Colors"
    Older computers used 16 bits: 65,536 different "High Colors" resolution.
    Very old computers, and old cell phones used 8 bits: 256 different "VGA colors".
    Example:
        screen.colorDepth;          //24

    6)screen.pixelDepth
    returns the pixel depth of the screen.
    Example:
        screen.pixelDepth;          //24
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

<h1>VARIABLES,LET AND CONSTANT</h1>
<pre>
To store value or user input we use variables
DECLARING:
var variable_name = value; //this can be reassign
const constant_name = value; //value of const won't be change
    var x=10;
    document.write(x);

    output:10

    var x=20;
    document.write(x);

    Output:20       //here the value of x is reassigned.

    for constant:
    const y=20;
    document.wtite(y)

    we cannot assign constant like this but var can be:
    const x;
    x=20;         //invalid

But we can declare the const again using the block/scope:
    const x=20;
    document.write("The value of const outside the scope:",+x)
    {
        const x=30;
        document.write("<br>The value of const inside the scope:",+x)
    }
    document.write("<br>The value of const outside the scope:",+x)

Output:
The value of const outside the scope:20
The value of const inside the scope:30
The value of const outside the scope:20
</pre>

<a name="fourteen"><h1>14. Events</h1></a><br>

<a name="fifteen"><h1>15. Storage</h1></a><br>
<pre>
<b>What are Cookies?</b>
Cookies are data, stored in small text files, on your computer. When a web server has sent a web page to a browser, the connection is shut down, and the server forgets everything about the user. Cookies were invented to solve the problem "how to remember information about the user": When a user visits a web page, his/her name can be stored in a cookie. Next time the user visits the page, the cookie "remembers" his/her name. Cookies are saved in name-value pairs like:

Cookie

            Creating a cookie:
                document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";
            To view cookie:
                console.log(document.cookie);
		
<b>Local Storage</b>

            Local storage are persistance.
            Creating local storage:
                localStorage.setItem('name','Bob');
                console.log(localStorage.getItem('name'));
            Removing loack storage:
                localStorage.removeItem('name');
            To update the local storage use the set item with different name:
                localStorage.setItem('name','Annu');
            
        
<b>Session Storage</b>

            This is same as local storage:
            Creating a session storage:
                sessionStorage.setItem('name','John');
                console.log(sessionStorage.getItem('name'));
            Removing the session storage:
                sessionStorage.removeItem('name')
</pre>

<a name="sixteen"><h1>16. Class & Objects</h1></a><br>
