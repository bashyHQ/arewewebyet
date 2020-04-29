---
layout: topic
title: "Deploying"

level: 3

intro: How are on quick and easy deploying of our applications into existing server infrastructures? Well, stuff is looking quite good actually.

---

<h2>Heroku {% include level.html level=3 %}</h2>

You didn't really expect Heroku to support rust natively, did you? But if you are looking at this subject, you probably are familiar with running heroku with an unofficial [buildpack](https://devcenter.heroku.com/articles/buildpacks). In that case, you are in a lot of luck, because [EMK](https://github.com/emk) provides that for you already: [github.com/emk/heroku-buildpack-rust](https://github.com/emk/heroku-buildpack-rust)

<h2>Docker {% include level.html level=2 %}</h2>

There are [official docker images](https://github.com/rust-lang-nursery/docker-rust) for rust ([`rust`](https://hub.docker.com/_/rust/)). Additionally, there are nightly images available ([`rustlang/rust`](https://hub.docker.com/r/rustlang/rust/)) if your application requires it. If you use docker's [multi-stage builds](https://docs.docker.com/develop/develop-images/multistage-build/), you can build your application binary and then copy it into a container. This allows you to avoid deploying the entire compilation toolchain with your web application.

<h2>Unikernels {% include level.html level=4 %}</h2>

Unikernels are the rising star and newest hot thing to do big scale deployment. With Rust being a system language unikernels are an obvious approach to the problem and doing your research you'll find that there is a lot happening here indeed. There's a number of unikernels which support rust:
 - [nanos](https://github.com/nanovms/nanos)
 - [rumprun](https://github.com/rumpkernel/rumprun) with `--target x86_64-rumprun-netbsd`
