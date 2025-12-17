# JAVASCRIPT NOTES

## KEYWORDS

keywords are predefined words which have some meaning in javascript. for example :- `for`, `while`, `true`, `false`, `typeof`, `let`, `var`, `const`,  etc.

## WORDS (IDENTIFIER or VARIABLE)

they are user defined words which satisfy the below conditions :-
-  they can contain uppercase letters (A to Z), lowercase letters (a to z), digits (0 to 9), and some special characters like underscore( _ ) and dollar sign($).
- they can't be a keyword.
- they can't contain whitespace ( ) or any other special character like &, %, @, #, etc.
- they can't start from digit(0 to 9) only alphabet(a to z) are allowed in the starting.

## VARIABLE

they are like a container, we can store out data in it.

there are five ways for creating a variable:-
```javascript
let a;                          //1
let a = 12;                     //2
var a;                          //3
var a = 12;                     //4
const a = 12;                   //5
const a;                        //doesn't exists (will always give an error)
```
1. - **var**  
        -  window mai add hota hai
        -  function scoped hota hai (mtlb yeh variable ek function ke andr use ho sakta hai or function ke bahr iski koi existance nhi hogi)
        - variable doesn't respect blocks.
        - can be declared again without an error (ek hi variable ko let says `a` ko do baar alag alag value ke sath declare kr skta hai  )
2. - **let** 
        - block scoped
        - can't be declared again.
        - can update the value of variable.
3. - **const**
        - variable will be constant value becomes unchangeable.

## DECLARATION AND INITIALIZATION

let suppose we created a variable
```javascript
let a;
```
it is called declaration(mtlb hmne koi variable banaya toh usko bolte hai declare krna ) or jb hmne uski phli value dedi toh use khte hai initialization. like this
```javascript
let a = 12;
```
it's `declaration + initialization`.

## SCOPE

- **GLOBAL**
those variable which are not defined inside any brackets.

- **BLOCK**
`{ }` the region inside these curly brackets are block scope.

- **FUNCTION**
`function(){}` variable which can be used inside a function are function scoped variables.

## REASSIGNATION VS REDECLARATION

```javascript
let a = 12;
let a = 13;
```
the above case is called re-declaration. are we are declaring `a` two times in global scope with let variable. this will give an error as redeclaration is not allowed with let keyword.

```javascript
let a = 12;
a = 13;
```

the above case is of re-assignaton which means we are giving a new value to our variable. this results the `a` variable will contain 13 value from now onwards.

## TEMPORAL DEAD ZONE

```javascript
console.log(a);



let a = 12;
```

this will definately gives an error `cannot access 'a' before initialization` as we are requesting for loging a value which doesn't exist before this line.

```javascript
console.log(a);
```
the above code will give an error `'a' is not declared`.

> mltb temporal dead zone utna area hai jitne ai javascript ko yeh pta hai ki variable exist krta hai pr wo use excess nhi kr skta. mtlb agr variable line no. 101 pe bna hai toh line no. 1 to 100 will be te teporal dead zone.

```javascript
console.log(a);



var a = 12;
```
variable doesn't have the temporal dead zone. output will be `undefined` due to hoisting.

## HOISTING IMPACT PER TYPE

We can say ,
jb hm koi variable create krte hai to wo 2 part mai tut jata hai (declaration and initialzation) or uska declaration part code mai sbse upr chala jata hai or initialization part whi rhjata hai.

```javascript
var a = 12;
```
toh yeh do part mai tutega joki honge
```javascript
var a = undefined;


a = 12;
```
## DATA TYPES
THERE ARE TWO TYPES OF DATA TYPES:
1. PRIMITIVES
   - jo bina brackets ke use ho
   - jinke directly copy kiyaa ja ske 
