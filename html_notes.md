# HTML

HYPER TEXT MARKUP LANGUAGE

---

EXTENSION FOR html file is `.html`

---

## BASIC STRUCTURE TAGS

### DOCTYPE

```html
<!DOCTYPE html>
```

doctype hme btata hai ki hmare document konse type ka h... that is html here.

### HTML TAG

after the DOCTYPE we have a html tag. inside the html tag there are 2 sub tags or children of html youh can say,

`<head>` head tag and `<body>` tag

```html
<!DOCTYPE html>
<html>
  <head></head>
  <body></body>
</html>
```

### HEAD TAG

it consists of configuration.

like;

if we add a

```html
<title>FIRST WEB PAGE</title>
```

inside the `<head></head>`

is title tag ki wjh se hmari file ka name hojaega `FIRST WEB PAGE`.

### BODY TAG

it means structure of the main content.

mtlb agr maine isme kuch bhi likhdhiya toh wo hmare web page mai show hone lgega.

---

## TYPES OF TAGS

1. **Normal (Paired tags)**

   mtlb aaise tags jo open or close dono hote hai. example:- `<head></head>`, `<body></body>`, `<html></html>`

2. **Self-closing tags**

   mtlb aaise tags jinhe close krne ki jrurt nhi pdti wohh khudme hi self closing tags hote hai. example:- `<meta>`,

3. **Inline block tags**
4. **Inline tags**
5. **Semantic tags**

---

## BOILER PLATE CODE

just by doing `! + enter` you can get a pre defined boilerplate code of html jisme hmare prerequisteries tags already written hote hai or inko again and again likh ke hmara time waste nhi hota.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

this is boilerplate code.

inside this there is a `<html lang="en">` which means aaki is html file ki language english honi chahiye. here `lang` is an attribute. will discuss it.

here is a `<meta>` tag is a self closing tag and isme kuch properties hai joki hmari basic configurations hoti hai.

here `<meta charset="UTF-8">` , charset is an attribute, attributes are the properties used inside any tag in html. charset

computer understands binary language which are in the form of 0 and 1 and every alphabet of english and any language any symbol there is an ASCII format where value already given to them jis se unhe define kiya jata hai.

full form of ascii = American Standard Code For Information Interchange.

and ASCII jaisa same format hota hai `UTF=8` jo hm hmare html mai use krte hai.

in the next `<meta name="viewport" content="width=device-width, initial-scale=1.0">` there is again a meta tag jisme name = viewport. viewport mtlb jitni bdi hmari screen hai us puri screen mai hme web page dikhe.

second property is content , means hmari web ki width hmare device ki width ke equal hogi. and `initial-scale = 1.0` means hmre web page ka zoom in size by default one hoga.

---

## BASIC STRUCTURE TAGS.

- html
- head
- title
- body
- meta
- link
- style
- script

## TEXT & CONTENT TAGS

- `<h1></h1>`, h2, h3, h4, h5, h6

  pre defined tag used to create headings. these heading are in bold format.

- `<p></p>`

  is tag ka use krke hm normally hmare content ko show kr re hote h.

- `<br>`

  br means break. mtlb agr kisi line ko bich mai se break krke usko next line se continue krwana h tb hm br tag use krte hai.

  it is a self closing tag.

- `<hr>`

  means hme apni file mai ek horizontal line leke aani h toh hm `<hr>` tag use krte hai

  ```html
  <h1>
    hello <br />
    <hr />
    world
  </h1>
  ```

## TEXT FORMATTING TAGS

- `<b></b>` and `<strong></strong>`

  bold

- `<i></i>` and `<em></em>`

  italic

- `<mark></mark>`

  highlight

- `<small></small>`

  make the content small

- `<del></del>`

  line through

- `<sub></sub>`

  subscript. mtlb niche power.

- `<sup></sup>`

  superscript. mtlb upr power.

---

## LINKS & NAVIGATIONS

`<a href = "https://google.com>">opens the google<a>`

agr aapko number dial pad m open krwana hai toh use kro `href = "tel:+916832946563"`

and agr mail krwani hai toh use `href = "mailto:example@gmail.com"`

## MEDIA TAGS

1. `<img>`

   ```html
   <img src="link here" alt="image here" />
   ```

2. `<audio>`

   ```html
   <audio src="" controls></audio>
   ```

