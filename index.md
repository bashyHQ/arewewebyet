---
layout: main
---

# Are we *web* yet?

**You can build stuff!**

<p>Rust has a mature <a href="/topics/stack/">HTTP stack</a>{% include level.html level=2%} and various <a href="/topics/frameworks/">frameworks</a>{% include level.html level=3 %} enable you to build APIs and backend services quickly. While increasingly more <a href="/topics/database/#drivers">databases drivers</a>{% include level.html level=2 %} become available, <a href="/topics/database/#orms">ORMs</a>{% include level.html level=5 %} and connections to <a href="/topics/services/">external services</a>{% include level.html level=5 %} (like search or worker queues) are still scarce. Looking further, it doesn't necessarily get better. Though there is significant support for base needs (like <a href="/topics/compression/">data compression</a>{% include level.html level=2 %} or <a href="/topics/logging/">logging</a>{% include level.html level=2 %}), a lot more web-specific needs are still unmet and immature.</p>

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
    <a href="/topics/frameworks/#pkg-gotham">Gotham</a>
  </li>
  <li>
    <a href="/topics/frameworks/#pkg-rocket">Rocket</a>
  </li>
  <li>
    <a href="/topics/frameworks/#pkg-tower-web">Tower Web</a>
  </li>
  <li>
    <a href="/topics/frameworks/#pkg-warp">Warp</a>
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
    <a href="/topics/database/#pkg-rustorm">Rustorm (Postgres / Mysql / Sqlite)</a>
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
    <a href="/topics/stack/#pkg-tiny_http">tiny_http</a>
  </li>
</ul>

### Getting started

A small selection of tutorials with no particular order

- [Creating a REST API in Rust with warp](https://blog.logrocket.com/creating-a-rest-api-in-rust-with-warp/)
- [Create an async CRUD web service in Rust with warp](https://blog.logrocket.com/create-an-async-crud-web-service-in-rust-with-warp/)
- [Building an API with Rust using Tokio and Warp](https://levelup.gitconnected.com/building-an-api-using-warp-and-tokio-26a52173860a)
- [Build an API in Rust with JWT Authentication](https://auth0.com/blog/build-an-api-in-rust-with-jwt-authentication-using-actix-web/)
- [Simple TODO Service With Actix (Rust): Part 1](https://dzone.com/articles/simple-todo-service-with-actix-rust-part-1)
- [Rust + Actix + CosmosDB (MongoDB) tutorial api](https://dev.to/jbarszczewski/rust-actix-cosmosdb-mongodb-tutorial-api-17i5)
- [Build a Smart Bookmarking Tool with Rust and Rocket](https://developers.facebook.com/blog/post/2020/06/03/build-smart-bookmarking-tool-rust-rocket/)
- [Rust Web development | Boilerplate free with Rocket](https://dev.to/nemesiscodex/rust-web-development-boilerplate-free-with-rocket-438l)
- [Your first Rust server with Rocket](https://www.newline.co/@lsunsi/your-first-rust-server-with-rocket--5967d91d)
- [Serverless Rust with Tide, Appsody and Knative](https://appsody.dev/tutorials/ServerlessRust/)


## In detail

learn more about the state of web development in Rust by topic:

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
