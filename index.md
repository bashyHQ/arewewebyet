---
layout: main
---

# Are we *web* yet?

**You can build stuff!**

<p>Rust has a mature HTTP stack and various frameworks enable you to build APIs and backend services quickly.

<p>&nbsp;</p>

## In detail

Learn more about the state of web development in Rust by topic:

<ul class="topic-list">
  {% for page in site.pages %}
    {% if page.layout == 'topic' %}
      <li><a href="{{page.url}}">{{page.title}}</a>  {% include level.html level=page.level%}</li>
    {% endif %}
  {% endfor %}
</ul>

<ul class="legend">
  <li>{% include level.html level=0 %}: everything is awesome<a href="https://www.youtube.com/watch?v=9cQgQIMlwWw" target="_blank">™</a>: stable, tested and mature</li>
  <li>{% include level.html level=1 %}: stuff's pretty great</li>
  <li>{% include level.html level=2 %}: getting there, stable but still maturing</li>
  <li>{% include level.html level=3 %}: not yet stable, but progressing</li>
  <li>{% include level.html level=4 %}: unstable/incomplete, needs work</li>
  <li>{% include level.html level=5 %}: barely there, needs serious work</li>
  <li>{% include level.html level=6 %}: basically nonexistent</li>
</ul>
