# C NOTES

## VARIABLE
- variables are case sensitive.
- 1st character should be an `alphabet` or `_`.
-  no comma / blank space allowed.
- No other symbol other than '_'.
---
### DATA TYPES

diferent data types uses different number of bytes value. `8 bit = 1 byte`. here are some data types and there size in bytes.

|Data type|size in bytes|
|:---- |----:|
**Char or signed char**|1
**Unsigned char**|1
**int or signed int**|2
**Unsigned int**|2
**short int or Unsigned short int**|2
**Signed shorot int**|2
**Long int or Signed long int**|4
**Unsigned long int**|4
**float**|4
**double**|8
**Long double**|10

> data types like `string` and `boolean` doesn't exists in C language as it isvery old language and at that time these things are not defined.

---
- #### INTEGER DATA TYPE

    data like whole numbers and digits are stored in integer data type. `int`

    ```c
    int age = 22;
    ```

- #### FLOAT DATA TYPE

    they are used to store decimaal values. 

    ```c
    float pi = 3.14;
    ```

- #### CHARACTER DATA TYPE

    they are used to store characters.

    ```c
    char hashtag = '#';
    ```
---

## CONSTANTS

the value which remains the same a in whole period of time called constants.

### INTEGER CONSTANTS

EXAMPLES:- `1`, `2`, `3`, `0`, `-1`, `-2`.
### REAL CONSTANTS

EXAMPLES:- `1.0`, `2.0`, `3.14`, `-2.4`
### CHARACTER CONSTANTS

EXAMPLES:- `'A'`, `'a'`, `'#'`, `'&'`

---
## KEYWORDS
reserved words that have special meaning to the compiler.

>there are 32 keywords in C

`auto`, `double`, `int`, `struct`, `break`, `else`, `long`, `switch`, `case`, `enum`, `register`, `typedef`, `char`, `extern`, `return`, `union`, `continue`, `for`, `signed`, `void`, `do`, `if`, `static`, `while`, `default`, `goto`, `sizeof`, `volatile`, `const`, `float`, `short`, `unsigned`

## PROGRAM STRUCTURE

```c
#include <stdio.h>

int main(){
    printf("HELLO WORLD");
    return 0;
}
```

HERE , `#include<stdio.h>` is a preprocessor directive. will discuss in detail after sometime.

uske baad `int main()` ki help se hm ek main function banate hai then jo compiler hai wohh main function ke andr ke code ko line by line check krta hai or run krta hai. `{}` ke andr jo code likha jata hai wo hoti hai statement  `;` ka mtlb ek trh se hota hai full stop. and funtion ki last statement hm `return 0` karte hai jisme `0` ka  mtlb hai 0 errors. mtlb hmara program 0 error ke run hojae 

---

## to print the output you need to run 2 code in terminal as follows:-
- gcc main.c
- ./a.exe

every time when you need to refresh the program and run it again.

---

## COMMENTS
 they are not a part of main program they are just used for to reader to explain what the given code is about of. 

 - `// comment here` used for single line comment.
 - `/*   comment here  */` used for multiple lines.

 mtlb yeh comments hmare code ka part nahi hote just extra instructions hote hai jo hm reader ko dete hai. like code ke bare m btana ki yeh code kis chj se related hai isme kya ho rha hai.

---

## OUTPUT 

for getting an output we use multiple functions.

### printf 
generally prints the given command.

```c
printf("hello world");
```
here the result output will be `hello world` , jo kuch bhi quotes ke andr likhe jate hai, single yah double quotes ke andr wo sara data as it is print ho jata hai. agr woh koi special command nhi hai to.

```c
#include<stdio.h>

int main(){
    printf("hello world");
}
```

is code ka output milega `hello world`. 
    
and yeh line multiple times print krwane ke liye is code ko utni hi time likhna pdega

```c
#include<stdio.h>

int main(){
    printf("hello world");
    printf("hello world");
    printf("hello world");
    printf("hello world");
}
```

the result will be `hello worldhello worldhello worldhello world` yeh pura code ek hi line mai print hoga kyuki hmne next line mai jane ki command nahi di thi. for that we need to:-

