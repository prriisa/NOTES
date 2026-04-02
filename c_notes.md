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

- condition means kya condition satisfy honi chahiye `i` ki taki loop run kre. or jab woh condition meet nahi hogi tohh loop rukjaega. `i<=5`

- updation mtlb har baar jab loop chle uske baad `i` ki value mai kya changes aane chahiye. `i++`

let's understand with an example:-

```c
for(let i = 0; i<=5; i++){
    printf("hello world\n");
}
```

in this code, the code starts with `i = 0` mtlb jb hmne code start kiya toh jo hmne ek random variable liya hai hmne uska naam i rkhdiya then us variable ko declare krke uski value assign krni 0 ke equal. then for loop mai condition check hogi or is loop ki condition hai `i<=5` mtlb i ki value less than or equal to 5 honi chahiye tbhi condition true hogi or loop run krega or jo loop k andr printf ki statement run hogi then runn hone k baad i ki value update hogi +1 se as `i++` is written in the updation part, and i ki value aab 1 hojaegi then yeh condition check hona print hona repeat hoga jbtk condition false nhi ho jati and output will be:-

```c
hello world
hello world
hello world
hello world
hello world
hello world
```
> here `i` variable is also called iterator / counter.

---
### print the numbers from 0 to 10.

```c
#include<stdio.h>

int main(){
    for(int i = 0; i<=10; i++){
        printf("%d \n" , i);
    };
}
```
here the output will be;

```c
0 
1 
2
3
4
5
6
7
8
9
10
```
---

### INCREMENT OPERATORS

- `i++` - (pre-increment) - use then increase

    - mtlb i ki value ko phle use krlo then uski value mai 1 increase krdo. example:-

        ```c
        #include<stdio.h>

        int main(){
            int i = 1;
            printf("%d \n" , i++);
            printf("%d" , i);
        }
        ```
        is statement mai hmne phle i ki value assign krayi = 1 and then i++ print kraya mtlb phle i ki original value print hojaegi or i ki original value mai 1 add hoajega or jb hm next time i variable ko use krenge to hme 2 milega. toh mtlb is code ka output hoga:-

        ```c
        1
        2
        ```

- `++i` - (post-increment) - increase then use

    - this operator first increase the value of the variable by one and then use that increased value.

        ```c
        #include<stdio.h>

        int main(){
            int i = 1;
            printf("%d \n" , ++i);
            printf("%d" , i);
        }
        ```
        the output of this code will be 
        ```c
        2
        2
        ```

- `i--` - (pre-decrement) - decrease then use

    - this operator is same as i++ bss usme +1 hojata tha variable mai or isme -1 hota hai.

        ```c
        #include<stdio.h>

        int main(){
            int i = 5;
            printf("%d \n" , i--);
            printf("%d" , i);
        }
        ```
        output will be=
        ```c
        5
        4
        ```

- `--i`- (post-decrement)  use then decrease

    - this operator first decrease the value of the variable and then uses the decreased value.

        ```c
        #include<stdio.h>

        int main(){
            int i = 5;
            printf("%d \n" , --i);
            printf("%d" , i);
        }
        ```

        output will be 
        ```c
        4
        4
        ```
---

>the value of i can be a float or a character value.

---
### PRINT CHARACTER FROM 'a' TO 'z'
```c
#include<stdio.h>
int main(){
for(char ch = 'a'; ch <='z' ; ch++){
    printf("%c \n", ch);
};
}
```
> characters itself have ASCII value means all characters have interger value like 'a' can also be written as `int(97)` so we can handle them as an integer.

---
### INFINITE LOOP

WHEN the loop does't know the ending then it becomes an infinite loop and wo tbtk chalta rhega jbtk computer ki memory full na ho jae.

```c
#include<stdio.h>
int main(){
for(int i = 1; ; i++){
    printf("%d \n", i);
};
}
```

---
### WHILE LOOP

```c
while(condition){
    //do some work
};
```
while loop means jbtk condition false na hojae jbtk andr ki statement ko chalate rho.

like jabtk sham na hojae tbtk dodte rho.

```c
#include<stdio.h>

int main(){
    int i = 0;
    while(i <=5){
        printf("%d \n" , i);
        i++;
    };
}
```
while loop mai hme variable loop ke bahr karna pdta hai or condition statement () mai likhte hai or{} mai woh statement likhte hai jo hme us condition ke meet hone pr krwani hai. and code ke end mai hi updation statement likhte hai compiler code ko line by line run krta hai or puri statement ke baad variable ki value update krdeta hai.

---
### print the value from 0 to n when the value of n is given by the user.

