---
layout: main
---

# Are we *web* yet?

**You can build stuff!**

<p>Rust has a mature <a href="/topics/stack/">HTTP stack</a>{% include level.html level=2%} and various <a href="/topics/frameworks/">frameworks</a>{% include level.html level=3 %} enable you to build APIs and backend services quickly. While increasingly more <a href="/topics/database/#drivers">databases drivers</a>{% include level.html level=2 %} become available, <a href="/topics/database/#orms">ORMs</a>{% include level.html level=5 %} and connections to <a href="/topics/services/">external services</a>{% include level.html level=5 %} (like search or worker queues) are still scarce. Looking farther, it doesn't necessarily get better. Though there is significant support for base needs (like <a href="/topics/compression/">data compression</a>{% include level.html level=2 %} or <a href="/topics/logging/">logging</a>{% include level.html level=2 %}), a lot more web-specific needs are still unmet and immature.</p>

<p>&nbsp;</p>

## Can I replace my Rails/Django/Flask already?

**Well, probably not yet**. While the basics are there, many of the handy utility libs that make working with many popular frameworks so quick and easy are still missing. **If your service primarily provides an API** to be consumed by  other computers, requires little external services and you are happy with writing most SQL yourself, then **Yes, You Can!** Otherwise, we would not recommend it just yet.

### What should I replace it with?

The web frameworks of choice in the community are:

<ul>
  <li>
    <a href="/topics/frameworks/#pkg-actix-web">Actix</a>
  </li>
  <li>
    <a href="/topics/frameworks/#pkg-conduit">Conduit</a>
  </li>
  <li>
    <a href="/topics/frameworks/#pkg-gotham">Gotham</a>
  </li>
  <li>
    <a href="/topics/frameworks/#pkg-nickel">Nickel</a>
  </li>
  <li>
    <a href="/topics/frameworks/#pkg-rocket">Rocket</a>
  </li>
</ul>

For data storage there are mature drivers for:

<ul>
  <li>
    <a href="/topics/database/#pkg-mysql">Mysql</a>
  </li>
  <li>
    <a href="/topics/database/#pkg-postgres">Postgres</a> 
  </li>
  <li>
    <a href="/topics/database/#pkg-redis">Redis</a>
  </li>
</ul>

If you'd like to use an ORM there is:

<ul>
  <li>
    <a href="/topics/database/#pkg-diesel">Diesel (Postgres / Mysql / Sqlite)</a>
  </li>
  <li>
    <a href="/topics/database/#pkg-rustorm">Rustorm (Postgres / Sqlite)</a>
  </li>
</ul>

If you need to (or want to) go lower in the stack:

<ul>
  <li>
    <a href="/topics/stack/#pkg-h2">H2</a>
  </li>
  <li>
    <a href="/topics/stack/#pkg-hyper">Hyper</a>
  </li>
  <li>
    <a href="/topics/stack/#pkg-solicit">Solicit</a>
  </li>
  <li>
    <a href="/topics/stack/#pkg-tiny_http">tiny_http</a>
  </li>
</ul>

### Getting started

After you've set up your Rust and worked yourself [through "The Book"](https://doc.rust-lang.org/book/), you might want to check any of these blog posts (ordered latest published first):

- [Using Stainless with Rocket](http://neikos.me/Using_Stainless_with_Rocket.html)
- [REST in Rust](https://gsquire.github.io/static/post/rest-in-rust/)
- [Connecting a webservice to a database in Rust](http://hermanradtke.com/2016/05/23/connecting-webservice-database-rust.html)
- [Let's Build a Web Server in Rust](https://dfockler.github.io/2016/05/20/web-server.html)
- [Creating a basic webservice in Rust](http://hermanradtke.com/2016/05/16/creating-a-basic-webservice-in-rust.html)
- [Build an API in Rust with JWT Authentication using Nickel.rs](https://auth0.com/blog/2015/11/30/build-an-api-in-rust-with-jwt-authentication-using-nickelrs/)


Either way you choose, if you find yourself stuck and looking for help, the [official Rust-Lang user forum](https://users.rust-lang.org/) has a [help section](https://users.rust-lang.org/c/help), where you are welcome to post your questions and soon will find help.


## In detail

learn more about the state of web developer in Rust by topic:

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


<h3> Latest News <a href="/atom.xml" title="subscribe"><i class="fa fa-rss-square"></i></a></h3>

<ul class="related-news">
  {% for post in site.posts | limit:5 %}
    {% include news_item.html post=post %}
  {% endfor %}
  <li><a href='/news/'>show all</a></li>
</ul>
