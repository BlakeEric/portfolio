---
layout: post
title: "Lightweight Alternatives to React"
date: 2020-02-07 11:11:07 -0700
---

## Alternative frameworks that utilize the developer-friendly patterns of React without breaking the bank.
<!--more-->

React is the developer’s equivalent of Avocado Toast. It’s great, but it’s expensive and has a lot of unnecessary toppings. React rewrites a lot of native browser functionality with features like the Virtual DOM and synthetic browser events. This practice negatively impacts SEO, progressive enhancement and initial load time. Read on for some light-weight alternatives that still allow for a rich user experience.

### Vanilla JS

Who said you had to use a front-end framework? For a lot of projects, the most efficient way to handle DOM manipulation is with regular-old JavaScript. Relatively recent updates such as the [Selectors API](https://www.w3.org/TR/selectors-api/) have made vanilla JS much more user-friendly, and you don’t have to worry about accidentally including code for features you don’t need.

### Preact

[Preact](https://preactjs.com/) is a React-like framework with nearly identical syntax, but [less unnecessary fluff](https://preactjs.com/guide/v10/differences-to-react). This is a great option if you know React already and has the benefit of being ten times smaller thanks to a simpler DOM diffing algorithm and the fact that it uses the browser's native `addEventlistener` for event handling, rather than implementing its own event system like React.

### Svelte

[Svelte](https://svelte.dev/) is a *compiler* that allows developers to write components in a format that looks a lot like regular HTML and Javascript with some JSX patterns mixed in. Its developers jettisoned the virtual DOM completely, arguing that the overhead in DOM diffing negates the fact that it saves parts of the UI from being unnecessarily repainted. Svelte’s build process compiles components into standalone JavaScript modules that don’t require a massive JS dependency. According to [Svelte’s documentation](https://svelte.dev/blog/frameworks-without-the-framework), “the [Svelte implementation of TodoMVC](http://svelte-todomvc.surge.sh/) weighs 3.6kb zipped. For comparison, React plus ReactDOM without any app code weighs about 45kb zipped. It takes about 10x as long for the browser just to evaluate React as it does for Svelte to be up and running with an interactive TodoMVC.”

### Conclusion

The ubiquity of bloated front-end frameworks comes at a cost. Webpages are [getting larger](https://httparchive.org/reports/page-weight) and less accessible to users who don’t have the latest technology. It’s nice to know that developers are building lighter frameworks that may help to reverse this trend.
