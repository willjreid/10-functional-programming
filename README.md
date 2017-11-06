![CF](https://camo.githubusercontent.com/70edab54bba80edb7493cad3135e9606781cbb6b/687474703a2f2f692e696d6775722e636f6d2f377635415363382e706e67) Lab 10: Functional Programming
===

## Submission Instructions
Follow the submission instructions from Lab 01.

## Resources  


[MDN: map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

[MDN: filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

[MDN: reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)

## Configuration
_Your repository must include:_

```
10-functional-programming
├── .eslintrc.json
├── .gitignore
├── LICENSE
├── README.md
├── node_modules
├── package-lock.json
├── package.json
├── public
│   ├── data
│   │   └── hackerIpsum.json
│   ├── admin.html
│   ├── index.html
│   ├── new.html
│   ├── scripts
│   │   ├── article.js
│   │   └── articleView.js
│   ├── styles
│   │   ├── base.css
│   │   ├── fonts
│   │   │   ├── icomoon.eot
│   │   │   ├── icomoon.svg
│   │   │   ├── icomoon.ttf
│   │   │   └── icomoon.woff
│   │   ├── icons.css
│   │   ├── layout.css
│   │   └── modules.css
│   └── vendor
│       └── styles
│           ├── default.css
│           ├── normalize.css
│           └── railscasts.css
└── server.js
```

## Feature Tasks

*As a user, I want an admin page so I can easily view the stats of my blog app.*

- For both index.html and admin.html, we'll want access to the `Article.all` data... but we'll have different view functions to set up for each of those pages. Complete the `Article.fetchAll()` method so that it calls a `next` parameter: a function to invoke when its work is done.  

*As a developer, I want to utilize IIFEs so that all of my function calls are executed on page load.*

- Let's make sure each one of our scripts are properly enclosed. Wrap the contents of article.js and articleView.js in an IIFE, like we did in class. Then pass in the new "app" object as an argument to the IIFEs and be sure to remember to export the `Article` and `articleView` objects. Keep in mind that this will change how we refer to those two objects throughout the app.
- Ensure both the index page and the admin page call `Article.fetchAll()` in a way that properly triggers the appropriate page setup methods.

*As a developer, I want to utilize functional programming so that my code makes sense and follows modern practices.*

-  Use the array methods `.filter()`, `.map()`, `.reduce()`, and `.forEach()` to transform the data into what you need it to be. Chain these methods together as needed.

### Stretch Goal

*As a user, I want additional stats so that I can track the progress of my app.*

- What additional statistical analysis would be of interest to you with this data set? Code it up!

## Documentation
_Your README.md must include:_

```md
# Kilovolt Blog with Functional Programming

**Author**: Will Reid
**Version**: 1.0.0

## Overview
Our goal with this project was to build on a mobile-first site, using jQuery to dynamically render blog posts sorted by most recent publication date and allow dynamic filtering in response to user preference for particular authors or categories.  We attempted to refactor some code lines to utilize functional programming best practices.

## Getting Started
To build this app on your own machine, clone this repo and launch the html page in your browser. You will need express and bodyParser, as well as Handlebars, and a node instance.

## Architecture
We are using a SMACSS organization of our CSS. The index.html file reveals the basic template for each article; the article.js file constructs each article; and the articleView.js file allows the user to interact with the elements on-screen.  The server.js file allows the server to provide content.

## Change Log
11-06-2017 -- committing with template links.

## Credits and Collaborations
I'd like to thank JB Tellez for helping me activate postgresql at long last.
```
