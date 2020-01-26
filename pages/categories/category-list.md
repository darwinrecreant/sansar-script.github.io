---
title: Category List
summary: "Complete list of categoriees"
sidebar: sidebar
permalink: category-list.html
topnav: topnav
---

{% assign categories = site.data.sidebars[page.sidebar].entries %}

<p>List of ctaegories for use in your page FrontMatter.</p>

<ul>
  {% for entry in categories %}
    {% for folder in entry.folders %}
        {% for folderitem in folder.folderitems %}
            {% if folderitem.category %}
            {% assign foldercategory = folderitem.category %}
                <li><strong>{{folderitem.category}}</strong></li>             
            {% endif %}
        {% endfor %}
      {% endfor %}
    {% endfor %}
</ul>
