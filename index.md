---
title: Rockbridge Bird Club
# bundle exec jekyll serve
# http://127.0.0.1:4000/
---
# Welcome to the Rockbridge Bird Club

**Encouraging enjoyment, knowledge, and conservation of birds in the Rockbridge
County, Virginia area.**

For more information, email rockbridgebirdclub@gmail.com

## Calendar

Details for Calendar events can be found in the Newsletter. Be alert for possible impromptu excursions!

<ul class="post-list">
  {% assign future_posts = site.posts | where_exp: "post", "post.date >= site.time" | sort: 'date'  %}
  {% for post in future_posts %}
    <li>
      <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

## Membership

**Join the Club!**  Dues are $15 per household, and donations above that amount are
gratefully received.  Your contribution helps pay for excellent programs open
to the public, educational projects for adults and kids, and more.  (Note that
donations to the Bird Club are not tax-deductable.) Please make out your check
to Rockbridge Bird Club and send it, along with your address, email address,
and phone number, to Jan Smith, 564 Big Hill Rd. Lexington, VA 24450. Thank
you.
