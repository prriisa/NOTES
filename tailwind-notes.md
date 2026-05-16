# TAILWIND NOTES

AFTER BEFORE
CSS VARIABLES
TAILWIND CSS

---

```css
h1::after{
    content:"";
    font-size: 25px;
    color:black;
}
```
h1 ke end me after ka content show hone lgega. is is a psudo element. yeh ek imaginary content hai.

if we add any content in case of div then it will be added in the after or before the content of that div. not after or before the div...

---

## CSS VARIABLES

allow you to store specific values like color fonts size in one place and reuse it multiple times.

```css
:root{
    --king:"red";
    --queen:"pink";
}
```

to use 

```css
h1{
    color:var(--king);
}
```

---
## TAILWIND CSS

YOU CAN APPLY MULTIPLE CLASSES TO A SINGLE TAG.

```css
<h1 class="blue flex">hello world</h1>
```

---
way to use tailwind css...

- google tailwind css

- open the first website

- get started

- go to play CDN

copy the script tag and paste it in your html head tag.

---
|properties|tailwind|
|:----:|:----:|
|height| h-20|
|width|w-full|
|display (flex,grid,initial,etc)|flex, grid, initial , none|
|background-color|bg-blue-600
|align-items|items-center
|justify-content|justify-center
|gap|gap-5
|font-size|text-(xl     xs      bs      md      lg      2xl    3xl      6xl     9xl  )  |
|hover|hover:text-black|
position|static      absolute        realtive        absolute        
