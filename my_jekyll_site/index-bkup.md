---
title: My page
layout: default
---

# {{ page.title }}

Content is written in [Markdown](https://learnxinyminutes.com/docs/markdown/).
Plain text format allows you to focus on your **content**.

You can use HTML elements in Markdown, such as the comment element, and they won't
be affected by a markdown parser. However, if you create an HTML element in your
markdown file, you cannot use markdown syntax within that element's contents.

<h2>Output all page URLs</h2>
  <ol>
    {% for key in site.pages %}
      <li>{{key.url}}</li>
    {% endfor %}
  </ol>


<h2>Output all page titles</h2>
  <ol>
    {% for key in site.pages %}
      <li>{{key.title}}</li>
    {% endfor %}
  </ol>

<h2>Filter by title</h2>
  <ol>
    {% for key in site.pages %}
    {% if key.title %}
        <li>{{key.title}}</li>
    {% endif %}
    {% endfor %}
</ol>

<h2>Output all `item.link`</h2>

  {% for item in site.data.navigation %}
  <a href="{{ item.link }}">{{ item.link }}</a>
  {% endfor %}