```c
#include<stdio.h>

int main(){
    printf("hello world\n");
    printf("hello world\n");
    printf("hello world\n");
    printf("hello world\n");
}
```

now the output will be 
```
hello world
hello world
hello world
hello world
``` 

as the command used `\n` is used for next line.

*if we want to print a variable after a string then we need to use:-*

1. **FOR INTEGER** - `%d`
```c 
#include<stdio.h>

int main(){
    int age = 18;
    printf("age is %d", age);
}
```

2. **FOR REAL NUMBERS** - `%f`
```c 
#include<stdio.h>

int main(){
    float pi = 3.14;
    printf("the value of pi is %f", pi);
}
```

3. **FOR CHARACTERS** - `%c`
```c 
#include<stdio.h>

int main(){
    char star = "*";
    printf("star look like this %c", star);

}
```

> `%d` , `%f` , `%c` are known as format verifiers. mtlb ye btate hai ki data kis format me aaega.

## INPUT

### scanf
 it is used to take input from the user. the format of using this function is 

 ```c
 scanf("%d" , age);
 ``` 
 which means hme age naam ke variable ka input lena hai jiska data type integer hoga.

```c
#include<stdio.h>

int main(){

    int age ;

    printf("enter your age:");
    scanf("%d", &age);
    printf("your age is %d", age);
    return 0;
}

```

is code ki explaination de toh `int age` sai age naam ka integer variable create hoga then print hoga `enter your age:` then compiler `scanf` ki wjh se user se input lega integer type input or usko age ke address pe save krdega and then print hoga your age is and user ne jo age input ki thi woh age.

## COMPILATION

compilation is a computer program which convert / translate  c language to machine language. 

**c code -> c compiler -> a.exe(windows)/a.out(mac).**

in general terms. c language code is written by coder in c language when we run the program it get checked by the compiler which checks all the errors in it. if the compiler found an error in the user's code it will give an error and compilation fails and if there is no error in it then compiler will convert .c extension file to a.exe(for window users) and a.out(for mac users) which out computer's server can understand.

> **problem** write a code to find the area of a square by giving its side.

```c
#include <stdio.h>

int main()
{
    int side;

    printf("enter the side of a square for calculating area: ");
    scanf("%d", &side);
    printf("the area of sqaure of side %d is %d", side, side * side);
    return 0;
}
```

there we go!!!

> CODE FOR FINDING THE AREA OF CIRCLE WHEN RADIUS IS GIVEN BY USER

```c
#include <stdio.h>

int main()
{
    float radius;
    float pi = 3.14;

    printf("enter the radius of a circle for calculating area: ");
    scanf("%f", &radius);
    printf("the area of circle of radius %f is %f", radius , pi*(radius*radius) );
    return 0;
}
```
yeahh youhh nailed it dude!

---
## INSTRUCTIONS 
these are statement in a program .
 
### TYPE DECLARATION STATEMENT 

declare the variable before using it. 

```c
int a = 12;
```

mtlb first time aap jab apni file mai koi variable introduce krte hai toh use declare krna pdta hai jisme hm uski type btate hai ki is variable mai hm konsa data store krenge

here declaration is `int` `float` `char` before a variable. 
 
you can't double declare a variable. 
means jab ek variable ko first time declare krte hai toh uski starting mai kuch keywords lgate hai pr jab hme us variable mai kuch update krna ho toh hm use redeclare nhi krenge just variable ko woh value assign krenge like :-

```c
int a = 12;
a = 16;
```

mtlb jb hmne first time a ko declare kiya toh uski value 12 thi firr hmne us value ko update krke uski value 16 krdi.

you can't use a variable befor declaration.

```c
int x = 12 + y;
int y = 18;
```
this code will give you an error as complier reads the file line by line and in the first line it will get an undefined variable y and can't give the value of y at that moment.

```c
int x , y , z ;
x = y = z = 4 ;
```
another way of declaring more than 1 variable at a time and then assigning them a value.

```c
int x = y = z = 4;
```
this will give an error kyuki aap ek sathh declare krke un variable ko use nhi kr skte 

---
### ARITHMETIC INSTRUCTIONS

A kind of mathematical operations.

