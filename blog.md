---
layout: pages
title: Blog
permalink: /blog/
---

  
  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          <p style="color:grey;font-size:18px;font-style:italic">{{ post.description }}</p>
        </h2>
      </li>
    {% endfor %}
  </ul>