2. REFERENCE
    - jo brackets se bne ho.
    - jinke copy kre toh hme dusre us datatype ka reference miljae (mtlb agrr hm kisi array ko copy kre arr2 mai toh gr hm arr2 ke elements mai change krenge toh wo arr1 mai bhi hoga.)

    ### PREMITIVE DATA TYPE
    1. STRING
        - `' '` single quotes
        - `" "` double quotes
        - ` `` ` backtick. 
            - variable term ko likhne k liye, use `${variable}` 

    2. NUMBER
    3. BULLEAN
        - TRUE
        - FALSE
    4. NULL
        - mtlb variable ki koi value toh hai par aapne jaan buchke abhi ke liye koi value nhi di in future null ko replace krke woh value daal skte hai.`let a = null;`



     5. UNDEFINED
        - jb hmne ek variable bnaya or usko value nhi di toh jvascript jo by default value deti hai wo undefined hoti hai. `let a;` here a = undefined

    6. SYMBOL
        - future mein hum koi libraries use karege ab is case mein un libraries mein kai baar kuchh fields hoti hai jinse similar hum bhi banaa dete hai aur galti se humaari banaai hui fields us library ki original fields ko change kar deta hai. `symbol(uid) = x`.

    7. BigInt
        - javascript mai ek max integer value hai jiske baad calculation errors aane lag jate hai jisko overcome krne k liye hm `n` letter ko us integer value ke end mai lagate hai. `8325932868n`
        > to check the bigest integer value in javascript type `Number.MAX_SAFE_INTEGER`
        
    ### REFERENCE DATA TYPE
    1. ARRAY
    2. OBJECTS
    3. FUNCTION
    

## DYNAMIC TYPING

> javascript mai static typing nahi hai isme dynaamis typing hai. dynamic typing ka mtlb hai ham kisi bhi variable mai kisi bhi datatype ki value daal skte hai or firr use change bhi krr skte haii like => 

``` javascript
let a = 14;
a = "hello world" ;
```
static typing mtlb variable ko starting mai hi datatype assign kr dena jisko wo baadme jake change nahi kar skta.

## TYPEOF QUIRKS

``` javascript
        > typeof "hello"       //string
        > typeof 11            //number
```

`" "` represents string and `11` is a number datatype

``` javascript
        > typeof null          //object
```

because of `bug` javascript returns object

``` javascript
        > typeof []            //object
```

`[]` represents `array` , which is a type of object.

``` javascript
        > typeof NaN          //number
```

`NaN` stands for `not a number` but the type of returns a number because it is a failed mathematical number operation , like `"harsh" * 3` 

## Instanceof

The instanceof operator in JavaScript determines whether an object is an instance of a particular class or constructor function. In simpler terms, it checks if an object was created using a specific "blueprint."
for example:-

```javascript
a = []
b = 12
a instanceof array              //true
a instanceof object             //true
b instanceof number             //true
b instanceof object             //false
```

## TYPE COERCION

> aaisa concept jisme aapka ek type dusre type mai automatically convert hojye.

for example:-
``` javascript
        > "1" + 1              // 11

        > "4" - 1              // 3
```

reason being, in javascript `+` stands for `addition` and `concatenation`. if one of the opperant is string then javascript convert the other one into string and then concate them.

where as ; when we talk about `-` it stands only for `subtraction` so if there is a string value present in an opperant then js convert it to a number (if possible) and then subtract.  

there is a huge difference between == and ===

## TRUTHY VS FALSY VALUES

all the values given below will return a false (or the meaning of these values is false) :-

- 0
- false
- NaN
- ""
- null
- undefined
- document.all

rest all the values will return a true (truthy in nature).

> to check whether a number is true or false. just add `!!` in the starting of the value in console window.

## OPERATORS

### 1. Arithmetic Operators

- `+` stands for
    - addition `1 + 2` returns `3`.
    - concatenation `"hello" + "world"` returns `helloworld`.

- `-` stands for subtraction `2 - 1` returns `1`.

- `*` stands for multiplication `2 * 2` returns `4`.

- `/` stands for division `2/2` returns `1`.

- `%` stands for modulus which returns remainder. `15 % 2` returns `1`.

- `**` stands for exponentiation `2**3` returns `8`.

### 2. Comparison Operator

- `==` is used for comparing two different values (not strict comparison).

```javascript
12 = 13     //false
12 = "12"   //true
```
 
- `===` is used for comparing two different values with their data type (strict comparison).

```javascript
12 === "12"             //false
"12" === "12"           //true
"priya" === "Priya"     //false
```

- `!=` stands for not equal (not strict comparison).

