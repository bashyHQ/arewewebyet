---
layout: topic
title: "Lower Web-Stack"

level: 2

intro: A strong lower web-stack is important not only to build strong web frameworks on top, but also to allow performance critical systems to reach deeper to squeeze out extra juice. Rust has a good support on HTTP servers, even an HTTP2 implementation, websockets and other protocols.

servers:
 - hyper
 - tiny-http

http2:
 - h2
 - solicit

websocket:
 - websocket
 - ws
 - websocket-stream
 - rustic-io

protocols:
 - crust
 - ftp
 - fastcgi

news_tag: stack


upcoming:
 - name: hyper-tokio
   url: https://github.com/hyperium/hyper/issues/934
   desc: a tokio/futures based hyper
 - name: fractalide
   url: https://github.com/fractalide/fractalide
   desc: simple rust microservices

---

## HTTP Servers

{% include packages.html packages=page.servers %}

## HTTP2

{% include packages.html packages=page.http2 %}

## Websocket

{% include packages.html packages=page.websocket %}


## Other protocols

{% include packages.html packages=page.protocols %}
