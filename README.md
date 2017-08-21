# Portfolio Instructions

How to create a portfolio website with Bootstrap!

[What is Bootstrap?](http://getbootstrap.com/)

> Bootstrap is a free front-end framework for faster and easier web development
>
> Bootstrap includes HTML and CSS based design templates for typography, forms, buttons, tables, navigation, modals, image carousels and many other, as well as optional JavaScript plugins
>
> Bootstrap also gives you the ability to easily create responsive designs
>
>    **[source](https://www.w3schools.com/bootstrap/bootstrap_get_started.asp)**

[Demo of common Bootstrap website](https://blackrockdigital.github.io/startbootstrap-stylish-portfolio/)

[Info about this template](https://startbootstrap.com/template-overviews/stylish-portfolio/)

[Github repo of this template](https://github.com/BlackrockDigital/startbootstrap-stylish-portfolio)

[How to deploy to Github Pages](https://pages.github.com/)

## Tips

* Think about who you want to view your site (potential employers, freelance opportunities, friends). I know it is tempting to make it flashy with tons of jQuery plugins, but the most important thing when designing your site is to make it EASY for your visitors to access the information they want and navigate around the page.

* Think about the goal for your site and what you want your users to do (read about your story, look at your work/code/writing, contact you). Guide them to taking those actions by making them prominent / easy to find.

* Wireframe what you want your site to look like first!

* Use proper indentation and organize your code. Chances are people will view your source!

* You may use Bootstrap or other CSS frameworks. If you do, you're encouraged to start off using it so that you get an idea of how you want your page to look, and then to gradually remove the Bootstrap in favor of CSS you wrote yourself.

## Inspiration

[How to build a data science portfolio](https://www.dataquest.io/blog/build-a-data-science-portfolio/)

Personal websites from some previous DSI grads:

* http://charlesmrice.com/
* https://michaeljsanders.com/
* https://mummertm.github.io/MarkMummert/
* http://www.datawrites.co/
* http://www.emilyschuch.com/
* http://www.codylaminack.com/
* https://sambozek.github.io/capstone.html#capstone

You can also Google "data scientist portfolio website" for more ideas :)

## Domains (Optional)

If you'd like, you can purchase a domain and then "point" the domain to your Github Pages repo. Here are instructions on how to do so:

https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages/

Recommendation: [Namecheap](https://www.namecheap.com/)

## Resources

* [Font Awesome](http://fontawesome.io/icons/)
* [Google Fonts](https://fonts.google.com/)
* [HTML Validator](https://validator.w3.org/)
* [Favicon](http://www.favicon-generator.org/)
* [Logo Creator](https://www.canva.com/)

## Tricks

1. Open links in new tabs:

```HTML
  <a href="#" target="_blank">HTML Text</a>
```

2. [W3 School Bootstrap Documentation](https://www.w3schools.com/bootstrap/default.asp)

3. Override default bootstrap CSS with `!important`:

  [Order of Specificity](https://css-tricks.com/specifics-on-css-specificity/)

Consider the following:

```HTML
  <p id="thing">Will be RED.</p>
```

With order of specificity in mind, which below will supersede the other?

```CSS
  p {
    color: red !important;
  }
  #thing {
    color: green;
  }
```

`!important` will ignore the rules and supersede id.

4. [Resizing images](https://www.w3schools.com/bootstrap/bootstrap_images.asp)

## HTML (Hyper Text Markup Language)

HTML exists to solve the problem of how a rich document can be expressed in plain text.
That is to say what are the parts of the document, what role does each part serve (e.g. heading, image, list, emphasized text, link etc.), and how do they relate to one another.

HTML expresses the **structure and semantics** of a document in plain text.

### Elements

![Parts of an Element](https://mdn.mozillademos.org/files/9347/grumpy-cat-small.png)

The parts of an HTML document are called **elements** and they are denoted with **tags**.
Tags come at the beginning and end of an element's content.

![Attributes](https://mdn.mozillademos.org/files/9345/grumpy-cat-attribute-small.png)

Extra information about elements can be added using **attributes** which are added to the opening tag.
A ubiquitous element which always needs an attribute is the `a` (for *anchor*) element.
The `a` element creates a link to another location, frequently another page.

We express the structure of an HTML document by nesting.
For example, we can take a paragraph:

```html
<p>The easiest way to learn HTML is to use it!</p>
```

and we can emphasize part of the text using `em` tags:

```html
<p>The easiest way to learn HTML <em>is to use it!</em></p>
```

We can add a link to the word `HTML` that goes to the MDN HTML page (https://developer.mozilla.org/en-US/docs/Web/HTML)

```html
<p>
  The easiest way to learn
  <a href="https://developer.mozilla.org/en-US/docs/Web/HTML">HTML</a>
  <em>is to use it!</em>
</p>
```

Notice the use of whitespace (line-breaks and indentation) here.
Any amount of whitespace is understood as a single space to the browser which lets us spread our content out for readability.

An element can be the child of another element (contained within its parent's tags) but can never straddle another element.

```html
<!-- Don't do this! -->
<p>The easiest way to learn HTML <em>is to use it!</p></em>
```

Similarly, do not omit closing tags.
Every element needs a closing tag (with the exception of **empty elements** which we'll discuss momentarily).

```html
<!-- Also, don't do this! -->
<p>The easiest way to learn HTML <em>is to use it!</em>
```

Browsers are extremely accommodating and so will likely display something but this behavior can't and shouldn't be depended upon.

Because the browser can be uninformatively accommodating, we want to double check our work with an [HTML validator](https://validator.w3.org/).

#### Head

The `head` element holds **metadata** about the document; metadata meaning extra information about the document beyond the content of the document.
One required piece of metadata is the `title` element.
Every page is required to have a title; without one the HTML document is invalid.

The `meta` element declares that the *charset* or set of characters used in this document is **utf-8** which includes most characters from all known human languages.
This is not required but can avoid some problems you might run into if you use special characters.

Other examples of metadata include links to external stylesheets (more later) and scripts to run on the page.

#### Body

The `body` element contains the information actually presented to the user; it represents the content of the document.


#### Headings

The `h1` - `h6` tags are for headings and subheadings.
It's rare to use past 3 or 4.

```html
<h1>I'm most important! There should really only be one of me on a page.</h1>
<h2>I'm still quite important! I'm fine being on the page a few times though</h2>
<h3>I'm pretty common!</h3>
<h4>I'm quite detailed</h4>
<h5>I'm probably deep in a menu</h5>
<h6>Wow, that's very detailed</h6>
```

#### Paragraphs

The `p` tag is used for paragraphs

```html
<p>Not a ton going on here...</p>
```

#### Lists

People love lists.
There are two types of HTML lists, ordered and unordered.

```html
<ol>
  <li>I'm first</li>
  <li>I'm second</li>
  <li>I'm third</li>
</ol>
<ul>
  <li>red</li>
  <li>green</li>
  <li>blue</li>
</ul>
```

#### Images

If there's anything people like more than lists, it's pictures.

Pictures are **empty elements** meaning that they cannot logically have children and so are represented in HTML with a single, self-closing element.
Some people put a slash at the end of empty elements but it is unnecessary.

```html
<img src="" alt="" />
<!-- is the same as -->
<img src="" alt="">
```

Images require two attributes, a `src` with a URL for an image, and an `alt` tag for screen readers and when something breaks and the image doesn't show up.

The url can be any address but generally we want to manage our own assets.

### CSS Rules

CSS styles are a series of **rules** or **rulesets**.
A rule is a combination of a **selector** and a set of **declarations**.

![Anatomy of a CSS Ruleset](https://mdn.mozillademos.org/files/9461/css-declaration-small.png)

## Selector

A selector is a pattern used to match element to which the rule should apply.
As shown this can be an element.
Very commonly we add `class` or `id` attributes to elements mark for targeting by a specific rule.

Selectors can be combined and related and there are many more types of [selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Selectors).

## Declaration

A declaration has two parts, a property and a value to which that property should be set.
In the example above, the property is `color` and the property value is `red`.
There must be a colon separating each property from its property value and a semicolon at the end of the declaration.
By adding just that rule to our CSS and refreshing the page in the browser, we can see the effect of the rule (though you have to scroll past the massive image -- we'll fix that shortly).

### Properties

Like HTML elements, there are tons of css properties and it is impractical to memorize them.
Again we're looking for the 20% that gets us 80% of the way.


#### [Background](https://developer.mozilla.org/en-US/docs/Web/CSS/background)

There is a ton we can do with the background.
Generally we will use a [**hex-triplet**](https://en.wikipedia.org/wiki/Web_colors#Hex_triplet) to describe colors.

## Importing Fonts

Google hosts a massive repository of fonts that can be imported for use on your page.

To add a font:
1. Go to [Google Fonts](https://fonts.google.com/)
2. Click the **+** button next to any font you want to import to your page (as a rule, any more than 3 fonts in a project quickly begins to look disjointed).
3. After selecting 1 or more fonts, click the bar on the bottom that says **1 Family Selected**.
4. Add the provided link element (something like `<link href="https://fonts.googleapis.com/css?family=Fresca" rel="stylesheet">`) to the head of your HTML.
5. Add the provided declaration (something like `font-family: 'Fresca', sans-serif;`) to a CSS rule targeting the elements to which you would like to apply the font.
