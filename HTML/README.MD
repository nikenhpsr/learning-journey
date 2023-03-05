# HTML Learning Journal

## Table of Contents

- [HTML Basics](#html-basics)
    - [HTML page structure](#html-page-structures)
    - [Tags vs elements](#tags-vs-elements)
    - [Attributes](#attributes)
    - [Case insensitive](#case-insensitives)
    -  [White space](#white-space)
- [The document heading](#the-document-heading)
    - [The title tag](#the-title-tag)
    - [The script tag](#the-script-tag)
    - [The noscript tag](#the-noscript-tag)
    - [The link tag](#the-link-tag)
    - [The style tag](#the-style-tag)
    - [The base tag](#the-base-tag)
    - [The meta tag](#the-meta-tag)
- [The document body](#the-document-body)
    - [Block elements vs inline elements](#block-elements-vs-inline-elements)
- Tags that interact with text
    - The p tag
    - The span tag
    - The br tag
    - The heading tags
    - The strong tag
    - The em tag
        - Quotes
    - Horizontal line
    - Code blocks
    - Lists
    - Other text tags
- Links
- Container tags and page structure HTML
    - Container tags
        - article
        - section
        - div
    - Tags related to page
        -  nav
        - aside
        - header
        - main
        - footer
- Forms
    - The input tag
        - Email
        - Password
        - Numbers
        - Hidden field
        - Setting a default value
    -  Form submit
    -  Form validation
        - Set fields as required
        - Enforce a specific format
    - Other fields
        - File uploads
        - Buttons
        - Radio buttons
        - Checkboxes
        - Date and time
        - Color picker
        - Range
        - Telephone
        - URL
    - The textarea tag
    - The select tag
- Tables
    - The table tag
    - Rows
    - Column headers
    - The table content
    - Span columns and rows
    - Row headings
    - More tags to organize the table
    - Table caption
- Multimedia tags: audio and video
    - The audio tag
    - The video tag
- iframes
    - Srcdoc
    - Sandbox
    - Allow
    - Referrer
- Images
    - The figure tag
    - Responsive images using srcset
    - The picture tag
- Accessibility
    - Use semantic HTML
    - Use alt attributes for images
    - Use the role attribute
    - Use the tabindex attribute
    - Use the aria attributes
        - aria-label
        - aria-labelledby
        - aria-describedby
        - Use aria-hidden to hide content

## Introduction

It will be brief since there is nothing much abot HTML. Hope it can help you to learn.

## HTML Basics

### HTML Page Structures

Let’s make an example of a proper HTML page.

Things start with the Document Type Declaration (aka doctype), a way to tell the browser this is an HTML page, and which version of HTML we are using.

Modern HTML uses this doctype:
```
<!DOCTYPE html>
```
Then we have the html element, which has an opening and closing tag:
```
<!DOCTYPE html>
<html>
  ...
</html>
```
Most tags come in pairs with an opening tag and a closing tag. The closing tag is written the same as the opening tag, but with a /:
```
<sometag>some content</sometag>
```
There are a few self-closing tags, which means they don’t need a separate closing tag as they don’t contain anything in them.The html starting tag is used at the beginning of the document, right after the document type declaration. The html ending tag is the last thing present in an HTML document.

Inside the html element we have 2 elements: head and body:
```
<!DOCTYPE html>
<html>
  <head>
    ...
  </head>
  <body>
    ...
  </body>
</html>
```
Inside head we will have tags that are essential to creating a web page, like the title, the metadata, and internal or external CSS and JavaScript. Mostly things that do not directly appear on the page, but only help the browser (or bots like the Google search bot) display it properly.

### Tags vs elements
I might use the tag or element term in the book meaning the same thing, except if I explicitly mention starting tag or ending tag.

### Attributes
The starting tag of an element can have special snippets of information we can attach, called attributes.

Attributes have the key="value" syntax:
```
<p class="a-class">A paragraph of text</p>
```
You can also use single quotes, but using double quotes in HTML is a nice convention.

We can have many of them:
```
<p class="a-class" id="an-id">A paragraph of text</p>
```
and some attributes are boolean, meaning you only need the key:
```
<script defer src="file.js"></script>
```
The class and id attributes are two of the most common you will find used.They have a special meaning, and they are useful both in CSS and JavaScript.

The difference between the two is that an id is unique in the context of a web page; it cannot be duplicated. Classes, on the other hand, can appear multiple times on multiple elements. Plus, an id is just one value. class can hold multiple values, separated by a space:
```
<p class="a-class another-class">A paragraph of text</p>
```
It’s common to use the dash - to separate words in a class value, but it’s just a convention.

### Case insensitive
HTML is case insensitive. Tags can be written in all caps, or lowercase. In the early days, caps were the norm. Today lowercase is the norm. It is a convention.

You usually write like this:
```
<p>A paragraph of text</p>
```
not like this:
```
<P>A paragraph of text</P>
```
### White Space
Pretty important. In HTML, even if you add multiple white spaces into a line, it’s collapsed by the browser’s CSS engine.

For example the rendering of this paragraph
```
<p>A paragraph of text</p>
```
is the same as this:
```
<p>A paragraph of text     </p>
```
and the same as this:
```
<p>


  A paragraph of text



</p>
```
Using the white-space CSS property you can change how things behave. You can find more information on how CSS processes white space in the CSS Spec

I’d say use the syntax that makes things visually more organized and easier to read, but you can use any syntax you like.

I typically favor
```
<p>A paragraph of text</p>
```
or
```
<p>
  A paragraph of text
</p>
```
Nested tags should be indented with 2 or 4 characters, depending on your preference:
```
<body>
  <p>A paragraph of text</p>
  <ul>
    <li>A list item</li>
  </ul>
</body>
```
Note: this “white space is not relevant” feature means that if you want to add additional space, it can make you pretty mad. I suggest you use CSS to make more space when needed.

Note: in special cases, you can use the ```&nbsp;``` HTML entity (an acronym that means non-breaking space) - more on HTML entities later on. I think this should not be abused. CSS is always preferred to alter the visual presentation.

## The Document Heading
The head tag contains special tags that define the document properties. It’s always written before the body tag, right after the opening html tag:
```
<!DOCTYPE html>
<html>
  <head>
    ...
  </head>
  ...
</html>
```
We never use attributes on this tag. And we don’t write content in it. It’s just a container for other tags. Inside it we can have a wide variety of tags, depending on what you need to do:

- title
- script
- noscript
- link
- style
- base
- meta

### The Title Tag
The title tag determines the page title. The title is displayed in the browser, and it’s especially important as it’s one of the key factors for Search Engine Optimization (SEO).

### The Script Tag

This tag is used to add JavaScript into the page. You can include it inline, using an opening tag, the JavaScript code and then the closing tag:
```
<script>
  ..some JS
</script>
```
Or you can load an external JavaScript file by using the src attribute:
```
<script src="file.js"></script>
```
The type attribute by default is set to text/javascript, so it’s completely optional.

There is something pretty important to know about this tag. Sometimes this tag is used at the bottom of the page, just before the closing </body> tag. Why? For performance reasons.

Loading scripts by default blocks the rendering of the page until the script is parsed and loaded. By putting it at the bottom of the page, the script is loaded and executed after the whole page is already parsed and loaded, giving a better experience to the user over keeping it in the head tag.

My opinion is that this is now bad practice. Let script live in the head tag.

In modern JavaScript we have an alternative this is more performant than keeping the script at the bottom of the page — the defer attribute. This is an example that loads a file.js file, relative to the current URL:
```
<script defer src="file.js"></script>
```
This is the scenario that triggers the faster path to a fast-loading page, and fast-loading JavaScript.

> Note: the async attribute is similar, but in my opinion a worse option than defer. In more detail, on page https://flaviocopes.com/javascript-async-defer/

### The Noscript Tag
This tag is used to detect when scripts are disabled in the browser.

> Note: users can choose to disable JavaScript scripts in the browser settings. Or the browser might not support them by default.

It is used differently depending on whether it’s put in the document head or in the document body.

We’re talking about the document head now, so let’s first introduce this usage. In this case, the noscript tag can only contain other tags:

1. link tags
2. style tags
3. meta tags

to alter the resources served by the page, or the meta information, if scripts are disabled.

In this example I set an element with the no-script-alert class to display if scripts are disabled, as it was display: none by default:
```
<!DOCTYPE html>
<html>
  <head>
    ...
    <noscript>
      <style>
        .no-script-alert {
          display: block;
        }
      </style>
    </noscript>

    ...
  </head>
  ...
</html>
```
Let’s solve the other case: if put in the body, it can contain content, like paragraphs and other tags, which are rendered in the UI.

### The Link Tag
The link tag is used to set relationships between a document and other resources. It’s mainly used to link an external CSS file to be loaded. This element has no closing tag.

Usage:
```
<!DOCTYPE html>
<html>
  <head>
    ...
    <link href="file.css" rel="stylesheet" />
    ...
  </head>
  ...
</html>
```
The media attribute allows the loading of different stylesheets depending on the device capabilities:
```
<link href="file.css" media="screen" rel="stylesheet" />
<link href="print.css" media="print" rel="stylesheet" />
```
We can also link to resources other than stylesheets. For example we can associate an RSS feed using
```
<link rel="alternate" type="application/rss+xml" href="/index.xml" />
```
Or we can associate a favicon using:
```
<link
  rel="apple-touch-icon"
  sizes="180x180"
  href="/assets/apple-touch-icon.png"
/>

<link
  rel="icon"
  type="image/png"
  sizes="32x32"
  href="/assets/favicon-32x32.png"
/>

<link
  rel="icon"
  type="image/png"
  sizes="16x16"
  href="/assets/favicon-16x16.png"
/>
```
This tag was also used for multi-page content, to indicate the previous and next page using rel="prev" and rel="next". Mostly for Google. As of 2019, Google announced it does not use this tag any more because it can find the correct page structure without it.

### The Style Tag
This tag can be used to add styles into the document, rather than loading an external stylesheet.

Usage:
```
<style>
  .some-css {
  }
</style>
```
As with the link tag, you can use the media attribute to use that CSS only on the specified medium:
```
<style media="print">
  .some-css {
  }
</style>
```
### The Base Tag
This tag is used to set a base URL for all relative URLs contained in the page.
```
<!DOCTYPE html>
<html>
  <head>
    ...
    <base href="https://flaviocopes.com/" />
    ...
  </head>
  ...
</html>
```
### The Meta Tag
Meta tags perform a variety of tasks and they are very, very important. Especially for SEO.vmeta elements only have the starting tag. The most basic one is the description meta tag:
```
<meta name="description" content="A nice page" />
```
This might be used by Google to generate the page description in its result pages, if it finds it better describes the page than the on-page content (don’t ask me how).

The charset meta tag is used to set the page character encoding. utf-8 in most cases:
```
<meta charset="utf-8" />
```
The robots meta tag instructs the Search Engine bots whether to index a page or not:
```
<meta name="robots" content="noindex" />
```
Or if they should follow links or not:
```
<meta name="robots" content="nofollow" />
```
You can set nofollow on individual links, too. This is how you can set nofollow globally.

You can combine them:
```
<meta name="robots" content="noindex, nofollow" />
```
The default behavior is index, follow.

You can use other properties, including nosnippet, noarchive, noimageindex and more.

You can also just tell Google instead of targeting all search engines:
```
<meta name="googlebot" content="noindex, nofollow" />
```
And other search engines might have their own meta tag, too.

Speaking of which, we can tell Google to disable some features. This prevents the translate functionality in the search engine results:
```
<meta name="google" content="notranslate" />
```

The viewport meta tag is used to tell the browser to set the page width based on the device width.
```
<meta name="viewport" content="width=device-width, initial-scale=1" />
```
Another rather popular meta tag is the *http-equiv="refresh"* one. This line tells the browser to wait 3 seconds, then redirect to that other page:
```
<meta
  http-equiv="refresh"
  content="3;url=http://flaviocopes.com/another-page"
/>
```
Using 0 instead of 3 will redirect as soon as possible.

This is not a full reference; Other less-used meta tags exist. After this document heading introduction, we can start diving into the document body.

## The Document Body

After the closing head tag, we can only have one thing in an HTML document: the body element.
```
<!DOCTYPE html>
<html>
  <head>
    ...
  </head>
  <body>
    ...
  </body>
</html>
```

Just like the head and html tags, we can only have one body tag in one page. Inside the body tag we have all the tags that define the content of the page. Technically, the start and ending tags are optional. But I consider it a good practice to add them. Just for clarity.

### Block elements vs inline elements
Visual elements, the ones defined in the page body, can be generally classified in 2 categories:

- block elements (p, div, heading elements, lists and list items, …)
- inline elements (a, span, img, …)

What is the difference?

Block elements, when positioned in the page, do not allow other elements next to them. To the left, or to the right.

Inline elements instead can sit next to other inline elements.

The difference also lies in the visual properties we can edit using CSS. We can alter the width/height, margin, padding and border of block elements. We can’t do that for inline elements.

> Note that using CSS we can change the default for each element, setting a p tag to be inline, for example, or a span to be a block element.

Another difference is that inline elements can be contained in block elements. The reverse is not true.

Some block elements can contain other block elements, but it depends. The p tag for example does not allow such option.

## References

- [Atomic Design](https://atomicdesign.bradfrost.com/) - Brad Frost
- [A free guide to learn HTML and CSS](http://marksheet.io)
- [Code Guide: Standards for developing flexible, durable, and sustainable HTML and CSS](http://mdo.github.io/code-guide/) - Mark Otto
- [Dive Into HTML5](http://diveinto.html5doctor.com) - Mark Pilgrim ([PDF](http://mislav.net/2011/10/dive-into-html5/))
- [freeCodeCamp HTML Handbook](https://www.freecodecamp.org/news/the-html-handbook/)
- [HTML5 For Web Designers](http://html5forwebdesigners.com) - Jeremy Keith
- [HTML and CSS: Design and Build Websites](https://www.amazon.com/HTML-CSS-Design-Build-Websites/dp/1118008189) - Jon Duckett
- [HTML Best Practices](https://github.com/hail2u/html-best-practices) - hail2u
- [HTML Canvas Deep Dive](http://joshondesign.com/p/books/canvasdeepdive/toc.html) - Josh Marinacci
- [HTML5 Canvas](https://www.oreilly.com/library/view/html5-canvas/9781449308032/ch01.html) - Steve Fulton, Jeff Fulton
- [HTML5 Canvas Notes for Professionals](https://goalkicker.com/HTML5CanvasBook/) - Compiled from StackOverflow documentation
- [htmldog.com](https://htmldog.com/guides/) - Beginner's to Advanced Guide
- [Interneting is Hard (But it Doesn't Have to Be)](https://www.internetingishard.com) - Oliver James
- [Practical Series: A website template](https://practicalseries.com/1001-webdevelopment/) - Michael Gledhill (HTML)
- [Pro HTML5 Programming](https://web.archive.org/web/20181215200026/http://apress.jensimmons.com/v5/pro-html5-programming/ch0.html) - Jen Simmons, Chris O'Connor, Dylan Wooters, Peter Lubbers
- [Resilient Web Design](https://resilientwebdesign.com/#Resilientweb%20design) - Jeremy Keith
- [Responsive Web Design with HTML5 and CSS: Build future-proof responsive websites using the latest HTML5 and CSS techniques](https://www.amazon.com/Responsive-Web-Design-HTML5-CSS-dp-180324271X/dp/180324271X/ref=dp_ob_title_bk) - Ben Frain
- [RTL Styling 101](https://rtlstyling.com) - Ahmad Shadeed
- [The HTML Handbook](https://flaviocopes.com/page/html-handbook/) - Flavio Copes (PDF, EPUB, Kindle) *(email address requested)*