# WWWTF?!

## Introduction

This document gives a brief overview of how contemporary frontend web development hangs together, with attention paid to the haphazard ways in which we got here. The intended audience is novices and the baffled.

### Authorial "credentials"

I've been a web developer for more than 10 years, and possess a little ancient knowledge of web time before that. I'm not a web historian, however, and the veracity of this account should be considered to be somewhere between a well-researched history of the web and a bunch of monkeys banging on typewriters.

## In the beginning

The world wide web was kicked off by Tim Berners-Lee in 1990. The initial intent of html was to create a web of linked hypertext documents, specifically research papers. The evolution of the web has largely about taking a system modestly intended for document display and (gradually) turning it into something that can display your facebook wall.

To give you an idea how plain the web initially was, the `<img>` tag wasn't introduced until 1993.

### Standards

It seems shocking now that the early web largely involved making shit up as it went along, but it was comparatively small and the technology developed rapidly. The formation of the W3C as the official web standards body in 1994 sought to remedy the chaos, but defining standards took time, implementing them took more time, and often browsers simply chose not to implement standards, invented ones of their own.

### Your browser history (part one)

This may be wildly boring, but here goes: the first widely used web browser was Mosaic, but it got eclipsed by Netscape around 1995ish. Netscape was in turn eclipsed by Internet Explorer not long after. In this early period browsers often differed in their interpretations of web standards and indeed supported their own markup as they jostled for consumer support. This meant that web site owners either chose which browser to support (leading to a craze of "best viewed in" logos on web pages), or had to find ways to support both. It was a bit dumb, but no one knew any better.


### Javascript

Around about the mid 90s the idea of making web pages do more interactive things took hold. Netscape came up with Java applets (in collaboration with Sun) and Javascript (no relation). Java applets were a thing for many years but eventually Javascript won out. (In the early 2000s Adobe (nee Macromedia) Flash was also an alternative to Javascript; it was extremely popular but rife with security issues and its usage waned with the introduction of HTML5.)

Early JS event handling and HTML manipulation was pretty primitive, by all accounts. Something vaguely resembling the modern world kicked off with Netscape 4 and IE4 with the introduction of the DOM.

### CSS

Remembering that HTML was initially a text-based system, in the early years styling was bolted on as an afterthought in fairly hideous ways by (for example) adding style attributes to elements and wrapping them in `<font>` tags:

```
<font size="+3" face="arial">
    <p color="red">Hot text</p>
</font>
```

Worse still if you wanted to do multi column page layouts you did it by bunging everything in a `<table>`. This made for a lot of markup and was just generally messy.

Cascading stylesheets (CSS) was the W3C-mandated solution to this problem, implemented either inline in the `style` attribute or (more orthodoxly) in separate CSS files. CSS adoption by browsers was fairly haphazard at first, but around 2000 it became stabler. However into the mid 2000s people continued to build table-based layouts.

## Web 2.0

If you worked in the web in the mid 2000s you couldn't avoid the phrase "Web 2.0". It described both a new breed of "social" websites (Myspace(!), YouTube, Facebook) and the new web technologies that powered those sites.

Web 2.0 has never really stopped, it's just people stopped using the phrase, probably around 2008ish(??)

### Your browser history (part two)

IE (and Microsoft generally) reigned supreme for the better part of 10 years, between the mid 90s and the mid 2000s. So great was the dominance that Microsoft didn't even bother to release a new version of IE between 2001 and 2006. This proved Microsoft's undoing; a new breed of standards-conformant browsers such as Firefox (derived from Netscape) and Safari (given prominance through the triumph of the iPhone) wrested a measure of control of the web back, and Chrome eventually finished IE off, and event IE's successor Edge is thoroughly ignored.

### AJAX

Web 2.0's special sauce was AJAX (asynchronous javascript and XML) which allowed JS to manage network requests in response to UI events without having to reload the page, making the interface faster, more responsive. Microsoft's original intent was to retrieve data from a server in XML format, but these days it's largely JSON.

### HTML5 and WHATWG vs W3C

(This is ancient history but it is still relevant today.)

