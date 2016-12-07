---
categories:
- technology
date: 2016-12-07T01:50:37+01:00
keywords:
- web
- technology
- static
- security
- performance
- cdn
tags:
- static sites
- web
- angularjs
title: The power of static websites
thumbnailImagePosition: left
thumbnailImage: images/post/ice-cube.png
---

Static website generation is becoming cool again.

With third-party services offering easy integration into static pages
on one side, and the hype around client-side javascript frameworks
powering full-api sites on the other, there are more and more use-cases
where serving static content is completely viable.

And there are many advantages to doing this.
<!--more-->

## Security

In the past years, web-based services and software have suffered countless
security vulnerabilities. Developers are humans. So sometime they make mistakes.
And a mistake can result in a security issue:

- Injection flaws
- Authentication flaws
- Cross Site Scripting
- Cross Site Request Forgery
- Unvalidated redirects

But the users and admins can also cause problems:

- Outdated or vulnerable software
- Software misconfiguration
- Broken architecture

Static content, in the other hand, has a far smaller attack surface.
There are still some attack vectors, but it eliminates a lot of threats.

## Performance

Website performance is crucial today. Studies have shown that people tend to
quickly leave unresponsive websites. So, when you talk about an e-commerce
website, the lack of speed quickly becomes missing money.

The closer the user is from the content, the quicker it's delivered.
With the rise of high-popularity worldwide websites, the need to put the content
as close as possible is high. Plus, moving data around the globe costs money.
It's often cheaper to serve content from a near network.

To answer this need,
[CDN](https://en.wikipedia.org/wiki/Content_delivery_network) were created.
They're perfect for speeding up static or semi-static data delivery, but there
are no miracles about dynamic content.

{{< alert info >}}
When I talk about semi-static content, I think of dynamic but medium-lived,
reusable content, with proper expiration info. Example: a dynamically-generated
image valid for a few minutes, with
[cache control](https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.9)
headers.
{{< /alert >}}

Usually, with server-side generated pages, the structured data is transfered
from a data source (ex: SQL Database) to the server. Then the server use it to
generate a page, putting all the content presentation layer around it, then
transferring all of this to the client. A large part of the webpage will not
change on the next call, but this will not be cached.

On the other hand, static websites are often fully cacheable.
All the presentation layer (pages, js,  css, images) will be transfered once
from the source to the CDN, then to the client. Later calls from clients in the
same region will be served directly from the CDN, and all of this is fully
cacheable.

For client-side javascript sites using APIs, only the variable structured data
will be transfered from the servers to the client. It means less traffic, less
server processing, quicker page loads with quickly available partial content.

Plus, as some javascript frameworks become popular, they become available freely
on vendor-provided CDNs, so clients of two different websites using the same
version of the framework will probably get it from the same location.
It means that when they will go visit the second site, parts of it will already
be in the local cache.

{{< alert success >}}
At [Scaleway](https://scaleway.com), we run a fully static website, and a static
user console powered by [AngularJS](https://angularjs.org), only consuming APIs.
{{< /alert >}}

## Simplicity

Running complex server software, or software with questionable security model
(Who said PHP ?) increases the risks of misconfiguration or vulnerabilities.

Plus, complexity comes at a cost:

- deploying software
- making sure it's working
- getting proper resources for it to run
- doing regular updates
- ensuring library compatibility
- scaling

All of this costs time and money.

## Tools

Many website creation tools emerged these last years, almost every popular
language has its own.

Here are some famous ones:

- [Jekyll](https://jekyllrb.com)
- [GitBook](https://www.gitbook.com)
- [Hugo](https://gohugo.io)
- [Hexo](https://hexo.io)
- [Octopress](http://octopress.org/)

(Source: [StaticGen](https://www.staticgen.com))

So, next time you have to choose the technology for a project,
don't forget to think about going static!
