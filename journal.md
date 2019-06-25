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

`<a href> <img> <li>`, basically anything within a <> is considered a tag.  Some tags require attributes, while it's optional for others.  An example of ones that require an attribute is `<a href="www.google.com">Google!</a>` - In this `href`is the attribute but it is required, otherwise `<a>` is a useless tag.  The same goes for `<img src="image link">` - the `src` is required to define where your picture is.  

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