```c
#include<stdio.h>

int main(){
    int num = 0;
    int i;
    printf("enter any number :");
    scanf("%d" , &i);

    while (num<=i)
    {
        printf("%d \n" , num);
        num++;
    }
}
```
---
### DO-WHILE LOOP

```c
do{
    //do some work
}while(condition);
```

yeh generally while loop jesa hi hota hai pr while loop mai phle condition check hoti hai phir agr condition meet hogi tohh loop k andr ki statement chlegi nhi toh nhi chlegi. pr do-while loop mai ek baar statement run hoti hai or firr condition check hoti hai or is time agr ocndition meet hui toh run hogi nhi toh loop bus ek baar run hoke rh jaega.

```c
#include<stdio.h>

int main(){
    int num = 0;
    do
    {
        printf("%d" , num);
        num++;
    } while (num >=2);
    
}
```
output will be
`0`

---
### print the sum of first n natural numbers where the given value of n = 4

from for loop

```c
#include<stdio.h>

int main(){
    int n = 4;
    int sum = 0;
    for(int i = 1; i <= n; i++){
        sum += i;
    }
    printf("sum = %d \n" , sum);
}
```
from while loop
```c
#include<stdio.h>

int main(){
    int n = 4;
    int i = 1;
    int sum = 0;
    while(i<=n){
        sum += i;
        i++;
    }
    printf("sum = %d \n" , sum);
}
```
---
### PRINT THE TABLE OF THE NUMBER WHOSE VALUE IS GIVEN BY USER.

```c
#include<stdio.h>

int main(){
    int n;
    printf("enter any number :");
    scanf("%d" , &n);

    for (int i = 1 ; i <=10 ; i++){
        printf("%d x %d = %d \n" , n , i , n*i );
    }
}
```

output:

```c
enter any number :2
2 x 1 = 2 
2 x 2 = 4
2 x 3 = 6
2 x 4 = 8
2 x 5 = 10
2 x 6 = 12
2 x 7 = 14
2 x 8 = 16
2 x 9 = 18
2 x 10 = 20
```
---
## BREAK STATEMENT
break statement is used to exit the loop.
```c
#include<stdio.h>

int main(){
    for (int i = 1 ; i <=5 ; i++){
        if(i==3){
            break;
        };
        printf("%d \n" , i);
    }
}
```
is code mai i ki value =5 hone tak loop chalna tha pr ek if condition lagi hui hai ki agr i ki value 3 ke equal aae toh loop ko break krdo. mtlb is code ka output aaega

```c
1
2
```
---
### KEEP TAKING THE INPUT FROM THE USER UNTIL THE VALUE IS AN EVEN NUMBER.
```c
#include<stdio.h>

int main(){
    int n;
    do
    {
        printf("enter a number :");
        scanf("%d" , &n);
        
        if(n%2 == 0){
            printf("end");
            break;
        }
    } while (1);
}
```
---
### CONTINUE STATEMENT

CONTINUE statement ka mtlb us particular variable ki value p aage ke code ko skip kro or loop ko aage continue kro.

---
### PRINT THE NUMBER FROM 0 TO 10 EXCEPT 4

```c
#include<stdio.h>

int main(){
    for(int i = 1; i<=10; i++){
        if(i==4) continue;
        printf("%d \n" , i);
    }
    return 0 ;
}
```
---
### PRINT ALL THE ODD NUMBERS BETWEEN 5 TO 50
```c
#include<stdio.h>

int main(){
    for(int i = 5; i<=50; i++){
        if(i%2==0) continue;
        printf("%d \n" , i);
    }
    return 0 ;
}
```
---
### PRINT THE FACTORIAL OF THE NUMBER n.
```c
#include<stdio.h>

int main(){
    int n;
    printf("enter a number :");
    scanf("%d" , &n);

    int factorial = 1;

    for(int i = n; i>=1; i--){
        printf("%d" , i);

        if(i!=1) printf("x");
        factorial*=i;
    }
    printf(" = %d", factorial);
    return 0 ;
}
```
IS CODE KO SIRF CHOTE NUMBERS KE SATH HI TEST KRSKTE HAI KYUKI FACTORIAL KI VALUE EXPONENTIALLY BADHTI HAI OR ITNI BDI VALUE FIRR `INT` MAI STORE NHI HO PAEGI OR RETURN M OUTPUT MILEGA 0.

---
## FUNCTION AND RECURSION

A function is a block of code that performs a particular task.

takes arguement => do work => give result.

it can be used multiple times.

**there are three steps to create a function:-**
- **function prototype/ function declaration:-**
    ```c
    void printHello();
    ```
    the name of the function can be anything means it is a variable.

