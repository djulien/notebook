# Contents
[toc]

## Introduction
A *JavaScript Notebook* is an interactive web page using JavaScript.  It is similar in concept to a [Jupyter Notebook](https://jupyter.org), except that it runs Javascript instead of Python (cause I'm a Node.js fan &#x1F601;).

This particular implementation is more simplistic.  Notebook pages are stored as Markdown (text) files, and a small Javascript server (in Node.js) uses [Showdown](https://github.com/showdownjs/showdown) to render the Markdown text as HTML tags for display in the browser.

The Notebook pages can be as simple as static Markdown/text, or as complex as an entire web app.  They can pull in additional HTML, CSS, Javascript, or other files from the web server's file system or from a public CDN.

Notebook pages are also intended to be self-contained (except for CDNs), similar in concept to [TiddlyWiki](https://tiddlywiki.com). (not there yet &#x1F615;)

## Getting Started
To create a Notebook page from scratch, just create a Markdown text file and store it on a web server with a file name ending with ".md".  Alternatively, open an existing/example notebook page, then edit it and save with a different file name.  The Markdown syntax is described on the [Showdown syntax wiki page](https://github.com/showdownjs/showdown/wiki/Showdown's-Markdown-syntax).

To set up the Javascript Notebook server, follow these steps:
1. install [Node.js](https://nodejs.org)
2. create a local folder for your Javascript Notebook pages; `cd` into the folder
3. `npm init && npm install --save https://github.com/djulien/jsNotebook`
OR
   `git clone https://github.com/djulien/jsNotebook`
4. `npm test`

When a Notebook page is opened in the browser, the server will render its contents as HTML so it can be displayed in the browser.

## Status
UNDER CONSTRUCTION

Current status/todo:
- [x] server renders MD to HTML
- [x] create a couple of examples
- [x] allow local/CDN Javascript files (OpenGL shader example)
- [ ] self-contained; rework template as bare-bones HTML file
- [x] auto-generate TOC from headings
- [ ] allow in-place Notebook editing
- [ ] live reload
- [ ] in-line fragment shader? (self-contained notebook)
- [ ] save edited Notebook to local/server
- [ ] file manager (tab)
- [ ] allow HTML/CSS/JS template editing (tabs)
- [ ] fancier Three.js, FX examples
- [ ] add extensions: showdown-icon, katex-latex?

#### (eof)
