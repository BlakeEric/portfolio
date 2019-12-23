---
layout: post
title: "You Don't Need Google Analytics"
date: 2019-12-07 15:59:17 -0700
categories: projects
---

## If you prioritize accessibility, usability, and privacy in front-end development, then Google Analytics is not your friend.
<!--more-->

Have you ever noticed how much Javascript gets loaded on big news sites? As of this writing [Wired's website](https://wired.com) loads __over 3MB of Javascript files alone__, making it almost unusable for anyone with a slow internet connection. Tracking scripts provided by Google, Facebook, and their friends are responsible for a large portion of this bloat. These scripts are used to monitor your behavior around the internet to ensure that the ads you see are sufficiently creepy.

I used to work for a small design/development agency where adding the Google Analytics script served as our stamp of completion just before turning a project over to the client. Even though many of our clients only used the platform to track general page views (or not at all) we always included it because we assumed "they might need it, someday". (That is the same logic you would use to convince yourself not to throw away that pair fingerless gloves from that 80's office party seven years ago.)

Just as you would consider the potential effect that other large third-party packages might have on usability, analytics should not get an automatic pass. Luckily, there are lighter, less invasive ways to track whether your website it meeting its goals.

### What makes Google Analytics problematic?

__It's big.__

The snippet placed in the `<head>` of your markup downloads a larger tracking file totaling around __40kb__. For viewers using older technology or who have a slower internet connection this would result in a noticeable performance hit.

__It's overloaded with features that are way beyond what is necessary for most websites or apps.__

Even in larger applications it is rare to make use of all the features Google Analytics offers. For smaller projects you most definitely do not. But since Google's analytics scripts are not open source, there is no way to pair down the code into only what is needed for your project.

__It's a privacy disaster.__

> Google uses its Analytics product, along with others, to determine a user’s browsing path around the internet. By linking that information to an IP address and an associated Google account, a complete profile of a person can be assembled. It’s this information that gives Google its advertising superpower. - [Hackernoon](https://hackernoon.com/data-privacy-concerns-with-google-b946f2b7afea)

## Options to replace Google Analytics with a more sane solution

__1. Remove analytics tracking completely:__ In some cases the only piece of data that is actively monitored is user traffic. Some hosting platforms provide visitor metrics by default.

__2. Use log analytics:__ Software exists that can turn your raw server logs into a set of organized statistics with many of the same features as Google Analytics. Take a look at [GoAccess](https://goaccess.io/) as an example.

__3. Use an image tracking solution:__ Image tracking works by placing a small `<img>` tag in the html of a website. When the browser makes a request to the url set as the `src` attribute in the image, the analytics service logs data from the IP address that made the request. This approach requires no Javascript and can generate detailed user reports without sacrificing privacy.

__4. Use a different JS tracker:__ There are many analytics options that count privacy as one of their priorities. [Matomo's](https://matomo.org/) analytics script is half the size of Google Analytics, and being open-source, can be modified to bring the size down even more.

## Conclusion

Consider the potential effects overloading your site with trackers might have on user's experience. In many cases there is a lighter alternative to Google Analytics that can provide equivalent data without sacrificing privacy or accessibility.
