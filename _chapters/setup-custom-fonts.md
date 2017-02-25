---
layout: post
title: Setup Custom Fonts
date: 2017-01-08 00:00:00
---

Custom Fonts are now an almost standard part of modern web applications. We'll be setting it up for our note taking app using [Google Fonts](https://fonts.google.com).

This also gives us a chance to explore the structure of our newly created React.js app.

### Include Google Fonts

For our project we'll be using the combination of a Serif ([PT Serif](https://fonts.google.com/specimen/PT+Serif)) and Sans-Serif ([Open Sans](https://fonts.google.com/specimen/Open+Sans)) typeface. They will be served out through Google Fonts and can be used directly without having to host them on our end.

Let's first include them in the HTML. Our React.js app is using a single HTML file.

{% include code-marker.html %} Go ahead and edit `public/index.html` and add the following line in the `<head>` section of the HTML to include the two typefaces.

{% highlight html %}
<link rel="stylesheet" type="text/css" href="https://fonts.googleapis.com/css?family=PT+Serif|Open+Sans:300,400,600,700,800">
{% endhighlight %}

Here we are referencing all the 5 different weights (300, 400, 600, 700, and 800) of the Open Sans typeface.

### Add the Fonts to the Styles

Now we are ready to add our newly added fonts to our stylesheets. Create React App helps separate the styles for our individual components and has a master stylesheet for the project located in `src/index.css`.

{% include code-marker.html %} Let's change the current font in `src/index.css` for the `body` tag from `font-family: sans-serif;` to the following.

{% highlight css %}
font-family: "Open Sans", sans-serif;
font-size: 16px;
color: #333;
{% endhighlight %}

{% include code-marker.html %} And let's change the fonts for the header tags to our new Serif font by adding this block to the css file.

{% highlight css %}
h1, h2, h3, h4, h5, h6 {
  font-family: "PT Serif", serif;
}
{% endhighlight %}

Now if you just flip over to your browser with our new app, you should see the new fonts update automatically; thanks to the live reloading.

![Custom fonts updated screenshot]({{ site.url }}/assets/custom-fonts-updated.png)

We'll stay on the theme of adding styles and setup our project with Bootstrap to ensure that we have a consistent UI Kit to work with while building our app.