- **function defination:-**
    ```c
    void printHello(){
        printf("hello world \n");
    };
    ```
- **function call**
    ```c
    #include<stdio.h>

    int main(){
        printHello();
        return 0;
    }
    ```
all together:-

```c
#include<stdio.h>
void printHello();      //function declaration

int main(){
    printHello();       //function call
    return 0;
}

void printHello(){
    printf("hello world \n");       //function defination
};
```
you can call a function multiple times.

---
### PROPERTIES

- excecution always starts from main.
- a function gets called directly or indirectly form main.
- there will be multiple functions in a program.
---
### TYPES OF FUNCTIONS

funtions are of two types:-
- user defined function

    - they are declared and defined by user.
    - example:- `printHello();` that we have created above.
- library functions

    - they are the inbuilt function which are built in C.
    - example:- `printf();` `scanf();`
---
### PASSING ARGUEMENTS

function can take values & give some value.

- the values taken - parameters
- gives a value - arguments/ return value

---
```c
void printHello();     //1

void printTable(int n);         //2

int sum(int a, int b);         //3
```
1. in the first code; function na koi arguement leta hai na hi koi value return krta hai. 
2. 2nd mai; function parameters leta hai koi value leta hai pr return nhi krta.
3. and the last one takes parameter and return integer value.

> main function mai hm jo variable use krte hai wohh hota hai main variable or arguement or jo variable jo hm function defination ke time use krte hai use khte hai parameters.

### difference between PARAMETERS AND ARGUEMENTS

|ARGUEMENTS|PARAMETERS|
|:----:|:----:|
|values that are passed in function call|values in function declaration and defination|
|used to send value|used to receive value|
|actual parameter|formal parameters|

### NOTE

- function can only return one value at a time.
- changes in parameters in function don't change the value in calling function. because a copy of the arguement is passed to the function.

    - mtlb agr hm main function ke kisi variable ko user defined function mai change krenge yah update krenge tohh wo sirf function ke andr hi valid rhega main function mai us value mai koi change nhi aaega.
---
### USE LIBRARY FUNCTION TO CALCULATE THE SQUARE OF A GIVEN NUMBER.

```c
#include<stdio.h>
#include<math.h>
int numSquare(int num);      //function declaration

int main(){
    int num;
    printf("enter a number :");
    scanf("%d" , &num);
    numSquare(num);       //function call
    return 0;
}

int numSquare(int num){
    int square;
    square = pow(num, 2);
    printf("the square of %d is %d" , num , square);       //function defination
};
```
---
### WRITE A FUNCTION TO CALCULATE THE AREA OF SQUARE CIRCLE AND A RECTANGLE.

```c
#include<stdio.h>
#include<math.h>

int areaSquare(int side);
int areaCircle(int radius);
int areaRectangle(int length, int breadth);

int main(){
    int side, radius, length, breadth;
    char type;
    printf("enter 's' for square; 'c' for circle; 'r' for rectangle :");
    scanf("%c", &type);

    switch(type){
        case 's':printf("enter the value of side :");
                scanf("%d" , &side);
                areaSquare(side);
                break;

        case 'c':printf("enter the radius of the circle :");
                scanf("%d" , &radius);
                areaCircle(radius);
                break;

        case 'r':printf("enter the length of the rectangle");
                scanf("%d" , &length);
                printf("enter the breadth of the rectangle");
                scanf("%d" , &breadth);
                areaRectangle(length, breadth);
                break;

        default: printf("enter a valid alphabet.");
    }
}

int areaSquare(int side){
    int area = side*side;
    printf("the area of given square of side %d is %d", side , area);
}

int areaRectangle(int length, int breadth){
    int area = length*breadth;
    printf("the area of the rectangle of given length %d and breadth %d is %d" , length , breadth , area);
}

int areaCircle(int radius){
    float area = (3.14)*(pow(radius, 2));
    printf("the area of the circle of radius %d is %f", radius , area);
}
```
---
## RECURSION

when a function calls itself, it is called recursion.

> the work which can be done by function can also be done by recursion and vice versa. but sometimes we need to write a huge line of codes to excecute a program but from recursion it can be done in a simpler way.

for example:-
```c
#include<stdio.h>

void printHW(int count);

int main(){
    int count;
    printf("enter a number :");
    scanf("%d" , &count);
    printHW(count);
    return 0;
}

void printHW(int count){
    if(count == 0) return;
    printf("hello world \n");
    printHW(count-1);
}
```
---
### FIND THE SUM OF FIRST N NATURAL NUMBERS USING RESURSION.

