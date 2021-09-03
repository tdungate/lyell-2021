### Digitized Gutenberg Bibles for the 2021 Lyell lectures

Small static (Jekyll) site for gathering together and viewing digitized Gutenberg Bibles, to accompany the Bodleian's [2021 Lyell Lectures](https://visit.bodleian.ox.ac.uk/event/the-lyell-lectures-2021). Runs as a [GitHub Page](https://pages.github.com/).

### Pages

* Index page with information and list of IIIF Gutenberg Bibles
* View page (`/view`), with a [Mirador](https://github.com/ProjectMirador/mirador) workspace containing all digitized bibles. None open by default, but can be passed a IIIF manifest using `manifest` to open with an object.

### Viewer

`/view/`embeds the UMD Version of Mirador (see [Mirador Docs](https://github.com/ProjectMirador/mirador/wiki/M3-Embedding-in-Another-Environment#in-an-html-document-with-javascript)). Uses the `_layouts/view.html` page layout, which loads the Mirador UMD and embeds `_includes/viewer.html`. This `include` sets up Mirador, and populates the workspace with IIIF manifests from `_data/manifests.json` (which should be a IIIF collection).

The `viewer.html` include also contains lines to allow a manifest to be passed to the viewer, using a `manifest` parameter.

### Styling

Uses default GitHub Pages styling, plus a custom footer.