`a + b` here `a` and `b` are operand 1 and operand 2 respectively. and `+` is the operator.

> operands are the variable jispe operation perform hota hai whereas operators are the symbols which helps in operation by doing a particular calculations or work.


```c
x = a + b * c % d
```

this is an arithematic instruction where the term written in the right hand side contains methametical operations and called as RHS where as x is in the left hand side which will stores the output of the given instruction. 

> LHS must contain only a single variable.

---

there are some main operators in c language.

`+` , `-` , `*` , `/` , `%`.

where 

- `+` stands for addition.
- `-` stands for subtraction.
- `/` stands for division.
- `*` stands for multiplication.
- `=` stands for assigning operator.
- `%` stands for modular which means remainder.

    -  ` 15%2` will give an output `1`. when we divide 15 by 2 the remainder is 1.

    -  **it doesn't work on float values**
---

#### SOME VALID AND INVALID OPERATION INSTRUCTIONS :-

|VALID| INVALID|
|:----:|:----:|
|a = b + c | a + b = c|
|a = b * c |a = bc|
|a = b / c|a = b ^ c|

> use `pow(x,y) for x to the power y.

---

#### TYPES OF CONVERSION

- `int` op `int` -> `int`
- `int` op `float` -> `float`
- `float` op `float` -> `float`
---

LET'S TAKE AN EXAMPLE:- 
1. `x = 1.99999` CONVERT IT INTO AN INTEGER VALUE.

```c
#include<stdio.h>
#include<math.h>