```c
#include<stdio.h>

int sum(int n);

int main(){
    printf("%d" , sum(5));
    return 0;
}

int sum(int n){
    if(n == 1) return 1;
    int sumNm1 = sum(n-1);
    int sumN = sumNm1 + n;
    return sumN;
}
```
---
### FIND THE FACTORIAL OF N.

```c
#include<stdio.h>

int factorial(int n);

int main(){
    int num;
    printf("enter a number :");
    scanf("%d" , &num);
    printf("%d" , factorial(num));

    return 0;
}

int factorial(int n){
    if (n == 1) return 1;
    return factorial(n-1)*n;
}
```
---
### PROPERTIES OF RECURSION

- recursion can sometimes give the most simple solution.
- `base case` is the condition which stops recursion.
- iteration has infinite loop & recursion has `stack overflow`.
---
### PRINT THE FIBONACCI SERIES FOR FIRST NTH TERM.

**FIBONACCI SERIES IS LIKE `0,1,1,2,3,5,8,13,21...`**

```c
#include<stdio.h>

int fibonacciSeries(int n);

int main(){
    int n;
    printf("enter the position of the last number :");
    scanf("%d" , &n);
    
    for(int i = 0; i <= n ; i++){
        if(i ==n ){
            printf("%d" , fibonacciSeries(i));
        }else{
        printf("%d , " , fibonacciSeries(i));
        }
    }
    return 0;
}

int fibonacciSeries(int n){

    if(n==0) return 0;
    if(n==1) return 1;

    int fibNm1 = fibonacciSeries(n-1);
    int fibNm2 = fibonacciSeries(n-2);
    int fibN = fibNm1+ fibNm2;

    return fibN;
}
```
---
### WRITE A FUNCTION TO FIND THE SUM OF DIGITS OF A NUMBER.

```c
#include<stdio.h>
int sum(int num);

int main(){
    int num;
    printf("enter a number to calculate its sum. :");
    scanf("%d" , &num);
    printf("%d" , sum(num));
}
int sum(int num){
    if(num == 0) return 0;

    return num%10 + sum(num/10);
}
```
---
## PRINTERS

A variable that stores the memory address of the different(another) variable.

```c
int age = 22;
int *ptr = &age;
int _age = *ptr;
```
> `*` stands for value at address

>`&` stands for address of operator.
---
### DECLARING POINTERS

```c
int *ptr;       //this will store address of integer value
char *ptr;      //this will store address of character value
float *ptr;     //this will store address of float value
```
---
### FORMAT SPECIFIER

```c
printf("%p" , &age);        //address of age will be printed
printf("%p" , ptr);     //address of variable stored in ptr will be printed
printf("%p" , &ptr);        //address of ptr will be printed
```
> for getting address as an output we need to use `%p` which is used to save hexa-decimal values.
`%u` is used to get the output in integer form, which is mainly used for unsigned integers.

```c
printf("%d" , age);         //this will print the value of age
printf("%d" , *ptr);        //this will print the value of the variable stored in ptr
printf("%d" , *(&age));     //first & gives the address of age, after that * will print the value at that address means the value of age will be printed here
```
---
### POINTER TO POINTER

A variable that stores the memory address of another pointer.

**syntax**

```c
int **pptr;
char **pptr;
float **pptr;
```
---
## POINTERS IN FUNCTION CALL

1. **CALL BY VALUE**
    - we pass value of variable as arguement.

    ```c
    #include<stdio.h>

    int sum(int n);

    int main(){
        int number = 15;
        sum(number);
        printf("number is %d \n" , number);
    }

    int sum(int n){
        n = n*n;
        printf("sum is %d \n" , n);
    }
    ```
    output will be 
    ```c
    sum is 225 
    number is 15 
    ```
    means call by value mai hm reference share nhi krte jis se hmare original variable pai function ka koi effect nhi pdta.

2. **CALL BY REFERENCE**
    - we pass address of variable as argument.

    ```c
    #include<stdio.h>

    int sum(int *n);

    int main(){
        int number = 15;
        sum(number);
        printf("number is %d \n" , number);
    }

    int sum(int *n){
        *n = (*n)*(*n);
        printf("sum is %d \n" , *n);
    }
    ```
    now the output will be
    ```c
    sum is 225 
    number is 225
    ```
---
### SWAP 2 NUMBERS, A & B

```c
#include <stdio.h>

int swap(int *a, int *b);

int main()
{
    int a = 3, b = 5;
    swap(&a, &b);
    printf("x = %d & y = %d \n", a, b);

    return 0;
}

int swap(int *a, int *b)
{
    int t = *a;
    *a = *b;
    *b = t;
    printf("a = %d & b = %d \n", *a, *b);
}
```
---
## ARRAYS