```javascript
12 != 13    //true
```

- `!==` stands for not equal with checking their data types (strict comparison). 

- `>` stands for greater than.

- `<` stands for less than.

- `>=` stands for greater than equal to.

- `<=` stands for less than equal to.

### 3. Assignment operator

- `=` is used for value assignation. 

```javascript
let a = 2;
```
- `+=` stands for add and then update. 

```javascript
let a = 12;
a += 3;          //new value of a = 15
```

- `-=` stands for subtract and then update.

```javascript
let a = 12;
a -= 2;          //new value of a = 12
```

- `*=` stands for multiply and then update.

```javascript
let a = 12;
a *= 3;         // new value of a = 36
```

- `/=` stands for divide and then update the variable value.

```javascript
let a = 12;
a /= 3;         // new value of a = 4
```

- `%=` means first find the remainder and then update the value of variable.

```javascript
let a = 12;
a /= 5;         // value of a will be 2
```
### 4. Logical Operator

- `&&` is known as `AND Operator` which means if both the operands are `true` then only it returns true otherise if returns `false` in every other case.

|Operand 1|Operand 2|Output Value|
|----|----|----|
|True|True|True|
|True|False|False|
|False|True|False|
|False|False|False|

- `||` is known as `OR Operator` which means if any of the operand pass true value then it returns a true. then case when both operands are false then only it returns a false.

|Operand 1|Operand 2|Output Value|
|----|----|----|
|True|True|True|
|True|False|True|
|False|True|True|
|False|False|False|

- `!` is `Not Operator` which reverse the value. if the answer is true then it returns a false, if it is false then it return true.

> if we use !! then it will reverse the value two times and gives the real truthy and falsy nature.

### 3. Unary Operator

these operators are only applicable for a single value.

