---
layout: post
title: "Add time to a Jekyll blog post"
date: 2019-04-16 22:09:18 IST
description: "Discovered this accidentally, and it is stupid easy"
author: Parth Paradkar
---

While I was further customizing the layout of my blog and posts, I thought it would be nice to show the time at which the post was published. However, the `Minima` theme for `Jekyll` only displays the date of publishing for the post by default. 

<img src="https://raw.githubusercontent.com/thescriptninja/thescriptninja.github.io/master/img/screenshot1.png">

The HTML for displaying the date in the `_layouts/post.html` will contain the following script in it within double curly brackets (can't show paste the HTML code as Jekyll automatically renders it.)

```
page.date | date: "%b %-d, %Y"
```

After a lot of Googling, I was soon lost in a myriad of unhelpful blog posts and documentation.
Finally I gave up searching and relented to the trial-and-error method. I changed the output string with different variations after the % sign. I won't give each step here, but I finally found the solution.

```

page.date | date: "%b %-d, %Y %T"

```


Tada!!

<img src="https://raw.githubusercontent.com/thescriptninja/thescriptninja.github.io/master/img/screenshot2.png">

### Thanks for reading!




