[separation of concerns]: https://en.wikipedia.org/wiki/Separation_of_concerns

[Apache Sling]: http://sling.apache.org/
[template engines]: https://sling.apache.org/documentation/bundles/scripting.html
[content management]: https://sling.apache.org/documentation/bundles.html#resource-providers

[Jekyll]: https://jekyllrb.com/
[Wordpress]: https://wordpress.org/
[Adobe Experience Manager]: https://en.wikipedia.org/wiki/Day_Software

[Webpack]: https://webpack.github.io
[Docker]: https://www.docker.com

[Lazybones]: https://github.com/pledbrook/lazybones
[SDKMAN]: http://sdkman.io/

[Google Analytics]: https://analytics.google.com/analytics
[Disqus]: https://disqus.com
[JSON-LD]: https://json-ld.org
[Opengraph]: http://ogp.me

## Introduction

Whistlepost is a templating engine for Web sites, that helps to manage site structure and content independently of the presentation. The
goal is to provide many of the benefits of a Content Management System (CMS) without the management overhead.

Often we think of modularity and encapsulation as important design principles for software that is more secure, reliable and easier to
maintain. This is often expressed as a [separation of concerns], which is the basis for the Whistlepost platform.

### Apache Sling

Whistlepost is built on [Apache Sling], which has a unique approach to content management in that it provides separation of not only the presentation and content but also the content structure itself. This helps to conceptualise the relationship between content and structure without being distracted by the presentation.

Whilst Whistlepost shares the same origins as [Adobe Experience Manager], it's focus is more aligned to the popular [Jekyll] template engine, which is more concerned with content rendering than lifecycle management. Whistlepost is designed to make it easy to "drop in" to a new or existing site to assist with the separation of the UI and content concerns. This is especially beneficial as sites grow larger and more unweildly over time, and allows both (UX/UI) designers and (content) developers to focus on what is most important to them.

## Features

The primary focus of Whistlepost is the separation of UI and content. Whistlepost doesn't impose restrictions on how the UI is built,
nor does it dictate how and where content is managed.

The key features of Whistlepost include:

* Support for multiple [template engines] including JSP, Thymeleaf and HTL (Sightly)
* Multiple [content management] solutions including NoSQL (e.g. MongoDB), AWS S3, Filesystem, etc.
* Extensions provide additional functionality to support additional site integrations (e.g. OpenGraph, json-ld, etc.)
* Built for containerisation (i.e. Docker) with support for horizontal scaling and multi-tenant solutions.