int a = (int) 1.99999 ; 
printf("%d \n" , a);
return 0;
```

the output will be `1` and c compiler doesn't do round off. it generally removes the digits after points.

--- 
#### OPERATOR PRECEDENCE

`*` , `/` , `%` > `+` , `-` > `=`

IF THERE WILL BE ANY OPERATION LIKE `a = 2 + 4 * 6`
then the value of a will be `26` as the high preference operator between `+` and `*` is `*`. so `4 * 6` = `24` and `2 + 24` = `26`.

---
if there comes a time when the operators used in an instructions are of same precedence the we have to perform a process called `ASSOCIATIVITY`. 

which means perform the calculations from left side to right side.

for example:-
```c
int a = 4 * 3 / 6 * 2;
```
the value of a will be `4` as `4 * 3` = `12` and `12 / 6` = `2` and `2 * 2` = `4`.

--- 
### CONTROL INSTRUCTIONS 

the instructions which are responsible for the control of code are called control instructions.

these are of some types.

- #### SEQUENCE INSTRUCTIONS 

    The instructions which flows line by line are called sequence instructions.

    for example:- 

    ```c
    #include<stdio.h>
    int main (){
        int a = 13;
        printf("%d" , a);
        return 0;
    }
    ```
    the above instructions works one by one or you can say in a sequence.

- #### DECISION CONTROL

    THE if-else condition comes under decision control instructions. discussed after some time.

- ### LOOP CONTROL 

    Loops comes under the loop control instructions. if we need to perform a specific task multiple times then, not writting them manually one by one we make a loop for them. don't worry! will discuss this also in detail after sometime.

- #### CASE CONTROL

    different from decision control but somehow some. will discuss in detail (switch-case method)

## OPERATORS

operators are some symbols which performs specific tasks.

- ### ARITHMETIC OPERATORS
    
    THESE TYPES OF OPERATORS WE HAVE ALREADY DISCUSSED ABOVE IN DETAIL.

    `+` , `-` , `*` , `/` , `%`

- ### RELATIONAL OPERATORS

    they describe the relation between two operators.

    - `==` stands for equal to which checks the equality between 2 terms. for examples:-

        ```c
        a === 13;
        ```
        this statement will check if the value of a is equals to 13 or not and returns true or false .

    - `!=` stands for not equals to. for example:-

        ```c
        a != 5;
        ```
        this will check if the value of a is not equals to 5. if yes then returns 1 and if no then returns 0.

    - `>` stands for greater then. same as the greater then sign in maths.

    - `<` stands for less than. same as the less than sign in maths.

    - `>=` stands for greater then or equals to. for example :-

        ```c
        a >= 5;
        ```
        this will check if the value of a is greater then 5 or equals to 5, returns `1 and 0` for `true and false`.

    - `<=` stands for less than or equals to. for example :-
        
        ```c
        a <= 5;
        ```
        this will check if the value of a is less then 5 or equals to 5, returns `1 or 0` for `true and false`.

- ### LOGICAL OPERATORS

    - `&&` stands for `AND OPERATOR`. when there are two statements and when we need to check if both the statements are true or not then we use and operator between these two. if both statements are true then the output will be 1 outherwise it will give a 0. for example:-

        ```c
        4 != 5 && 5 > 4;
        ```
        the output of this statement will be 1(true) as both the statements are true.

    - `||` stands for `OR OPERATOR`. when there are two statements and when we need to check if one of them is true or not. in this condition we use and operator which checks if any one or both of the statements are true or not. for example:-

        ```c
        4 != 3 || 4 < 3;
        ```

        this will give an output `1` as first statement is true among the both.

        ```c
        4 != 3 || 4 > 3;
        ```
        this will also give an output `1` as both the statements are true and the condition of getting a true is if one of them is true or both are true.

    - `!` stands for `not operator`. if the value is true then make it false and if it is false make it true. examples are:-

        ```c
        !(3 > 4)
        ```
        in this condition statement the term `3 > 4` is false and we have used a not operator before this condition then it will get an output `1` as true.

        > it we need to flip the output then we use a not operator.



- ### ASSIGNMENT OPERATORS

    - `=` stands for equals to. for assigning a value to a variable. example:- `a = 2`

    - `+=` stands for plus equals to which generally adds the given value to the past value of the variable. example:- 
        ```c
        #include<stdio.h>
        int main(){
            int a = 2;
            a += 4;
            return 0
        }
        ```

        the past value assigned to a is 2 and when we use `a +=4` then 4 will be added to the past value of a which is 2 and assign the new value to the variable i.e. 6. so the new value of a is 6.

    - `-=` stands for minus equals to which is mostly same as += operator but it subtracts the given value from the original value and save the new value to the variable. example:-

        ```c
        #include<stdio.h>
        int main(){
            int a = 10;
            a -= 4;
            return 0
        }                   // new value of a = 6
        ```
        
    - `*=` stands for multiply equals to which multiply the given value to the assigned value of the variable and then change the value of that variable to the resultant value. example:-

        ```c
        #include<stdio.h>
        int main(){
            int a = 10;
            a *= 4;
            return 0
        }                       //new value of a = 40.
        ```

    - `/=` stands for divide equals to which divide the original value from the given value and assign the new value to the variable. example:-

        ```c
        #include<stdio.h>
        int main(){
            int a = 12;
            a /= 4;
            return 0
        }                       //new value of a = 3.
        ```

    - `%=` stands for modulus equals to which generally find the remainder after dividing the assigned value with the given value and assign the variable the remainder.

        ```c
        #include<stdio.h>
        int main(){
            int a = 10;
            a %= 4;
            return 0
        }                       //new value of a = 2.
        ```


- ### BITWISE OPERATORS

- ### TERNARY OPERATORS

    I think you willn't understand it now; come after you cover if else conditional statement.

    ```c
    condition ? do something if true : do something if false;
    ```

    for example :-

    ```c
    #include<stdio.h>

    int main(){
        int marks = 98;

        marks > 90 ? printf("great job!") : printf("try harder...");
    }
    ```

---
### OPERATOR PRECEDENCE

|PRIORITY|OPERATOR|
|:----:|:----:|
|1|!|
|2|* , / , %|
|3|+ , -|
|4|< , <= , > , >=|
|5|== , !=|
|6|&&|
|7| OR OPERATOR |
|8|=|

---
### WRITE A PROGRAM TO FIND THE AVERAGE OF 3 VARIABLES

```c
#include<stdio.h>