collection of similar data types stored at contiguous memory locations.

mtlb it is a kind of collection of similar data types.

```c
int marks[] = {12, 42, 15};
```

### SYNTAX

```c
int marks[3];           //this array store 3 integer value every block containing 4 bytes storage.
char name[10];          // this array stores 10 characters
float price[2];         // this array stores 2 float values
```

> base indexing = 0
if there are 3 values in an array then first number has an index value 0, second one has index value 1, and 2 for the third one.
---
### INPUT & OUTPUT

```c
scanf("%d" , &marks[0]);        //this will take an input and store it on the 0th index of marks array.
printf("%d" , marks[0]);        //this will print the 0th value of marks
```
---
### WRITE A PROGRAM TO ENTER THE PRICE OF 3 ITEMS & PRINT THEIR FINAL COST WITH GST.

```c
#include<stdio.h>

int main(){
    int price[3];

    printf("enter the price of 1st product :");
    scanf("%d" , &price[0]);

    printf("enter the price of 2nd product :");
    scanf("%d" , &price[1]);

    printf("enter the price of 3rd product :");
    scanf("%d" , &price[2]);

    int totalPrice = price[0] + price[1] + price[2];
    float gst = 0.18 * totalPrice;

    printf("your total price with GST = %f" , totalPrice + gst);
}
```
---
### INITIALIZATION OF ARRAY
```c
int marks[] = {97 ,77 ,79};

int marks[3] = {97, 77, 79};
```
---
### POINTER ARITHMETIC

pointer can be incremented & decremented

**CASE-1**
```c
int age = 22;
int *ptr = &age;
ptr++;
```
is code ka simple mtlb ye h ki hmne phle age ki value 22 assign ki then uske address ko pointer variable me store kraya; agr hm ptr++ yah ptr-- mai se koi function perform krte hai toh pointer variable usme jo variable hai uski value mai +1 store nhi krti h blki uski jo variable ki jo memory location hai usko 4 bytes se increase yah decrease kr deti h...let's understand with an example:-
```c
#include<stdio.h>

int main(){
    int age = 22;
    int *ptr = &age;
    printf("%u \n" , ptr);          //prints the current memory location of variable age

    ptr++;
    printf("%u \n" , ptr);          //prints the increased memory location of age by 4 bytes

    ptr--;
    printf("%u \n" , ptr);          //prints the decreased memory location of age by 4 bytes

}
```
then the output will be;

```c
6422296 
6422300 
6422296
```

**CASE-2**
```c
float price = 20.00;
float *ptr = &price;
ptr++;
```
yebhi same waise hi work krega integer ki trh because both have 4 bytes of memory storage value
**CASE-3**
```c
char star = '*';
char *ptr = &star;
ptr++;
```
in this case the memory get increased by 1 as character stores 1 byte of memory.

---
- we can also sbutract one pointer from another.
- we can also compare 2 pointers of same type.
---
### ARRAY IS A POINTER 
```c
int *ptr = %arr[0];
        OR
int *ptr = arr;
```
BOTH ARE SAME AS THE ARRAY ITSELF IS A POINTER WHICH LOCATED THE ADDRES OF ITS FIRST INDEX VALUE AS A POINTER.

---
### TRAVERSE AN ARRAY
```c
int aadhar[10];
int *ptr = &aadhar[0];
```
---
### print every value of array using pointer.

```c
#include<stdio.h>

int main(){
    int aadhar[5];

    int *ptr = &aadhar[0];
    for(int i = 0 ; i < 10 ; i++){
        printf("%d index : ", i);
        scanf("%d" , (ptr+i));
    
    }

    for(int i = 0; i<10; i++){
        printf("%d index = %d ", i , *(ptr+i));
    }
    return 0 ;
}
```
---
### ARRAYS AS FUNCTION ARGUEMENT

#### FUNCTION DECLARATTION
```c
void printNumbers(int arr[] , int n);
``` 
OR
```c
void printNumbers(int *arr , int n);
```
#### FUNCTION CALL
```c
printNumbers(arr , n);
```
let's understand with an example:-
```c
#include<stdio.h>

void printNumbers(int arr[] , int n);

int main(){
    int arr[] = {2, 4, 6, 8, 10};
    printNumbers(arr , 4);

    return 0;
}

void printNumbers(int arr[] , int n){
    for(int i = 0 ; i<=n ; i++){
        printf("%d \t" , arr[i]);
    }
}
```
output will be:- `2      4       6       8       10`
---
### MULTIDIMENSIONAL ARRAYS
#### 2D ARRAYS
```c
int arr[][] = {{1,2},{3,4}};
```
**TO ACCESS**
```c
arr[0][0];      //1
arr[0][1];      //2
arr[1][0];      //3
arr[1][1];      //4
```
---
#### WRITE A FUNCTION TO PRINT THE ODD NUMBERS IN AN ARRAY.

