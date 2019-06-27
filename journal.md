# My Learning Journal

This journal is composed of things that I have learned from the Code Fellows 102 class.

## GIT

Commands | Description
-------- | ------------
git clone link | This will clone the repository from github to your local computer
git status | This displays the current status of your files
git add file | This adds a file name to be committed
git add . | This adds all untracked files
git commit -m " " | This commits the file(s) you just added with a message
git push origin master | This pushes to git
git fetch origin | This fetches the current version on git
git pull | This pulls the latest data fetched from git


## HTML

The basic layout of a HTML5 website

```
<!DOCTYPE html>
<html>
    <head>
        <title></title>
    </head>
    <body>
        <header>
            <nav>
            </nav>
        </header>
        <main>
            <section></section>
            <section></section>
        </main>
        <footer>
        </footer>
    </body>
</html>
```

- DOCTYPE sets the type of document and "should" be the only capitalization in your HTML code.
- head contains the collection of metadata for this document.
- title sets the title of the website
- body is the body of your website, think of a piece of paper.  The entire 8.5x11 size is your body
- header typically refers to the top of the website
- nav is a new HTML5 element, typically refers to the navigation bar of a website
- main is where the main content will go, again think of a piece of paper.  The lines on the paper is where your main content goes.
- footer typically refers to the bottom of the website

## Additional notes for HTML

`<a href> <img> <li>`, basically anything within a <> is considered a tag.  Some tags require attributes, while it's optional for others.  An example of ones that require an attribute is `<a href="www.google.com">Google!</a>` - In this `href`is the attribute but it is required, otherwise `<a>` is an anchor tag that's not doing too much.  The same goes for `<img src="image link">` - the `src` is required to define where your picture is.  

Now there are other attributes that aren't required, but can be utilized to specifically label things for CSS optimization later on.  Examples of this could be `<section id="Main-Content"></section>` or `<img id="doggo" src="cutedog.jpg">`.  Assigning the id attribute to these elements makes it so these are unique.

There's also a thing called Parent and Children, basically meaning if there's a tag inside of a tag, it's a Parent/Child.

```
    <section>
        Look at my cute puppy! <img src="cute_dog.png">
        Here are some facts about him!
        <ul>
            <li>He snores!</li>
            <li>He loves to eat!</li>
            <li>He's lazy...</li>
        </ul>
    </section>
```

In this example, `<section>` is a parent of `<img>, <ul> and <li>`.  `<ul>` is a parent of `<li>`.  `<img>` and `<ul>` are siblings, since they reside on the same level.  This is a very important thing to note and key to writing clean and neat code as this will help tremendiously later on when it comes to creating the CSS.  It's much easier to be able to identify the list of dog facts because you can break it down and understand exactly where it sits!


## Cascading Style Sheets

CSS is what styles the sheets, hence the "style" portion in the name.  While you don't *need* an extra file for CSS, meaning that you could write it within your .html file, it's really not recommended.  Biggest reason being is because you could have one file that controls how your entire website looks, and it would be very easy to change one line in there and change the design of your entire website.  But, if you wrote your css within each html file, then you would have to go and change each and every file until everything was updated.  Kinda sucks...

CSS Selector Notes | Description
------------------ | -----------
* | This targets ALL elements on a page
h1, h2, h3 | This would target the `<h1>, <h2>, <h3>` elements on a page
.note | This targets any `class="note"` elements on a page
p.note | This targets any `<p class="note">` elements on a page
#note | This targets any `id="note"` elements on a page
li>a | This targets any `<a>` elements that are a child of an `<li>`
p a | This targets any `<a>` elements that sit within a `<p>`
h1+p | This targets the first `<p>` element after an `<h1>` element
h1~p | If you had two `<p>` elements inside of an `<h1>`, this would apply to both


CSS Color Notes | Description
--------------- | -----------
hex | #123456
rgb | 0, 50, 100
color name | red
opacity | Specify a number between 0.0 & 1.0.  `opacity: 0.1;`
rgba | rgb alpha, same as rgb but applies opacity.  `background-color: rgba(0,50,100,0.1);`
hsl | hue saturation lightness.  Hue is an angle, 0-360.  Saturation is %, 0-100.  Lightness is %, 0-100 (0% - white, 50% normal, 100% - black) `background-color: hsla(0, 100%, 100%, 0.5);`


## JavaScript!

JavaScript is super awesome and allows you to do basically anything you want within your project.  The real trick is just figuring out how to get it to do that one thing...


Arithmetic Operators | Description
-------------------- | -----------
+ | Adds one value to another
- | Subtracts one value from another
/ | Divides two values
* | Multiplies two values
++ | Increased value by one
-- | Subtracts value by one
% | Divides two values and returns the remainder


### Functions!

Functions let you group a series of statements together to perform a specific task.  If different parts of a script repeat the same task, you can reuse the 
function rather than repeating the same set of statements.

`document.write('Hello!');` and `function sayHello() { document.write('Hello!') };` are the same, but the main difference being is that you can now call `sayHello()` 
at any time in your code, instead of writing out `document.write('Hello!');`, so it makes things faster for you later on.  This of course is a very basic example, but with more
complex bits of code, it becomes much easier to run things after you have the shell created.

A better example of "complex" code would be `function getArea(width, height) { return width * height }`, in this bit you are saying that your width and height can be changed
depending on what it is that you insert into your function.  So you can insert `getArea(3, 5)` and this would return 15.  Or you can set the numbers as a var before your function
like `var wallWidth = 3; var wallHeight = 5;` and then do `getArea(wallWidth, wallHeight);` which returns 15 - only difference here is that you've set your wallWidth & wallHeight dependant
to a variable, which you could also change later on as you go.

```
function calculateArea(width, height) {
  var area = width * height;
  return area;
}
var wallOne = calculateArea(3,5);
var wallTwo = calculateArea(8,5);

console.log(wallOne); //This returns 15
console.log(wallTwo); //This returns 40
```