int main(){
    int num1 ;
    int num2 ;
    int num3 ;
    printf("enter the first number :");
    scanf("%d" , &num1);
    printf("enter the second number :");
    scanf("%d" , &num2);
    printf("enter the third number :");
    scanf("%d" , &num3);

    printf("the mean of the given data is %d" , (num1+num2+num3)/3);
    return 0;
}
```

##  CONDITIONAL STATEMENT 

generally there are two type of conditional statements:-

### IF STATEMENT 

```c
if(condition here ){
    //do something is true
};
```

if the given condition meets then the statement written in the if block will exicute.

---
### IF - ELSE STATEMENT

```c
if(condition here ){
    //do something is true
}
else{
    //do something id false
};
```

if the written condition found to be true then the statement written in the if block will run otherwise the condition written in the else block will exicute.

example:-

```c
#include<stdio.h>

int main(){

    int age ;
    printf("enter your age :");
    scanf("%d", &age);

    if(age >= 18){
        printf("you are an adult \n");
        printf("you can vote \n");
        printf("you can drive also! \n");
    }else{
        printf("you are not an adult \n");
    };
    return 0;
}
```
if there in only one statement in your excecution code then you can write it without brackets. 

```c
#include<stdio.h>

int main(){
    int a = 12;
    if(a > 10) printf("you can apply");
    else printf("you can't apply");
}
```

but it is not good for a good programmer you should always use curley brackets.

---

### ELSE-IF STATEMENT

if there is more than one condition to check then there you need to use else-if condition statement

```c
if(condition1){
    //do something if condition1 is true
}
else if(condition2){
    //do something when condition2 is true
}
else{
    //do something if all conditions are false
};
```
you can add multiple else-if statement in between if and else.

if the first condition is false only then it will check the next condition. means the condition will be check from top to bottom, if any condition found to be true then all the conditions statement written bellow will be ignored.

example:-
```c
#include<stdio.h>

int main(){
    int marks = 98;

    if(marks > 90){
        printf("you scored A \n");
    }
    else if(marks > 80){
        printf("you scored B \n");
    }
    else if(marks > 70){
        printf("you scored C \n");
    }
    else if(marks > 60){
        printf("you scored D \n");
    }
    else{
        printf("you scored A \n");
    }

}
```

---

if you want to print output for more then one condition then you need to use if statement more than once.

> REMAINDER :- you will understand the ternary operator now.

### SWITCH STATEMENT

```c
switch(number){
    case C1: //do something
        break;
    case C2: //do something
        break;
    default: // do something
}
```
example:-

```c
#include<stdio.h>

int main(){

    int day;
    printf("enter a number (1-7) :");
    scanf("%d", &day);

    switch (day){
    case 1: printf("Monday \n");
        break;
    case 2: printf("Tuesday \n");
        break;
    case 3: printf("Wednesday \n");
        break;
    case 4: printf("Thursday \n");
        break;
    case 5: printf("Friday \n");
        break;
    case 6: printf("Saturday \n");
        break;
    case 7: printf("Sunday \n");
        break;
    default: printf("enter a valid number (1-7)");
    }
}
```

agr hr case ke baad break nahi lgaya tohh jis case mai condition satisfy horhi h us case ke baad sare cases k switch automatically on hojaynge.

- cases can be in any order.
- nested switch (switch inside a switch) is allowed.

---
### WRITE A CODE TO CHECK IF THE GIVEN CHARACTER IS AN UPPERCASE CHARACTER OR A LOWERCASE CHARACTER.

```c
#include<stdio.h>

int main(){
    char character;
    printf("enter a character: ");
    scanf("%c", &character);

    if(character>= 'A' && character<= 'Z'){
        printf("uppercase \n");
    }
    else if(character>= 'a' && character<= 'z'){
        printf("lowercase \n");
    }else{
        printf("not a english letter");
    };
}
```
---

### WRITE A CODE TO CHECK IF A NUMBER IS AN ARMSTRONG NUMBER OR NOT.

---

## LOOP CONTROL INSTRUCTIONS

if there is a condition when we need to repeat a particular code for a multiple times. to save the time we use loops.

there are three types of loops:-

1. **for loop**
2. **while loop**
3. **do-while loop**

---
### FOR LOOP IN C LANGUAGE

```c
for(initialisation ; condition ; updation){
    // do some work here
};
```
- the work of initialisation statement is to initial the loop. here we create a variable and give its starting position from where it should start. `int i = 0` 

2:50:02