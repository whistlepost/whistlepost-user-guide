# Publishing Content

## Templates

Templates are used to render the content to a particular output format, such as HTML.
Every content node defines a default template that is used when the content is requested.

Templates may be defined in multiple languages, with the most common being JavaScript (ESP),
Thymeleaf, and Groovy Markup.

### ESP

TBD.

### Thymeleaf

TBD.

### Groovy Markup

TBD.


## Models

Models provide a mechanism for accessing and validating content when rendering with templates.
Whistlepost provides some common model types to represent the structured content mentioned in
the authoring section.

### Article

TBD.

### Recipe

TBD.

### Advertisement

TBD.

### Collection

TBD.


## Static Assets

Rendering content as HTML will typically require additional static files such as style documents (CSS),
media (e.g. images, video, etc.), fonts and Javascript. Whistlepost manages static assets separately from
the templates to allow for improved management of site assets.

For example, you may choose to use a package management tool or bundler to package assets, which may require
some compilation tasks as part of the buid.

### NPM

The Node Package Manager (NPM) provides a way to easily manage your client JavaScript libraries and include
them in your site static assets. Yarn may also be used in place of NPM, which provides similar functionality.

### Webpack

A common approach is to use Webpack to package all CSS, fonts and JavaScript to a single set of files that may
be referenced in the site templates.
