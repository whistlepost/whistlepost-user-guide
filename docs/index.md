[separation of concerns]: https://en.wikipedia.org/wiki/Separation_of_concerns

[Apache Sling]: http://sling.apache.org/
[template engines]: https://sling.apache.org/documentation/bundles/scripting.html
[content management]: https://sling.apache.org/documentation/bundles.html#resource-providers

[Schema.org]: https://schema.org
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

## Overview

Whistlepost is a content-first web design platform that builds upon existing technologies and standards to offer a unique approach to website management. The _content_ of a Whistlepost site consists of site structure, page copy and semantic metadata, which together convey the site's strategy and purpose. Visual layout and theming are secondary concerns with Whistlepost, as they can often become a distraction from the original goals and intention of the site.

## Content-first

Whistlepost is designed to support just about any form of content through customization, however out-of-the-box content structure is based on Schema.org metadata. Schema.org is a collaboration between many prominent organizations to define common metadata for content published on the World Wide Web. As such this seems to be a good basis for default content metadata in Whistlepost.

A default site content template is provided via a Github repository, and provides a suggested initial site structure along with some default site management metadata. Using this template as a basis provides an extremely easy way to begin designing a complete website with no web design experience necessary. In fact, when paired with Forestry.io, managing site content can be entirely GUI-based without any local checkout of source repositories.

### Schema.org

All Whistlepost content is compliant with a corresponding [Schema.org] type, making it trivial to include metadata in published content. [Schema.org] metadata provides the benefit of improved Search Engine Optimization (SEO), maximising the reach to your potential target audience.

### Forestry.io

Forestry.io is an online content management platform designed for static site generators, such as Hugo and Jekyll. However it turns out that Forestry.io is also versatile enough to manage site content defined in JSON files, which is essentially what Whistlepost content is. The default site content template includes predefined Front Matter and Sidebar sections to make it easy to get started defining content right away. 

The _configuration_ sections provide Front Matter for configuration of site-wide properties such as branding, navigation, analytics and social media details. The _pages_ sections represent the actual site structure and content, including a default homepage and collections for popular Schema.org content types.

The initial homepage is configured to display a collection of articles with a single feature article as might be used for a blog or news site. However this can be changed simply by changing the template of the homepage, which could be more product- or event-focused, or maybe intended simply to promote a person or place. With Forestry.io and Whistlepost you are free to experiment with different site structures without rewriting the content you already have, which can be reassuring if you have built up years worth of content. 

## Presentation

Of course a website is not complete until it can be verified in a browser, and Whistlepost provides a variety of approaches to testing and publishing content. The Whistlepost publishing engine is built on [Apache Sling], which has a unique approach to the separation of presentation and content that makes the content-first approach of Whistlepost possible. The content as defined in the Github repository mentioned above is pacakged as a _bundle_ and deployed along with the Sling engine and a collection of other supporting bundles. This includes theming bundles that define the actual rendering of content in the browser, and Whistlepost provides an increasing array of theming options.

A default site theme template is also provided via a Github repository, which can be used as the basis for defing your own custom site themes. The theme is where the visual design elements are developed, and may be as trivial or complex as is desired, and may support a range of modern frameworks such as Web Components, React, Bootstrap, etc. The default theme uses Bootstrap to provide visual design consistency and Thymeleaf for HTML templating.

### Thymeleaf

Thymeleaf is a server-side template engine that integrates well with Apache Sling to define page fragments and layouts to define the presentation layer of a website. Thymeleaf provides good support for the _Don't Repeat Yourself (DRY)_ principle by allowing HTML fragments to be included in multiple different pages as required. Apache Sling also includes support for other templating engines such as HTL, JSP and server-side JavaScript, which you are also free to use when defining website themes.

The default theme includes support for rendering pages containing the supported Schema.org entities, including Article, Event, Person, Place, Recipe, etc. In addition various lists are supported for rendering collections, as well as different layouts for pages such as the homepage.

## Publishing

The core Whistlepost engine is released as a Docker image, which may be used either locally for testing or deployed in a variety of containerisation platforms. When run locally content and/or themes may be mounted via filesystem bind mounts or packaged bundles. This make it easy to update content on-the-fly and see changes immediately in the browser.

The ability to mount bundles on container instances also makes this approach well-suited to horizontally-scaled container platforms in that multiple instances can simultaneously share the same content and theming bundles avoiding the need for complex publishing procedures.
