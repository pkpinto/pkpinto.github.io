---
layout: post
title:  'MathJax in Jekyll'
date:   2019-08-10 22:50:00 +0200
categories: jekyll update mathjax
---
{% include mathjax.html %}

Just the example provided by [Arthur O'Dwyer](https://quuxplusone.github.io/blog/2018/08/05/mathjax-in-jekyll/).

Step three is to realize that the Markdown processor used by Jekyll — its name is "Kramdown" —
has a built-in feature called ["math blocks"](https://kramdown.gettalong.org/syntax.html#math-blocks)
which can be hooked up to MathJax! This means that the rest of the integration has already been done for you.
Having followed steps 1 and 2 above, you can now just write TeX code with double-dollar-sign escapes:

    ... a given wire happens to be carrying "$$\lvert 0\rangle$$."
    By that we mean that it's carrying the linear combination
    $$\sum_{x=1}^{\infty} 1$$  ...

This renders as:

... a given wire happens to be carrying "$$\lvert 0\rangle$$."
By that we mean that it's carrying the linear combination
$$\sum_{x=1}^{\infty} 1$$  ...

And if you make a paragraph that contains nothing but a `$$`-escaped chunk of math,
it will be rendered using MathJax's `mode=display`, i.e., TeX display mode.

$$\sum_{x=1}^{\infty} 1$$
