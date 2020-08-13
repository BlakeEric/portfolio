---
layout: post
title: "13 Semantic HTML Elements You’ve Probably Never Heard Of"
date: 2020-08-01 12:19:07 -0700
---

## With the abstractions that modern front-end frameworks provide, it’s easy to dismiss plain old HTML as a thing of the past — a mere starting point that necessarily leads to “bigger and better” options. Developers with intimate knowledge of HTML are becoming rarer, and at the same time, experts in accessibility and progressive enhancement are needed like never before.
<!--more-->

[View the original article on Codeburst](https://codeburst.io/13-semantic-html-elements-youve-probably-never-heard-of-fa1d49f93225)

Despite its lack of “cool factor,” HTML is a dynamic tool that is very much alive and changing. In fact, developers have been using the lessons learned from building front-end applications to improve HTML itself, and as the language evolves, so too does its potential. And when it comes to cleaner, more deliberate development strategies, HTML can be used to replace functionality commonly generated with a hodgepodge of div and span elements, CSS overrides, and React abstractions.

So without further ado, here are a bunch of semantic HTML elements to help you on your quest to build a better web. If you’ve used these elements before, then congratulations. You are a hero and the web needs you. If these elements are new for you, then consider this an invitation to dive further into the intricacies of HTML.

*Note: many of these elements have polyfills to support older browsers**,* *but always consult the documentation before using them.* 

## 1. `<area>`, `<map>`

The [`<area>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/area) element, used within a [`<map>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/map) element, defines a specific region of an image and optionally associates it with a link. Using these elements, you can create links around certain *parts* of an image.

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="blakeeric" data-slug-hash="jOWLwpo" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="&amp;lt;area&amp;gt; and &amp;lt;map&amp;gt; elements">
  <span>See the Pen <a href="https://codepen.io/blakeeric/pen/jOWLwpo">
  &lt;area&gt; and &lt;map&gt; elements</a> by Blake Eric (<a href="https://codepen.io/blakeeric">@blakeeric</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

## 2. `<base />`

The `[<base>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/base)` element creates the root URL to use relative URLs in an HTML document. 
It can even be accessed within scripts using `document.baseURI`.

```
<head>
    <base href="https://www.myurl.com/" />
</head>

<body>
    <a href="suburl">Visit https://www.myurl.com/suburl</a>
</body>
```

## 3. `<cite>`

The [Citation element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/cite) defines a reference to a cited creative work.

```
<img src="the_alchemist_cover.jpg" alt="The Alchemist Book Cover">
<p><cite>The Alchemist</cite> by Paulo Coelho. Published in 1988.</p>
```

## 4. `<datalist>`

The [`<datalist>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist) element contains a list of `<option>` elements that represent key recommended terms for other fields. Take a look at the example below where an `<input/>`  component can be augmented with search-like functionality without the need for JavaScript.

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="blakeeric" data-slug-hash="QWyMojx" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="&amp;lt;datalist&amp;gt; demo">
  <span>See the Pen <a href="https://codepen.io/blakeeric/pen/QWyMojx">
  &lt;datalist&gt; demo</a> by Blake Eric (<a href="https://codepen.io/blakeeric">@blakeeric</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

## 5. `<details>`

The [Details element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details) is basically the native HTML version a dropdown UI component. Additional information is displayed when the element is toggled into an "open" state.

<p class="codepen" data-height="265" data-theme-id="light" data-default-tab="html,result" data-user="blakeeric" data-slug-hash="eYJEXJo" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="&amp;lt;details&amp;gt; demo">
  <span>See the Pen <a href="https://codepen.io/blakeeric/pen/eYJEXJo">
  &lt;details&gt; demo</a> by Blake Eric (<a href="https://codepen.io/blakeeric">@blakeeric</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

## 6. `<dialog>`

The HTML [`<dialog>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog) element represents an interactive component such as a dismissable warning.

```
<dialog open>This is an open dialog window</dialog>
```

## 7. `<dd>, <dt>, <dl>`

[These elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dd) provide descriptions, definitions, or values for items in a description list. Newer browsers automatically format terms and definitions with logical indentation.

```
<dl>
    <dt>George Michael</dt>
    <dd>80's Musician</dd>
    <dt>Madonna</dt>
    <dd>90's Musician</dd>
</dl>
```

## 8. `<dfn>`

The [Definition element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dfn) is used to indicate the term being defined within other content. The nearest parent element is the definition for the indicated term.

```
<p><dfn>HTML</dfn> is the standard markup language for creating web pages.</p>
```

## 9. `<hgroup>`

The [`<hgroup>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hgroup) element wraps a multi-level heading, grouping a set of `h1`-`h6` elements.

```
<hgroup>
    <h1>Main Header</h1>
    <h2>Subheader</h2>
</hgroup>
```

## 10. `<kbd>`

From [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/kbd): “The `<kbd>` element represents a span of inline text denoting textual user input from a keyboard, voice input, or any other text entry device. By convention, the user agent defaults to rendering the contents of a `<kbd>` element using its default monospace font, although this is not mandated by the HTML standard.”

```
<p>Press <kbd>Cmd</kbd> + <kbd>C</kbd> to copy text.</p>
```


## 11. `<mark>`

The [`<mark>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/mark) element defines text that is highlighted for reference or notation purposes

```
<p>This is not that important. <mark>But this is</mark>.</p>
```

## 12. `<meter>`

The HTML [`<meter>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meter) element creates a visual representation of a fraction or percentage.

```
<label for="completion">Completion</label>
<meter id="completion" value="2" min="0" max="10">2 out of 10</meter>
```

## 13. `<progress>`

The HTML [`<progress>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/progress) creates a visual representation of the progress of an action.

```
<label for="file">Downloading progress:</label>
<progress id="file" value="32" max="100"> 32% </progress>
```
## Conclusion

These are just some of the many ways semantic HTML can be used to streamline your code. A more thorough understanding of HTML and the possibilities it presents can help developers ensure front-end applications work well for as many users as possible. **So don’t forget about HTML.** You may come to regret it in a couple of years when your React application is outperformed by leaner, simpler projects that make use of the latest HTML and vanilla JavaScript have to offer.


## Further Reading: The Future of Web Components

Semantic HTML elements aren’t the only tools you should be paying attention to. Web Components are a new technology within HTML and vanilla JavaScript that allows developers to create and use their own HTML elements and encapsulate their functionality away from surrounding HTML code. Sound familiar? Read more about web components [here](https://developer.mozilla.org/en-US/docs/Web/Web_Components).