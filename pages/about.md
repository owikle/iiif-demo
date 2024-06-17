---
title: About
layout: about
permalink: /about.html
# include CollectionBuilder info at bottom
credits: true
# Edit the markdown on in this file to describe your collection
# Look in _includes/feature for options to easily add features to the page
---

{% include feature/jumbotron.html objectid="objects/PC004934.jpg" %} 

## About CollectionBuilder-CSV and IIIF

This is a CollectionBuilder-CSV template featuring single- and multi-page IIIF objects displayed in Universal Viewer.

Paths to IIIF manifests can be added to metadata as the value for object_location field.
Thumbs and smalls can use IIIF Image API values or other paths to thumb and small objects within or outside the repository.
object_location can either include links to json manifest files that are hosted outside the repository (sometimes can cause CORS issues), or the manifest files can be downloaded and placed in the CB repo's objects folder and their paths used for object_location values.
There is a mix of both cases in this collection.

In the case of this repository, a demo iiif layout was created (`_layouts/iiif.html`) which includes the Universal Viewer code (`_includes/item/iiif-manifest-universal-viewer.html`).
Objects then are displayed using Universal Viewer if their display_template value is `iiif`.

Alternately, in `_layouts/image.html` one could swap out `{% raw %}{% include item/image-gallery.html %}{% endraw %}` for `{% raw %}{% include item/iiif-manifest-universal-viewer.html %}{% endraw %}` and all objects with display_template value `image` would be displayed in Universal Viewer, provided that they have a IIIF manifest as their value for object_location.