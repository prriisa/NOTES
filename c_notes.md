# C NOTES

## VARIABLE
- variables are case sensitive.
- 1st character should be an `alphabet` or `_`.
-  no comma / blank space allowed.
- No other symbol other than '_'.

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