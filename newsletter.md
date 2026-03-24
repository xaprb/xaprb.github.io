---
title: Newsletter
---
# Newsletter

The Club's newsletters are available below in PDF format. 

<ol class="newsletter-list">
  {% assign newsletter_files = site.static_files | where_exp: "file", "file.name contains '-newsletter'" | where_exp: "file", "file.extname == '.pdf'" | sort: 'name' | reverse %}
  
  {% for file in newsletter_files %}
    {% assign date_parts = file.name | split: "-" %}
    {% if date_parts.size >= 3 %}
      {% assign year = date_parts[0] | plus: 0 %}
      {% assign month = date_parts[1] | plus: 0 %}      
      {% if year > 1900 and month >= 1 and month <= 12 %}
        {% assign date_string = year | append: "-" | append: month | append: "-01" %}
    <li>
      <a href="{{ file.path | relative_url }}">
        {{ date_string | date: "%B %Y" }} Newsletter
      </a>
    </li>
      {% endif %}
    {% endif %}
  {% endfor %}
</ol>