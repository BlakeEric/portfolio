---
layout: post
title: "How to Be a More Ethical Developer in 2020"
date: 2020-04-15 08:59:17 -0700
---

## By using a “simple-first” approach, front-end developers can create a healthier internet.
<!--more-->

[View the original article on JavaScript in Plain English](https://medium.com/javascript-in-plain-english/how-you-can-become-a-more-ethical-developer-in-2020-a96efb803f3e)

The last couple of years have not been pretty for the tech industry. With the average user growing more wary of how their online data is being used and more frustrated by disruptive online advertising, how can developers work to create a safer, more useful, and more ethical web in 2020?

### Simplicity goes hand-in-hand with accessibility and privacy.

Consider the "share" button snippet provided by Facebook:

{% highlight html %}
<!-- Load Facebook SDK for JavaScript -->
<div id="fb-root"></div>
<script>(function(d, s, id) {
  var js, fjs = d.getElementsByTagName(s)[0];
  if (d.getElementById(id)) return;
  js = d.createElement(s); js.id = id;
  js.src = "https://connect.facebook.net/en_US/sdk.js#xfbml=1&version=v3.0";
  fjs.parentNode.insertBefore(js, fjs);
}(document, 'script', 'facebook-jssdk'));</script>

<!-- Your share button code -->
<div class="fb-share-button"
  data-href="https://www.your-domain.com/your-page.html"
  data-layout="button_count">
</div>
{% endhighlight %}

This snippet downloads more than 200kb (60kb gzipped) worth of tracking scripts that make the page slower, gather private data about the user’s browsing habits, and contribute to the scourge of targeted ad campaigns that make the user experience worse. It will also not work if a user has JavaScript disabled or if the script fails to download.

Now consider a simpler solution to create the same functionality:

{% highlight html %}
<a href="http://www.facebook.com/sharer.php?u=https://www.your-domain.com/your-page.html">
  Share This Link on Facebook
</a>
{% endhighlight %}

By using a humble html link, we not only protect the user’s privacy, but also make the page faster and more reliable.

### Guidelines for the "simple-first" approach

* __Prioritize the user over the developer__ - The goal should be to get useful information to the user as efficiently as possible, even if it means utilizing fewer “cutting-edge” tools. JQuery, for example, is over 33kb minified and gzipped. Vanilla Javascript is slightly less concise but can be easily used to create the same functionality in most cases. Check out [Go Make Things](https://gomakethings.com/articles/) for vanilla JS tips.

* __Use native browser functionality when possible__ - JavaScript frameworks like React and Vue offer a lot of useful features, but these should be carefully weighed against the features web browsers provide by default. The react-router package, for example, performs the same basic functionality as the navigation built into all web browsers while being more likely to cause usability issues in older versions. If there is a clear benefit to using a third-party package--by all means--use it. But first find out if the same functionality is possible using simple HTML, CSS, and vanilla JavaScript on the front end.

* __Only gather user data if you need it__ - Collecting usage data is important if you are trying to determine whether or not the goals of your content are being met. However, you can choose an analytics service that only gathers the data necessary to measure these goals. Google Analytics collects way more data than is needed to analyze traffic on the vast majority of websites, and its respect for user privacy is [questionable](https://hackernoon.com/data-privacy-concerns-with-google-b946f2b7afea). Try skipping JS-based analytics by using [GoAccess](https://goaccess.io/) to analyze your server logs, or use [Matomo](https://matomo.org/) for a lighter analytics platform with a more responsible privacy policy. I address these options in more detail in a [separate article]({% post_url 2019-12-07-you-dont-need-google-analytics %}).

* __Rethink advertising__ - Sites that use Google and Facebook’s advertising platforms end up being slow, bloated behemoths that are inaccessible to users who don’t have the latest gadgets. These scripts stalk users around the internet to establish eerily detailed advertising profiles. Luckily, there are more respectable advertising solutions like [Codefund](https://codefund.io/), as well as [alternative methods of monetizing your content](https://hackernoon.com/monetize-your-website-without-advertising-email-hcaptcha-recaptcha-brave-f266e905510a).

* __Use vetted third-party integrations__ - When possible, use third-party packages and APIs built by developers who share your interest in creating a better web.

### Conclusion

Developers don’t always get the final say on all of these decisions, but if more of us advocate for a “simple-first” approach we can prove that engaging and successful web products can be created without sacrificing trust or accessibility.
