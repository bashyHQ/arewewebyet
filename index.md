---
layout: main
---

# Are we *web* yet?

**You can build stuff!**

<p>Rust has a mature <a href="/topics/stack">HTTP stack</a>{% include level.html level=2%} and various <a href="/topics/frameworks">frameworks</a>{% include level.html level=3 %} enable you to build APIs and backend services quickly. While increasingly more <a href="/topics/database#drivers">databases drivers</a>{% include level.html level=2 %} become available, <a href="/topics/database#orms">ORMs</a>{% include level.html level=5 %} and connections to <a href="/topics/services">external services</a>{% include level.html level=5 %} (like search or worker queues) are still scarce. Looking farther, it doesn't necessarily get better. Though there is significant support for base needs (like <a href="/topics/compression">data compression</a>{% include level.html level=2 %} or <a href="/topics/logging">logging</a>{% include level.html level=2 %}), a lot more web-specific needs are still unmet and immature.</p>

<p>&nbsp;</p>

## Can I replace my Rails/Django/Flask already?

**Well, probably not yet**. While the basics are there, many of handy utility libs that make working with many popular frameworks so quick and easy are still missing. **If your service primarily provides an API** to be consumed by  other computers, requires little external services and you are happy with writing most SQL yourself, then **Yes, You Can!** Otherwise, we would not recommend it just yet.

### What should I replace it with?

The frameworks of choice of the community are <a href="/topics/frameworks#pkg-iron">iron</a>, <a href="/topics/frameworks#pkg-conduit">conduit</a> and <a href="/topics/frameworks#pkg-nickel">nickel</a>, best run with a <a href="/topics/database#pkg-postgres">postgres</a> or <a href="/topics/database#pkg-mysql">mysql</a> backend accompanied by <a href="/topics/database#pkg-redis">redis</a> – all these drivers seem to be fairly mature. If you want to wrap that into an ORM <a href="/topics/database#pkg-rustorm">rustorm</a> and <a href="/topics/frameworks.html#pkg-diesel">diesel</a> are at your disposal – both are still fairly young though.

If you need to (or want to) go lower in the stack, those frameworks all use the fairly stable and mature <a href="/topics/stack.html#pkg-hyper">hyper http stack</a>, if you want it slimmer <a href="/topics/stack.html#pkg-tiny_http">tiny_http</a> might be an option and for the async-fans <a href="/topics/stack.html#pkg-rotor-http">rotor</a> has you covered. If you need HTTP2, you have to turn to <a href="/topics/stack.html#pkg-solicit">solicit</a> as none of the other stacks supports it just yet.


## In detail

learn more about the state of web developer in rust by topic:

<ul class="topic-list">
  {% for page in site.pages %}
    {% if page.layout == 'topic' %}
      <li><a href="{{page.url}}">{{page.title}}</a>  {% include level.html level=page.level%}</li>
    {% endif %}
  {% endfor %}
</ul>

<h3> Latest News <a href="/atom.xml" title="subscribe"><i class="fa fa-rss-square"></i></a></h3>

<ul class="related-news">
  {% for post in site.posts | limit:5 %}
    {% include news_item.html post=post %}
  {% endfor %}
  <li><a href='/news/'>show all</a></li>
</ul>