```c
#include<stdio.h>

int countOdd(int arr[] , int n);

int main(){
    int arr[] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
    countOdd(arr , 10);
}

int countOdd(int arr[] , int n){
    for(int i = 0 ; i<= n ; i++){
        if(arr[i] % 2 == 0){
            continue;
        }else{
            printf("%d \t" , arr[i]);
        }
    }
}
```
---
#### WRITE A FUNCTION TO REVERSE AN ARRAY

```c
#include<stdio.h>

int reverseArr(int arr[] , int n);
void printArr(int arr[] , int n);

int main(){
    int arr[] = {1,2,3,4,5,6};
    reverseArr(arr , 6);
    printArr(arr , 6);
    return 0;
}

int reverseArr(int arr[] , int n){
    for(int i = 0 ; i < (n/2) ; i++){
        int firstVal = arr[i];
        int secondVal = arr[n-i-1];

        arr[i] = secondVal;
        arr[n-i-1] = firstVal;
    }
}

void printArr(int arr[] , int n){
    for(int i = 0 ; i< n ; i++){
        printf("%d" , arr[i]);
    }
}
```
> this shows that a array only uses call by reference as when we make any changes to an array by making functions then the changes will also reflects in the original array. so keep in mind before using.

---
#### WRITE THE FUNCTION TO PRINT N NUMBER OF FIBONACCI SERIES.

```c
#include<stdio.h>

int fibonacci(int n);

int main(){
    int length;
    printf("enter the length of fibonacci series you want :");
    scanf("%d" , &length);
    fibonacci(length);

    return 0;
}

int fibonacci(int n){
    int arr[n];
    for(int i = 0 ; i<=n ; i++){
        if(i == 0){
            arr[0] = 0 ; 
        }
        else if(i == 1){
            arr[1] = 1;
        }else{
            arr[i] = arr[i-1] + arr[i-2];
        }
        printf("the value at index %d is %d \n" , i , arr[i]);
    }
}
```
---
#### CREATE A 2D ARRAY, STORING THE TABLES OF 2,3 

```c
#include<stdio.h>

int main(){
    int table[2][10];
    for(int i = 0; i<=9 ; i++){
        table[0][i] = 2*(i+1);
        table[1][i] = 3*(i+1);
    }
    for(int i = 0 ; i <= 1 ; i++){
        for(int j = 0 ; j <= 9 ; j++){
            printf("%d \n" ,table[i][j] );
        }
    }
}
```
---
## STRINGS
a character array terminated by a '\0'(null character)

null character denotes string termination

example:-
```c
char name[] = {'p','r','i','y','a','\0'};
char class[] = {'B','t','e','c','h','\0'};
```
### INITIALISING STRINGS
```c
char name[] = {'P','R','I','Y','A'};
char name[] = {"priya"};
```

every letter occupy a particular memory location and in a string all characters have continuous memory location;

|P|R|I|Y|A|\O|
|:----:|:----:|:----:|:----:|:----:|:----:|
2000|2001|2002|2003|2004|2005|
---
### create a string firstName and lastName to store details of user & print all the characters using a loop.

```c
#include<stdio.h>

int printName(char name[]);

int main(){
    char firstName[10], lastName[10];
    int countName = 0 , countLastName = 0;

    printf("enter your first name :");
    scanf("%s" , &firstName);

    printf("enter your last name :");
    scanf("%s" , &lastName);

    printName(firstName);
    printf("\n");
    printName(lastName);
}

int printName(char name[]){
    for(int i = 0; name[i] != '\0'; i++){
        printf("%c \n" , name[i]);
    }
}
```
---
### STRING FORMAT SPECIFIER

`%s`

when ever we need to use a string character for printing or taking input or using it into another funtion we uses a new format specifier which is `%s` which knows the string values and is used in string operations.

```c
char name[] = "priya";
printf("%s" , name);
```
---
### DRAWBACK OF SCANF FOR STRING VALUES.

`scanf()` cannot input multi-word strings with spaces. like;

when you input a value in scanf() using `&s` like `it is a rainy day` it will only scan the first word of the paragraph. i.e. `it` and store it to the given variable and you won't be able to store more words in it.

HERE; 
`gets()` & `puts()` come into the picture.

- `gets(str)` => inout a strings (even multiword).(dangerous & outdated)