- `+` stands for addition
> if we use + in front of any string which is number from inside then this + operator convert that string into a number. (if there is a string which can't be converted into a number then js will return 'NaN' for sure. )

- `-` stands for subtraction
> it is used to change the nature of a number i.e. positive and negative.

- `!` is a not operator which reverse the nature of the value.

- `typeof` used to find the type of any given value.

- `++`
 1. pre-increment -> first then value is increased by 1 and then it is used in the expression.

``` javascript
a = 12;
++a;            //13
```
2. post-increment -> first the value is used in the expression then after it will increase by 1.

``` javascript
a = 12;
a++;            //12
b = a;          //13
```

- `--`
 1. pre-increment -> first then value is decreased by 1 and then it is used in the expression.

``` javascript
a = 12;
--a;            //11
```
2. post-increment -> first the value is used in the expression then after it will decrease by 1.

``` javascript
a = 12;
a--;            //12
b = a;          //11
```

### 6. Ternary Operator

`?:`is known as ternary Operator which is an easy way of writing if condition statment for a single condition.
standard form of writing it is:-

```javascript
        condition ? if true then : if false then
```
for example:-

```javascript
12 > 13 ? console.log("true") : console.log("false");           // 12 is not greater then 13 then the output will be false.
```

## CONTROL FLOW

### 1. If Statement

if the condition written in () meets true then the code written in {} will execute. 

```javascript
if (condition){
        //do some work
}
```

### 2. If Else Statement

if the condition written in () meets true then the code written in {} of if statement will execute otherise the code of else will executes.

```javascript
if (condition){
        //do some work
} else{
        //do some more work
}
```
for example:-

```javascript
if (100>50){
        console.log("true");
}else{
        console.log("false")
}                                //output false
```

### 3. Else If Statement

it is used for handling multiple conditions.
```javascript
a = 75;
if (a>80){
        console.log('A');
}else if(a>50){
        console.log('B');
}else{
        console.log('C , failed!')
}
```

### 4. Switch Case Statement

```javascript
a = 1
switch (a) {
	case 1:
		console.log('good');
		break;
	case 2:
		console.log('fair');
		break;
	default:
	        console.log('please enter a valid value');
}
```

### Early Return Pattern

```javascript
function getval(val){
        if(val>75) return "A";
        else if (val > 50) return "B";
        else if (val > 33) return "C";
        else return "fail";
}
console.log(getval(69));
```

## LOOPS

> javascript mai kuch bi repeat karne ko loops kehte hai.

kaha se jaana hai -> kaha tak jaana hai -> kese jana hai --> `for loop`.

kaha se jaana hai -> kab rukna hai -> kese jana hai --> `while loop`.

### For Loop

```javascript
for(start ; end ; change){
        //code
};
```

for example; print from 1 to 100:-

```javascript
for(let i = 1 ; i = 100 ; i++){
        console.log(i);
};
```

### While Loop

```javascript
start
while(end){
        //code
        change;
};
```

for example; 1 se jbtk 32 nhi aajata value print kro:-

```javascript
let i = 1 ; 
while ( i < 32 ){
        console.log(i);
        i++;
};
```

### Do While Loop

```javascript
start
do{
        //code
}
while(end);
```

for example:-

```javascript
let i = 1 ;
do{
        console.log(i);
        i++;
}
while(i<32);
```

## BREAK AND CONTINUE

```javascript
for( let i = 1 ; 1 < 101 ; i ++){
        if(i === 44){
                continue;       //when the value of i reaches 44 then i will not be logged and the code will run further.
        }
        console.log(i);
        if(i === 32){
                break;          //when the value of i reached to 32 then the code will stop!
        };
};
```

## FUNCTIONS

> jab hm koi code likhte hai to wo automatically run krne lgta hai pr agr hme chahiye ki jb hm khe wo tbhi work kre us se phle na kre..uske liye hm use krte hai functions

- doesn't work before calling.
- can be used more than once(baar baar pura code nhi likhna pdta).
- which saves time.

everytime when we need to run that particular function we need to call it `func_name()` like this!!

### Function Declaration

```javascript
function func_name() {
        //code
};
func_name();
```
func_name is the name of function. user can make function name by there own.

### Function Expression

```javascript
let func_name = function() {
        //code
};
func_name();
```

here, func_name is a variable in which a function is stored. it is also the name of that function.

### Fat Arrow Function

```javascript
let func_name = ()=>{          
        //code
}
fnc();
```
`func_name` is a variable here and also the name of the name of the function.

### Parameter AND Arguement

variables which are used at the time of function making in () brackets are called `Parameters` whereas the values we use in the place of those variables at the time of function calling are known as `Arguements`.

- #### DEFAULT PARAMETERS

if you defined some variable as parameters and doesn't give them  value while calling will result an undefined value.

```javascript
function add(v1 , v2){
        console.log(v1 , v2);
}
add();          //output will be undefined , undefined
```

trying adding two undefined values results a `NaN`.

```javascript
function add(v1 , v2){
        console.log(v1 + v2);
}
add();          //output will be NaN
```

in these cases, if you don't need these types of things in your code so you can set some default parameters so that if the function doesn't get the value at calling time so it can use the default value.

```javascript
function add(v1 = 0, v2 = 0){
        console.log(v1 + v2);
}
add();          //output will be 0.
```
l
- #### REST and SPREAD PARAMETER

if there are many values in the arguement so we need to create the same number of parameters , at this time we use rest parameter. `...val` where val is a variable.

```javascript
function add(...val){
        console.log(val);
}
add(1,2,3,4,5);          //output will be [1,2,3,4,5]
```
 agr hm iska use function parameter space mai karte hai to woh rest parameter hote hai or agr iska use array yah object mai kare toh woh spread parameter hote hai.

### Return and Early Returns

```javascript 
function abcd(){
        return 12;
}
console.log(abcd());            //output = 12
```

### First Class Function

functions can be treated as values.

```javascript
let abcd(val){
        val();
}
abcd(function(){
        console.log("hello");           //output => hello
});
```

### High Order Function

functions which returns or accept a function in its parameter. In the above code,

```javascript
let abcd(val){
        val();
}
```
OR 
```javascript
let abcd(){
        return function(){
                //code
        }
}
abcd()()                //here the first bracket if for running abcd function and 2nd one is for running inner function
```
we call it as a high order function.

### Pure VS Impure Function

aaisa function jo bahr ki value ko na badle woh pure function.

aaisa function jo bahr ki value ko badalde woh impure function.

```javascript
let a = 12;

function abcd(){                        //pure function
        console.log("hello");
};

function nextVal(){                     //impure function
        a++;
};
```

### Closure

ek function jo return kare dusra function aur return hone wala function parent function ka variable use kre.

```javascript
function abcd(){
        let a = 12;
        return function(){
                console.log(a);
        };
};
```

### Lexical Scope

``` javascript 
function abcd(){
    let a = 12;
    function defg(){
        let b = 13;
        function hijk(){
            let c = 14;
        };
    };
};
```

 Lexical scope ka mtlb hai ki jaise hmne `a` variable bnaya toh hm usko pure abcd() function m access kr skte hai mtlb function defg() or function hijk() mai bhii pr hmne function defg() mai b variable bnaya toh hm use defg() mai or hijk() mai hi excess kr skte hai abcd() mai nhii or c variable ko sirf function hijk() mai. So point is ki aapke variable ka scope kya h.


### IIFE (IMMEDIATELY INVOKED FUNCTION EXPRESSIONS)

``` javascript 
(function (){
    console.log("hello");
}) ();
```

It is like hmne koi function bnaya bina naam diye or usko () mai dal diya and ushi time usko call krdiya is called IIFE. 


### Hoisting difference between variable and function

Which means :-
``` javascript 
abcd();


function abcd(){
    console.log("hello");
};
```
 
mtlb aap function ko banane se phle usko call kar skte hoo pr yeh sirf function statement and function declaration mai work karti hai function expressions mai work nahi krti firr same error aata hai jesa variable mai aata hai.


## ARRAY
### create an array using -
```javascript
let arr = [1,2,3,4];
```
OR
```javascript
let arr = new Array();
```

- **index value of array starts from 0 to upto so on from the L -> R direction.**
- **from R -> L directon index values are  -1,-2,-3,-4,...**

 means the index value of the above array is :-

|value|index value L -> R|index value R -> L|
|:----:|:----:|:----:|
|1|0|-1|
|2|1|-2|
|3|2|-3|
|4|3|-4|

```javascript
arr[0];                 //arr_name[position]
```
this will give the value of array at 0th position.

### Array Modifictaion

```javascript
let arr = [1 , 2 , 3 , 4] ;
arr[2] = 12 ;                   //ouput = [1 , 2 , 12 , 4]
```

**asking for any value which doesn't exist returns an `undefined`**

### Array Methods

- **PUSH** - adding value in the last position.
```javascript
let arr = [1 , 2 , 3 , 4];
arr.push(100);                  //arr will be [1 , 2 , 3 , 4 , 100]
```

- **POP** - remove the lastmost value from the array.

```javascript
let arr = [1 , 2 , 3 , 4];
arr.pop();                  //arr will be [1 , 2 , 3]
```

- **SHIFT** - remove the first value from the array.

```javascript
let arr = [1 , 2 , 3 , 4];
arr.shift();                  //arr will be [2 , 3 , 4]
```

- **UNSHIFT** - this will add element in the starting of array.

```javascript
let arr = [1 , 2 , 3 , 4];
arr.unshift(100);                  //arr will be [100, 1 , 2 , 3 , 4 ]
```

- **SPLICE** - this will remove element from the given position and your can also give the no. of values your want to remove continuously.

```javascript
let arr = [1 , 2 , 3 , 4];
arr.splice(2 , 1);                  //arr will be [1 , 2 , 4 ] as this method one value from index 2.
```

```javascript
let arr = [1 , 2 , 3 , 4 , 5];
arr.splice(2 , 2);                  //arr will be [1 , 2 , 5 ] as this method two value from index 2.
```

- **SLICE** - slice doesn't change the original array. it can be stored in a new array.
```javascript
slice(start? : number , end? : number);
```

```javascript
let arr = [1 , 2 , 3 , 4 , 5];
let newarr = arr.slice(0, 3);           //from index position 0 to 3
console.log(newarr);            // [1 , 2 , 3 , 4]
```

- **REVERSE** - this will reverse your array.

```javascript
let arr = [1 , 2 , 3 , 4 , 5];
arr.reverse();                  //[5 , 4 , 3 , 2 , 1]
```

- **SORT** - this will sort your array in ascending or descending order.

```javascript
let arr = [22 , 3 , 55 , 10];
arr.sort(function(a , b){
        return a - b;
});                             //[3 , 10 , 22 , 55]
```

```javascript
let arr = [22 , 3 , 55 , 10];
arr.sort(function(a , b){
        return b - a;
});                             //[55 , 22 , 10 , 3]
```

- **FOREACH** - 
```javascript
let arr = [1 , 2 , 3 , 4];
arr.forEach(function(val){
        console.log(val);
});
```

array ki har ek value ke liye ek function chlega mtlb according to there index values ek ek krke value function k parameter ko milegi or firr us value ke liye function chalega.

- **MAP** - 

```javascript
let arr = [1 , 2 , 3 , 4];
arr.map(function(val){

});
```
map bhi forEach ki trh array se ek ek value leta hai or uspe function apply krwata hai or use ek nye array mai save krdeta hai.
> `arr.map()` ka use sirf tbhi krna hai jab jb aapko ek nya array bnana ho purane ke data ke basis pe.
- purane or nye array k no. of values equal hogi.  
- map method dikhte hi ek nya blank array bnalo mind mai.

```javascript
let arr = [1 , 2 , 3 , 4];
let newArr = arr.map(function(val){
        return 12;
});                             //newArr = [12 , 12 , 12 , 12]
```
- return krna compalsary hai nahii toh `undefined` return hojaega automatically.

- **FILTER** - 
```javascript
let arr = [1 , 2 , 3 , 4 , 5 , 6 , 7 , 8];
let newArr = arr.filter(function(val){
        if(val > 4) return true;
        return false;
});                             //this results newArr = [5 , 6 , 7 , 8]
```
filter method bhi map ki trh hai woh ek ek krke arr se value leta hai uspe funtion lgata hai or agr return mai true hoga toh us value ko new array mai pass kar dega or agr false hoga toh usko delete kar dega.

- **REDUCE** - array ko reduce kar dena ek single value mai.

```javascript
let arr = [1 , 2 , 3 , 4];
arr.reduce(function(accumulator , val){
        return accumulator + val
}, 0);                          //10
```
accumultor ek variable hai jiski value hmne last mai define kr rkhi h i.e. 0 or yeh apni value yaad rkhta hai. or function mai jo value return hoti hai woh waps accumulator mai chali jati hai.

- **FIND** - find ke function k return mai jo conditon hai yeh usko dhundta hai array mai or jha ise sbse phli value mil jati hai toh ushe print krwadeta hai.

```javascript
let arr = [1 , 2 , 3 , 4 , 3 , 1]
arr.find(function(val){
        return val === 3;
});
```

- **SOME** - 
```javascript
let arr = [ 10 , 20 , 88 , 64];
let any = arr.some(function(val){
        return val > 50;
});
console.log(any);                     //true
```

mltb agr some method ke andr jo function hai uski return condition kisi ek bhi value pe satisfy hojati hai toh woh output mai true deta hai otherwise false.

- **EVERY** - 
```javascript
let arr = [ 10 , 20 , 88 , 64];
let every = arr.every(function(val){
        return val > 5;
});
console.log(every);                     //true
```
mltb agr some method ke andr jo function hai uski return condition hr value pe satisfy hojati hai toh woh output mai true deta hai otherwise false.

### DESTRUCTIVE OPERATOR

let's suppose you have to copy some elements from an array to a new array and you don't want to use that `arr[0]` property multiple times so there is an another way for that :-

```javascript
let arr = [1 , 2 , 3 , 4];
let newArr = arr;               //this will give you the reference of arr so if you make any changes in newArr if will be done is  arr also. so this is a wrong way of copying an array!!
```
so here is the correct way of copying an array.

```javascript
let arr = [1 , 2 , 3 , 4];
let [a , b , , c] = arr                 //a = 1; b = 2; c = 4
```
if you want to copy the whole array

```javascript
let arr = [1 , 2 , 3 , 4];
let newArr = [...arr];                  //this ... will make all value of arr copied to newArr.
```

`...` operator is known as spread operator as we studied above. It is only used for arrays. which means take all the values from `arr` and spread it in `newArr`. 
