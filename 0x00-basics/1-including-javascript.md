# Including Javascript

There are two main ways of adding Javascript to HTML:  

<ul>
    <li>Internal Javascript</li>
    <li>External Javascript</li>
</ul>

## Internal Javascript  

Here,JavaScript is written inside a `<script> `tag within the `HTML` file

```HTML
<!doctype html>
<html lang="en>
    <head>
        <meta charset="UTF-8"/>
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Document</title>
    </head>
    <body>
        h1>JavaScript</h1>
    <script>
      console.log("Hello,");
      console.log("JavaScript is good")
    </script>
    </body>
</html>
```
Placing the scripts at the bottom of the `<body>  ` improves the display speed; because script interpretation slows down the display  

## External Javascript

Here , the Javascript file is stored in a separate file name .js and linked to the `HTML` document using the `<script>` tag with a source attribute.

``` HTML
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <script src="MAIN.js"></script>
  </head>
  <body>
    <h1>Externa Javascript file</h1>
  </body>
</html>
```
 app.js

 ``` javascript
 console.log("This is an external Javascript file");
 console.log("Javascript is fun");
 ```

## Optimizing script loading

JavaScript can block page rendering if not loaded correctly.

The browser parses out `HTML` code line by line and when it comes across a resource that needs to be downloaded to the page e.g. an image, it sendsa request to the server to download this resource

However, when it comes across the script tags to download   Javascript, it stops until the Javascript has beem downloaded, it then executes this Javascript has been downloaded and then continues parsing the `HTML`.

This can end up hurting perfomance

To improve perfomance,use:

### 1. `defer` keyword

<ul> 
    <li>This ensures that scripts are loaded after the HTML is fully loaded.<li>   <li>Example:</li>
 </ul>

``` HTML
    <script src="main.js" defer></script>
```

### 2. `async` keyword

<ul> 
    <li>Loads scripts asynchronously and runs them as soon as they are downloaded.<li>   <li>May execute JavaScript out of order.</li>
 </ul>

``` HTML
    <script src="main.js" async></script>
```

### 3. The script tag at the end of the page.

<ul> <li>Put the script tag at the very end of the page before the closing body tag.</li></ul>

``` HTML
...
    <script src="main.js"></script>
</body>
</html>
```


Avoid using the async keyword unless you are absolutely sure that it fits your needs, stick to the defer keyword or using the script tag at the end of the HTML document before the closing body tag.
    
