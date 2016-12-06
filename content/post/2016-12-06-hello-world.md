---
categories:
- general
date: 2016-12-06T19:50:37+01:00
keywords:
- blogging
- static site
- github
- github pages
- jekyll
- hugo
title: Hello, World
thumbnailImagePosition: left
thumbnailImage: images/post/daft-hello.jpg
---

> Hello, World.

Welcome to my blog. It's been a while I've been thinking about opening one,
but I somehow lacked a bit of motivation. I needed a little something more
to convince me to start it. It's a bit about time, but also about fun, and
convenience.
<!--more-->

I'm a unix sysadmin and a developer, and I usually prefer plaintext and
console over web interfaces. So, when i discovered
[Markdown](https://daringfireball.net/projects/markdown/), i was really happy.
A simple language for simple documents, (almost) as easy to read in a terminal
as it in a web interface, covering 99% of common document edition needs, no
proprietary format, no complicated applications. Definately nice.

[Github](https://github.com) is great example of markdown versatility.
They use it to render all the README.md file that you see on projects front
pages. Few style classes, few types of elements. This gives github a nice
and coherent look-and-feel over all the site and projects it hosts.

![Github README markdown](/images/post/github-readme-markdown.png)

## Github Pages

After that, they pushed the concept further by creating
[Github Pages](https://pages.github.com/), powered by
[Jekyll](https://jekyllrb.com/), a software written by one of Github's founders.

The concept is simple: generating static-only sites. On Github Pages, the aim is
to provide simple, versionable, developer-friendly and light pages to create
(or generate) projects documentation.

Jekyll, itself, is not limited to documentation. Its core, combined with
different templating engines, themes and plugins makes it a versatile and
powerful publishing tool. And the permalinks, categories, pages, tags, posts
and custom layouts make it perfectly suitable to host a blog.

## Creating a static blog

Incredible! Blogging with just a text editor. The fun could finally start.

Now I needed:

- to learn Jekyll
- a nice theme
- somewhere to host the blog
- a way to edit and make changes from anywhere

Learning a new technology is always fun. So this was a already
a decent motivation to learn jekyll but it's even more fun to be able to
apply it directly to a project.

As a Github user, it felt logical to host the content there.
Plus the Markdown format used to create pages and posts is really suited
to be versioned.

Regarding the hosting platform, I got my own, but since it's all public,
I see no problem hosting it on Github Pages. Plus it's really simple since
it's already integrated, the publishing workflow is automatic and it's free.

Everything going great for now.

While looking for a theme, I discovered [Hugo](https://gohugo.io), a static
site generator written in [Go](https://golang.org). As I felt rapidly more
comfortable with it than with Jekyll, (and they got pretty themes, too),
it became the generator for my blog. Since it's a static binary, it's also
got no dependencies and is really faster to generate pages.

Nice, but it doesn't have the advantage to be integrated in Github.
So, it needs some automation, and this will the topic of another post !

(post icon credits: [Tsukasa-Tux](http://tsukasa-tux.deviantart.com))
