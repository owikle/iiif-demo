# CollectionBuilder-CSV and IIIF

This is a CollectionBuilder-CSV template featuring single- and multi-page IIIF objects displayed in Universal Viewer.

Paths to IIIF manifests can be added to metadata as the value for object_location field.
Thumbs and smalls can use IIIF Image API values or other paths to thumb and small objects within or outside the repository.
object_location can either include links to json manifest files that are hosted outside the repository (sometimes can cause CORS issues), or the manifest files can be downloaded and placed in the CB repo's objects folder and their paths used for object_location values.
There is a mix of both cases in this collection.

In the case of this repository, a demo iiif layout was created (`_layouts/iiif.html`) which includes the Universal Viewer code (`_includes/item/iiif-manifest-universal-viewer.html`).
Objects then are displayed using Universal Viewer if their display_template value is `iiif`.

Alternately, in `_layouts/image.html` one could swap out `{% include item/image-gallery.html %}` for `{% include item/iiif-manifest-universal-viewer.html %}` and all objects with display_template value `image` would be displayed in Universal Viewer, provided that they have a IIIF manifest as their value for object_location.

----------

## CollectionBuilder 

<https://collectionbuilder.github.io/>

CollectionBuilder is a project of University of Idaho Library's [Digital Initiatives](https://www.lib.uidaho.edu/digital/) and the [Center for Digital Inquiry and Learning](https://cdil.lib.uidaho.edu) (CDIL) following the [Lib-Static](https://lib-static.github.io/) methodology. 
Powered by the open source static site generator [Jekyll](https://jekyllrb.com/) and a modern static web stack, it puts collection metadata to work building beautiful sites.

The basic theme is created using [Bootstrap](https://getbootstrap.com/).
Metadata visualizations are built using open source libraries such as [DataTables](https://datatables.net/), [Leafletjs](http://leafletjs.com/), [Spotlight gallery](https://github.com/nextapps-de/spotlight), [lazysizes](https://github.com/aFarkas/lazysizes), and [Lunr.js](https://lunrjs.com/).
Object metadata is exposed using [Schema.org](http://schema.org) and [Open Graph protocol](http://ogp.me/) standards.

Questions can be directed to **collectionbuilder.team@gmail.com**

## License

CollectionBuilder documentation and general web content is licensed [Creative Commons Attribution-ShareAlike 4.0 International](http://creativecommons.org/licenses/by-sa/4.0/). 
This license does *NOT* include any objects or images used in digital collections, which may have individually applied licenses described by a "rights" field.
CollectionBuilder code is licensed [MIT](https://github.com/CollectionBuilder/collectionbuilder-csv/blob/master/LICENSE). 
This license does not include external dependencies included in the `assets/lib` directory, which are covered by their individual licenses.
