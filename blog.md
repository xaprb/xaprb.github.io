---
title: Blog
---
# Blog


<ul class="post-list">
  {% assign sorted_posts = site.posts | sort: 'date' | reverse %}
  {% for post in sorted_posts %}
    <li>
      <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      {% if post.date >= site.time %}
        <span class="future-badge">(Upcoming)</span>
      {% endif %}
    </li>
  {% endfor %}
</ul>