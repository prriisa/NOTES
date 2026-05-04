# SWAP 2 VARIABLES

## 1. SWAP 2 VARIABLE using 3rd VARIABLES

```js
//variavle defination
let a = 15;
let b = 12;
let temp;
console.log(a, b);

// variable swap
temp = a;
a = b;
b = temp;
console.log(a, b);

```

## 2. SWAP 2 VARIABLE WITHOUT USING EXTRA VARIABLE (addition/subtraction)

```js
//variable defination
let a = 30;
let b = 20;
console.log(a, b);

// variable swap
a = a + b;
b = a - b;
a = a - b;
console.log(a, b);
```

## 3. SWAPING VARIABLE VIA (multiplication/division)

```js
//variable defination
let a = 30;
let b = 20;
console.log(a, b);

// variable swap
a = a * b;
b = a / b;
a = a / b;
console.log(a, b);
```

## 4. SWAPING VARIABLE VIA XOR (bitwise operator)

```js
//variable defination
let a = 30;
let b = 20;
console.log(a, b);

// variable swap
a = a ^ b;
b = a ^ b;
a = a ^ b;
console.log(a, b);
```
---
## Initial:
```js
a = 5  (0101)
b = 10 (1010)
```
Now:
```js
a = a ^ b
a = 5 ^ 10 = 15 (1111)
```

Now:
a = 15
b = 10

```js
b = a ^ b
b = 15 ^ 10 //5
```

Now:
a = 15
b = 5

```js
a = a ^ b
a = 15 ^ 5 //10
```

Final:
```js
a = 10
b = 5
```
---