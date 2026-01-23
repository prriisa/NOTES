# JAVASCRIPT ADV NOTES

`Document Object Model`
everything you see in your website is a part of DOM.

there are multiple types of notes in a DOM tree. these are:-

1. Element
2. Text
3. Comment
4. Document
5. Attribute

> element can also have children in it whereas, other can't have.

## DOM MANIPULATION

- **selecting by**

    - getElementById

        ```javascript
        let abcd = document.getElementById("abcd");
        ```

    - getElementsByClass

        ```javascript
        let abcd = document.getElementsByClassName("abcd");
        ```
        - after logging, we get an array like structure.

    - quarySelector
        ```javascript
        let abcd = document.quarySelector("abcd");
        ```

    - quarySelectorAll
        ```javascript
        let abcd = document.quarySelectorAll("h1");
        ```

        - It will select the first coming element only.

        - after logging you will get an array like structure.

    > `getElementsByClass` and `quarySelectorAll` exactly returns an `HTML collection` which looks like an array but not generally an array.
    
    - the below thing will only select the lists of even index.

    ```javascript
    document.quarySelector("li:nth-child(2n)");
    ```



- **Text/Content Access**

    - **innerText**

        - if you want to change only Text content.

    ```javascript
    let h1 = document.quarySelector("h1");
    h1.innerText = "hello world"
    ```
    - **textContent**

        - it is same as innerText. but `faster` then innerText and also can tell about hidden elements.

    ```javascript
    let h1 = document.quarySelector("h1");
    h1.textContent = "hello world"
    ```
    - **innerHTML**

        - if you want to add HTML tags, then you can go through it.

    ```javascript
    let h1 = document.quarySelector("h1");
    h1.innerHTML = "<i>hello world</>"
    ```

- **Attribute Manipulation**

inside a tag, everything else written is attribute. for example;
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Document</title>
</head>
<body>
    <h1 id="heading">HELLO</h1>
    <script src="script.js"></script>
</body>
</html>
```
here;

 `html` `lang` `charset` `name` `content` `rel` `href` `id` `src`
 all are attributes.
 
 - 
    - **getAttribute**

    from this , you can get the value of any attribute.
    ```javascript
    let a = document.quarySelector("a");
    console.log(a.getAttribute("href"));
    ```

    another way of getting the value of an attrubiete is like `console.log(img.src)`.

    - **setAttribute**

    from this, you can change the value of any attribute of html file.

    ```javascript
    let a = document.querySelector("a");
    a.setAttribute(name , value);
    ```
    
    - **removeAttribute**
    
    from this, you can remove any attribute.

    ```javascript
    let a = document.quarySelector("a");
    a.removeAttribute("href");
    ```

## DYNAMIC DOM MANIPULTION

- **createElement**
- **appendChild**
- **removeChild**
- **prepend**


with `createElement`, you can create element using javascript.
```javascript
let h1 = document.createElement("h1");
```

but by using only this your element will not be added in your webpage. if you want, then you have to `append` or `prepend` that element.

> append => addes in the end

> prepend => added in starting

```javascript
let h1 = document.createElement("h1");
h1.innerText("hello");
document.body.append(h1);
```
- `append` and `appendChild` are the same. 

- from `removeChild` or `remove`, you can remove any element.

## ADDING STYLE USING JAVASCRIPT

you just need to do a single thing, and that is:
```javascript
h1.style.color = 'red';
```
that simple dude!

### APPLYING A CLASS ON AN ELEMENT
you can `add` any font class on your element.

```javascript
h1.classList.add("<class-name>")
```

you can also `remove` any by-default applied font by doing:

```javascript
h1.classList.remove("<class-name>");
```

if your class is applied then `toggle` will remove it or if the class is not applied then toggle will apply it.

```javascript
h1.classList.toggle("<class-name>");
```