3. `<video>`

   ```html
   <video src="" autoplay muted loop></audio>
   ```

4. `<iframe>`
   kisi bhi third party website ki vdo agr hme hmare webpage pe play krni hai toh hm iframe use krte hai.

   youtube ki link mai jgh bhi `watch?` likha ho usko replace krdo `embed` sai

   ```html
   <iframe src="" frameborder="0"></iframe>
   ```

---

## LIST TAGS

- ul => unordered list

- ol => unordered list

- li => list
- dl
- dt
- dd

---

## TABLE TAGS

- `table` => forms a table
- `thead` => table heading
- `tbody` => table body
- `tfoot` => table footer
- `tr` => table rows
- `td` => table data
- `th` => table's heading data
- `caption` =>
- `colgroup` =>
- `col` =>

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <table border="2">
      <caption>
        food items...
      </caption>

      <colgroup>
        <col style="background-color: red;" />
        <col style="background-color: blue;" />
        <col style="background-color: pink;" />
      </colgroup>

      <thead>
        <tr>
          <th>name</th>
          <th>quantity</th>
          <th>price</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>maggie</td>
          <td>10</td>
          <td>15</td>
        </tr>
        <tr>
          <td>lays</td>
          <td>100</td>
          <td>10</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <th colspan="2">total price</th>
          <td>104</td>
        </tr>
      </tfoot>
    </table>
  </body>
</html>
```

---

## FORM TAGS

- `form` => used to create a form

    ```html
    <form></form>
    ```
    
- `input` => used to take input

  ```html
  <input type="text" placeholder="Enter your name" />
  ```

- `textarea` => used to take a big input. 

    ```html
        <label for="review">review</label>
        <textarea name="" id="review" rows="3"></textarea>
    ```

- `button` => usually a button
- `select` => used tos select options
- `option` => used in select tags to make otpions

  ```html
  <select name="" id="">
    <option value="html">html</option>
    <option value="css">css</option>
    <option value="javascript">js</option>
  </select>
  ```

- `optgroup` => agr aapko multiple groups bnane hai options ke tb iska use krte hai.

    ```html
        <select name="" id="">
            <optgroup label="frontend">
                <option value="">html</option>
                <option value="">css</option>
                <option value="">js</option>
            </optgroup>
            <optgroup label="backend">
                <option value="">Nodejs</option>
                <option value="">Expressjs</option>
                <option value="">Mongodb</option>
            </optgroup>
        </select>
    ```

- `label` => creates a label jispe click krne ke baad woh input yah select heighlight ho jata hai

    ```html
    <label for="name">username</label>
    <input id="name" type="text" placeholder="Enter your name"/>
    ```
    label ke `for` attribute and input ki `id` ki same value honi chahiye.

- `fieldset` => yeh kind of ek box bna deta hai jisme hm inputs le skte hai
- `legend` => legends is used to create the heading of the fieldset.
    ```html
      <fieldset>
        <legend>personal details</legend>
        <label for="name">username</label> <br>
        <input id="name" type="text" placeholder="Enter your name" /> <br> <br>
        <label for="email">email</label> <br>
        <input id="email" type="text" placeholder="Enter your email address" /> <br> <br>
        <label for="mobile">mobile no</label> <br>
        <input id="mobile" type="text" placeholder="Enter your mobile no." /> <br> <br>
      </fieldset>
    ```

- `output`

---

- `details`
- `summary`

    ```html
    <details>
        <summary>open me</summary>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestiae, ipsa!</p>
    </details>
    ```
    yeh kind of ek drop down create krta hai jisme summary mai jo likha hai woh phle display hoga or agr hmne uspe click kiya then hmare details mai jokuch written tha woh visible hoga.

--- 
agr kisi tag mai `contenteditable = "true"` krde toh aap website mai hi usko edit krskte ho.
```html
    <h1 contenteditable="true">hello</h1>
```

---
agr kisi tag mai `draggable = "true"` krde toh aap website mai hi usko drag krskte ho.
```html
    <h1 draggable="true">hello</h1>
```

---

## SEMENTIC TAGS

- `header` => top of the webpage
- `main` => main content of the webpage
- `footer` => bottom of the webpage
- `section` => sections inside the main tag
- `article` => article
- `aside` => left section
- `details`
- `summary`
