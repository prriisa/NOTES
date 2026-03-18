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
