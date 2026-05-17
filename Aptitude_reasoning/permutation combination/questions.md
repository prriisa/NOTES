# QUESTIONS ON PERMUTATION

`ques` in how many different ways can be the letter of the words BRAIN be arranged

```
BRAIN = 5 letters = 5! = 5 x 4 x 3 x 2 x 1 = 120
```

---
`ques` in how many different ways can the letter of words TITLE be arranged

```
total letters = 5
repeated letters = 2

5!/2! = 60
```

---

`ques` IN how many different ways can the letter of the words LEADING be arranged so that vowels always come together

```
in LEADING we have 3 letter. treat these 3 as a word so now we have 5 different letters to rearrange

= 5! 

and we also can arrange the vowels inside the word, so

5! x 3! = 120 x 6 = 720
```

---

`ques` in how many different ways can the letter of the words CORPORATION be arranged so that the vowels always come together

```
we have 5 vowel here...
OOAIO

and making this a capsule we have 7 letters 
C R P R T N [OOAIO]

and there are also 2R repeating so the combination for this will be 7!/2!

and the combination inside the capsule will be 5!/3! as there are 3O present 

(7! x 5!) / (3! x 2!) = 50400
```

---

`ques` how many 3 digit numbers can be formed with 1, 2, 3, 4, 5 but the numbers must be multiple of 5.


```
the position of ones element is fixed i.e. 5
and the probability of the number that can be in tens place and hundreds place is 5*5 so the ans is 5 x 5 x 1 = 25
```

---

`ques` how many numbers of four digits greater than 2400 can be formed with digits 0 , 1, 2, 3, 4, 5 & 6no digit being repeated in any number?

```
first will calculate the number greater than 3000,

4 x 6 x 5 x 4

= 480
now the number btw 2400-2999

1 x 3 x 5 x 4 = 60

total numbers = 540
```

---

`ques` from the group of 12 men and 10 has to be selected in how many ways can we select 10 men.

```
nCr = (12 x 11) / (2 x 1) = 66
```

---

`ques` from a group of 7 men and 6 women, five persons are to be selected to form a committee. in which there must be 2 women and 3 men.

```
6C2 x 7C3
(6 x 5 x 7 x 6 x 5) /( 2 x 3 x 2 ) = 525
```

---

`ques` from a group of 7 men and 6 women, five persons are to be selected to form a committee so that at least 3 men are there on the committee. in how many ways can it be done.

```
7C3 x 6C2
    +
7C4 x 6C1
    +
7C5 x 6C0

= 

35 x 15 = 525
35 x 6 = 210
21 x 1 = 21

525 + 210 + 21 = 751
```

---

`ques` Out of 7 consonants and 4 vowels, how many words of 3 consonants and 2 vowels can be formed?

```
7C3 x 4C2 = 35 x 6 = 210 x 120 = 25200
```

---

`ques` in a group of 6 boys and 4 girls, four children are to be selected. in how many different ways can they be selected such that at least one should be there?

```
6C1 x 4C3
+
6C2 x 4C2
+
6C3 x 4C1
+
6C4 x 4C0

=

6 x 4 + 15 x 6 + 20 x 4 + 15 x 1 = 209
```

---