In 1997 HTML v4 came out and was widely adopted by the web. W3C saw the way forward after HTML4 as XHTML, an XML (look it up) conformant version of HTML. XHTML uptake was pretty limited and there was something of a schism between browser makers who had to maintain a level of backwards compatibility and the W3C which was (to the browser makers at least) a bureaucracy infested with special interest interference. The result was the formation of the WHATWG to modernise HTML as HTML5. W3C and WHATWG reconciled with W3C deciding to codify WHATWG's work periodically and WHATWG continually making a "living standard".

### The increasing importance of Javascript

By the mid 2000s Javascript was mature but also a pain to work with. However a highly interactive UI had transformed web pages from being passive documents for passive reading to application interfaces that could display such exciting things as video players and content editors. Implementing these widgets in Javascript meant writing a lot of Javascript, and libraries that could reduce the amount of JS that needed to be written were sorely needed. The jQuery javascript library provided a simplified syntax for DOM manipulation and made writing UI interactions easier.

(From a historical perspective jQuery is at best a stepping stone but I used it a lot and still love it.)

## Today

Today HTML5 is well and truly the lingua franca of the web. CSS has matured and is pretty solid. Javascript continues to bubble and froth with change, however, and there have been developm

The following are features of the modern web development landscape.

### Javascript frameworks

While jQuery allowed users to pile more and more javascript into web pages, it didn't facilitate readable code. What was needed was a JS library that would provide conventions for a developer to follow.

There are many such frameworks out there, including:

* backbone.js (hated it)
* ember.js (never used it)
* angular.js (used version 1)
* react.js (currently use and like)
* `insert numerous additional flavours of the month here`

The point is not so much which framework is best but the necessity of using a framework for "modern" web development.

### One page apps

With javascript's ability to manipulate the DOM, HTML can be as simple as:

```
<body>
    <div id="app" />
</body>
```

... with everything you see in the page being inserted into the DOM by the page's associated javascript.

### Open source

Open source software (free to use, free to alter, free to contribute back) is now used across the web industry in a myriad of ways. For a web developer it means you can build a site out of a thousand off the shelf components

#### Git and Github

Approximately 2005ish there was a bit of a carry on about the propietory source control system being used for the Linux kernel, and Linus himself decided to write his own source control system, which like Linux he named after himself: git. There are other source control packages out there but git has kind of become the lingua franca through the ubiquity of github.

Github hosts a bajillion things related and unrelated to the web. Of most value web wise is innumerable NPM javascript modules (see below).

#### Node.js and npm

Node.js is an implementation of Chrome's javascript engine intended to be run on/as a web server. NPM is node's package management system. Node's principle attraction for frontend web development is the fast collection of libraries available for download and use, and the portability of installing these libraries in multiple environments via the `package.json` file.

### CSS frameworks

As with JS frameworks CSS has been a subject of attempt to provide disclipline. Stylesheet languages such as SASS and LESS allow users to write styles in a more concise, orderly fashion. There are also composite frameworks like bootstrap which provide both JS and CSS templates for site development.

## Nuts and bolts: Ecmascript + Babel + webpack + typescript

All through the history of the web, browsers have been bottlenecks for developing new features. In recent years updates to the Javascript standard (called ECMAscript) have come quicker than browsers can implement. The solution is [Babel](https://babeljs.io/), a JS library which takes code written in unsupported versions of Javascript and transpiles them to browser-friendly JS.

Transpiling JS adds a lot of complexity to the build process, but the ability to write code using more modern language features is seen as worthwhile.

Microsoft has developed TypeScript, an extension of Javascript which supports typing, throwing a mass of errors if a passed variables don't conform to type.

Finally there are libs that build JS files from source through transpilation and minification, such as webpack and browserify. These libraries can also transpile SASS and LESS files.

## Conclusion

The modern state of web development is vastly more complicated now than it was 10 years ago, and the web today is unrecognisable from its origins. If Tim Berners-Lee had known back in 1989 what the web would become, he'd be like "whaaat?". Where will it go? Well, from the javascript side it'd be nice if the Babel/webpack shimming wasn't necessary, and indeed browser support (aside from dirty old IE) is almost there. Except browsers will then have to play catchup with ES7 and Es8 and... so who knows.
