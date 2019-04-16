---
layout: post
title: "Add time to a Jekyll blog post"
date: 2019-04-16 22:09:18 IST
description: "Discovered this accidentally, and it is stupid easy"
author: Parth Paradkar
---

While I was further customizing the layout of my blog and posts, I thought it would be nice to show the time at which the post was published. However, the `Minima` theme for `Jekyll` only displays the date of publishing for the post by default. 

<img src="https://raw.githubusercontent.com/thescriptninja/thescriptninja.github.io/master/img/screenshot1.png">

This is the HTML for displaying the date in the `post.html` layout in the `_layouts` folder.

```

 <p class="post-meta"><time datetime="{{ page.date | date_to_xmlschema }}" itemprop="datePublished">{{ page.date | date: "%b %-d, %Y" }}</time>{% if page.author %} • <span itemprop="author" itemscope itemtype="http://schema.org/Person"><span itemprop="name">{{ page.author }}</span></span>{% endif %}</p>

```

After a lot of Googling, I was soon lost in a myriad of unhelpful blog posts and documentation.
Finally I gave up searching and relented to the trial-and-error method. I changed the output string with different variations after the % sign. I won't give each step here, but I finally found the solution.

```

 <p class="post-meta"><time datetime="{{ page.date | date_to_xmlschema }}" itemprop="datePublished">{{ page.date | date: "%b %-d, %Y %T" }}</time>{% if page.author %} • <span itemprop="author" itemscope itemtype="http://schema.org/Person"><span itemprop="name">{{ page.author }}</span></span>{% endif %}</p>

```

Tada!!

<img src="https://raw.githubusercontent.com/thescriptninja/thescriptninja.github.io/master/img/screenshot2.png">

### Thanks for reading!