- `fgets(str , n , file)` => stops when n-1 char input or new line is entered.

- `puts(str)` => output a string.

```c
#include <stdio.h>

int main(){
    char paragraph[100] ; 
    printf("enter your paragraph :");
    gets(paragraph);
    puts(paragraph);
}
```
this will take input for variable named paragraph and then print it back on the screen.

but as we know `gets()` is dangerous as it is unable to count the string length entered and because of this it leads to get **hacked** by hackers. so we use `fgets()` in place of it.

here, we need to enter the string name; variable maximum length; and file, currently enter `stdin` in its place, will discuss about it later.

example:-

```c
#include <stdio.h>

int main(){
    char paragraph[100] ; 
    printf("enter your paragraph :");
    fgets(paragraph , 100 , stdin);
    puts(paragraph);
}
```
---
### STRING USING POINTERS
```c
char *str = Hello world";
```
store string in memory & the assigned address is stored in the char pointer `str`

```c
char *str = "hello World";      //can be reinitialized

char str[] = "hello world";     //cannot be reinitialized
```
---
### STANDARD LIBRARY FUNCTIONS
`<string.h>`

1. **strlen(str)**

    count number of characters excluding `\0`
    ```c
    #include<stdio.h>
    #include<string.h>

    int main(){
        char *name = "priya";
        int length = strlen(name);
        printf("%d" , length);
    }
    ```

2. **strcpy(newStr , oldStr)**

    copies value of old string to new string

    ```c
    #include<stdio.h>
    #include<string.h>

    int main(){
        char *name = "priya";
        int length = strlen(name);
        printf("%d" , length);
    }
    ```


3. **strcat(firstStr , secStr)**

    this will add 2 strings.

    ```c
    #include<stdio.h>
    #include<string.h>

    int main(){
        char oldStr[100] = "oldStr";
        char newStr[100] = "newStr";
        strcat(newStr , oldStr);
        printf(newStr);
    }
    ```
    before concatination keep in mind that the first string should have the space to add the second one in it.

4. **strcmp(firstStr , secStr)**

    compare 2 strings & return a value.
    - 0 -> string equal
    - positive -> first > second (ASCII)
    - negative -> first < second (ASCII)

    ```c
    #include<stdio.h>
    #include<string.h>

    int main(){
        char firstStr[] = "Apple";
        char secStr[] = "Banana";
        printf("%d" , strcmp(firstStr , secStr));
    }
    ```
---

### TAKE A STRING INPUT FROM THE USER USING %c.

```c
#include<stdio.h>
#include<string.h>

int main(){
    char str[100];
    char ch;
    int i = 0;
    printf("enter your string :");

    while(ch != '\n'){
        scanf("%c" , &ch);
        str[i] = ch;
        i++;
    }
    str[i] = '\0';
    printf(str);
}
```
---
### FIND THE SALTED FORM OF A PASSWORD ENTERED BY USER IF THE SALT IS "123" & ADDED AT THE END.

```c
#include<stdio.h>
#include<string.h>

int main(){
    char password[50];
    char *salt = "123";
    printf("enter your password :");
    scanf("%s" , &password);
    strcat(password , salt);
    printf("final password: %s", password);   
}
```
---
### WRITE A FUNCTION NAMED SLICE, WHICH TAKES A STRING & RETURNS A SLICED STRING FROM INPUT n TO m.

```c
#include<stdio.h>
#include<string.h>

void slice(char string[], int start , int end);

int main(){
    char string[100];
    int start , end ;
    printf("enter your string you want to slice :");
    fgets(string , 100 , stdin);

    printf("enter the starting slice index :");
    scanf("%d" , &start);
    printf("enter the ending slice index :");
    scanf("%d" , &end);

    slice(string , start , end);
}

void slice(char string[] , int start , int end){
    char newstr[100];
    int j = 0;
    for(int i = start; i <= end ; i++ , j++){
        newstr[j] = string[i];
    }
    newstr[j] = '\0';
    puts(newstr);
}
```
---
### WRITE THE FUNCTION TO COUNT THE OCCURRENCE OF VOWELS IN A STRING.

```c
#include<stdio.h>
#include<string.h>

int countVowels(char string[]);

int main(){
    char str[100];

    printf("enter your string :");
    fgets(str , 100 , stdin);

    countVowels(str);
}

int countVowels(char string[]){
    int count = 0;
    for(int i = 0 ; string[i] != '\0' ; i++){
        if(string[i] == 'a' || string[i] == 'A' || string[i] == 'e' || string[i] == 'E' || string[i] == 'i' || string[i] == 'I' || string[i] == 'o' || string[i] == 'O' || string[i] == 'u' || string[i] == 'U'){
            count++;
        }
    }
    printf("the total number of vowels present in your string is : %d" , count);
}
```
---
### CHECK IF A GIVEN CHARACTER IS PRESENT IN A STRING OR NOT.

