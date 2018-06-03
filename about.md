---
layout: page
title: About AWWY
permalink: /about/
---

## About

Are We Web Yet – or AWWY (pronounced _a-we?_) for short – tries to answer the question: **Can I use Rust to do web development (yet)?**

## How to use the site

This website has various features that make your life easier researching whether you can use Rust for the web development already or not. While some stuff is possible already, other parts are still challenging and this website wants to give you insight for your particular case. The easiest is to start looking into the [topics](/topics/) most relevant for you.

While most things should be rather quick to comprehend, there are some features, we'd like to explain to you a little deeper to improve the speed with which you can answer the question for you.

### The Package Info

![Package Info](/assets/about/package-info.png)

For each package we list the most important information in one quick view. Aside from the package id (`hyper`), the header shows various links – if available: the crate.io-page, the homepage, the documentation and to the source code. Tip: When you hover over name, it also shows when the package was created and last updated.

In the second row features the latest published version number, how often the package has been downloaded so far and how it is licensed – all as pretty badges of live data pulled from [shields.io](http://shields.io/).

Under that you can find the short description provided for that package.

#### Comments

![comments](/assets/about/comments.png)

Now some packages contain an extra `comments` sections. By default these are hidden to not clutter the page when you only want to have an overview of what's going on in a specific topic. But with just one click on the word, you can toggle the visibility of the comments for that package.

![comments visible](/assets/about/comments-shown.png)

Each comment features the author, when it was written and what version they were talking about. Make sure to always check the version with the one you see above, things might have changed!

Next to the text itself the side-bar is color coded, where blue and grey indicate informational content, green a positive review or even recommendation, yellow an warning and red an important problem or blocker.

You can also toggle all comments with the little switch on the top right on each topic page. The setting will be saved in your browser and applied on every page load.

### Understanding the level indicator

Throughout the app – mostly on section titles – you find the small `level indicators`: a colored glyph, which should give you a hint on the maturity of the subject overall as designated by the [curators](/curators/). The following indicators are available:

<ul>
  <li>{% include level.html level=0 %} – everything is awesome<a href="https://www.youtube.com/watch?v=9cQgQIMlwWw" target="_blank">™</a>: stable, tested and mature</li>
  <li>{% include level.html level=1 %} – stuff's pretty great</li>
  <li>{% include level.html level=2 %} – getting there, stable but still maturing</li>
  <li>{% include level.html level=3 %} – not yet stable, but progressing</li>
  <li>{% include level.html level=4 %} – unstable/incomplete, needs work</li>
  <li>{% include level.html level=5 %} – barely there, needs serious work</li>
  <li>{% include level.html level=6 %} – basically non-existent</li>
</ul>

If you need a reminder, you can also just hover over the glyph to get the text.


## Credits

This project is hosted and largely developed by [The Bashy](http://bashy.io/), specifically [Benjamin Kampmann](/curators/#ben). The content is curated by the [curators](/curators/). The first version was developed and hosted by [Chris Morgan](https://github.com/chris-morgan). All content is licensed under the [Creative Commons Attribution License (International)](https://github.com/bashyHQ/arewewebyet/blob/gh-pages/LICENSE).
