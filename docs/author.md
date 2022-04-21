# Digital Content Authoring
This page outlines how content authoring is supported with Whistlepost.

## Overview

Digital content authoring is primarily focused on managing site content without concern for how the content is displayed on the live site. A content author will make use of the provided templates to populate content that combined with styling and appearance to render the final site.

Whistlepost content is a collection of JSON documents arranged in a hierarchical structure that typically represents the published website structure. For example, if you have a collection of articles published at `http://example.com/articles/` then you might have the JSON for those articles under `/content/articles/`. Each JSON document will contain the metadata required to render the published content, including a reference to the intended page template to be used for rendering:

```json
{
  "title": "My Whistlepost Site",
  "sling:resourceType": "wp/page/index",
  "show_advanced_settings": false,
  "jcr:primaryType": "nt:unstructured",
  "description": "",
  "author": ""
}
```

Whistlepost provides some default templates for content, however ultimately you can design content templates to match just about any structure that you require.

## Editors

Whilst some content can be sufficiently defined with plain text, sometimes there is a need
for richer formatting and layouts. To support such content Whistlepost provides a selection
of editors capable of capturing and rendering markup and rich content formats.

### Editor.js

TBD.

### Prosemirror

TBD.

### Mobiledoc

TBD.

## Structured Content

Whilst every Whistlepost site may choose to render content in unique ways, we can define
some common structured metadata that is typical for a particular type of page. Using common
types allows us to provide consistent formatting a layout of pages and page sections.

### Article

A news article is typically defined to include a tile, an abstract, a cover image, and a body of text.

### Recipe

A recipe consists of a title, an abstract, a cover image, a list of ingredients, and a method.

### Advertisement

An advertisement may consist of a title, a thumbnail image and a full-size image.

### Collection

A collection will consist of a title, a description, a page count (for paging resources), and a list of resources
included in the collection.

## Sitemap

TBD.