```c
#include<stdio.h>
#include<string.h>

void findChar(char string[] , int ch);

int main(){
    char str[100] , ch;
    printf("enter your string :");
    fgets(str , 100 , stdin);
    printf("enter the character you want to find :");
    scanf("%c" , &ch);

    findChar(str , ch);
}

void findChar( char string[] , int ch){
    int charCount = 0;
    for(int i = 0 ; string[i] != '\0' ; i++){
        if(string[i] == ch){
            charCount++;
        }
    }
    if(charCount > 0){
        printf("given character is present in the string %d times" , charCount);
    }else{
        printf("character is NOT present.");
    }
}
```
## STRUCTURES

a collection of values of different data types

example:-
```
name(string)
class(number)
roll no(number)
```

### SYNTAX

```c
struct student{
    char name[100];
    int roll;
    float cgpa;
};
```
> struct is a userdefined data type.

how to use that data type
```c
struct student s1;
s1.cgpa = 7.5;
```
means this will create a structure of student named s1 whose cgpa is 7.5

```c
#include<stdio.h>
#include<string.h>

struct student{
    char name[100];
    int roll;
    float cgpa;
};

int main(){
    struct student s1;
    strcpy(s1.name , "Priya Sharma");
    s1.roll = 110040;
    s1.cgpa = 9.1;

    printf("student name = %s \n" , s1.name);
    printf("student roll number = %d \n" , s1.roll);
    printf("student cgpa = %f \n" , s1.cgpa);

    return 0;
}
```
---
### STRUCTURES IN MEMORY

memory alloted for the above structure is like:-

name|roll|cgpa|
|:----:|:----:|:----:|
2010|2110|2114|

as `char` takes 1 bit storage, `int` takes 4 bit storage.

structures are stores in contiguous memory location
---
### BENIFITS OF STRUCTURES

1. saves user from creating too many variable.
2. good data management or organisation.
---
### ARRAY OF STRUCTURES

```c
struct student ECE[100];
struct student COE[100];
struct student IT[100];
```
TO ACCESS

```c
IT[0].roll = 200;
IT[0].cgpa = 7.6;
```
---
### INITIALIZING STRUCTURES

```c
struct student s1 = {"priya" , 110040 , 9.2};       //enter the data in sequence.

struct student s2 = {"rajat" , 122506 , 7.4};

struct student s3 = {0};        //this means every value of s3 is null
```
---
### POINTER TO STRUCTURES

```c
struct student s1;
struct student *ptr;
ptr = &s1;
```
here first we have created a student structure for s1 and then created a pointer structure and then give the address of s1 to that pointer.
---
### ARROW OPERATOR

`(*ptr).code` <---> `ptr->code`

```c
(*ptr).roll         //complicated way of writing
ptr->roll           //arrow operator for simple coding
```
---
### PASSING STRUCTURE TO FUNCTION

```c
void printInfo(struct student s1);
```
---

## typedef KEYWORD

used to create `alias` for data types (nicknames).

```c
typeded struct ComputerEngineeringStudent{
    int roll;
    float cgpa;
    char name;
} coe;
```
in the above code the structure is created named ComputerEngineeringStudent whose nickname is coe.

we can call it as coe while adding information or using that structure.

```c
coe student1;
```
this will create a student 1 for that structure given above.

example:-
```c
#include<stdio.h>
#include<string.h>

typedef struct computerEngineeringStudent{
    int roll;
    float cgpa;
    char name[100];
} coe;

int main(){
    coe s1;
    s1.roll = 110040;
    strcpy(s1.name , "priya");

    printf("student name is %s \n" , s1.name);
    
    return 0;
}
```
---
## FILE IO
FILE - container in a storage device to store data.

- ram is `volatile`
- contents are lost when program terminates
- files are used to persist the data
---
### OPERATION ON FILES
- `CREATE` a file
- `OPEN` a file
- `CLOSE` a file
- `READ` from a file
- `WRITE` in a file
---
### TYPES OF FILES
1. **TEXT FILES** -> TEXUAL DATA
    example:- `.txt`, `.c`
2. **BINARY FILES** -> BINARY DATA
    example:- `.exe`, `.mp3`, `.jpg`
---
### FILE POINTER 

FILE is a (hidden) structure that needs to be created for opening a file. A FILE `ptr` that points to this structure & is used to access the file.

```c
FILE *fptr;
```

9:29:34
