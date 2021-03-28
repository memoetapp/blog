---
layout: post
title: "Memoet tech stack"
date: 2021-03-28 07:00:00
tags: ["Tech"]
---

Start making a website in 2021 put you in a too-many-choices situation, both
for server side and client side. We didn't even mention deployment methods,
CI/CD pipelines, monitoring and alert systems,... However, the answer is
quite more simple than we thought: choose whatever we are comfortable with.

This article only do some explainations about our decisions, it may not apply
for your particular context.

### Why Elixir?

The question start with Memoet's determination from the beginning: it will
start small, be open source and support a self-hosted solution.

We can't simply remove components from a website because it's small. It must
have a framework to do request-response cycle, a database for permanent
storage, a cache for memorize intense functions' result, a queue to execute
long-running tasks, oh and before that, a web server or reverse proxy to
secure and distribute client requests to our web application.

Elixir couldn't replace the database (we use Postgres for that purpose by the
way), but it can do caching, queuing, and web servering also, all from one
running process. We are hooked the first time we heard that, too!

Another great thing about Elixir is we can write a Rust library and import
them from Elixir using Native Implemented Functions (NIFs). We are using Rust
for the SuperMemo2 core logic, which is a ported version of Anki scheduler,
which was written in Python.


### Why not React, Vue, or Stelve?

Because we are tired of build time, of getting one million packages to run
a simple web app, and a bunch of state management frameworks which promised to
make the state managing easier but are hard to keep them not to be abused in
many huge chunks of client code.

In Memoet we only need a little of hiding and showing texts, some transitions
here and there, and AlpineJs does us good.


### TailwindCSS makes styling elements a joy

CSS is not so hard, but it's hard to pick one style in a pool of unlimited
options. Tailwind does a great work of limiting our options into a few and
hence make styling things become much easier and joyful. All Memoet styles are
hand-crafted `rem` by `rem` using TailwindCSS.

If you ask about BootstrapCSS, it is great, but it's component-based, and is
hard to write customized elements because you have to use all CSS options,
again. We would like to be creative and confined at the same time for our
design, so all votes go to Tailwind.


### Conclusion

Making a web app is easy nowaday, the difficult thing is to pick what really
bring you the joy. In our case, it is Elixir, AlpineJs and TailwindCSS.

Take a peak at our source: [github.com/memoetapp/memoet](https://github.com/memoetapp/memoet).
