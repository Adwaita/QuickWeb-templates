# Introduction
This document provides a short summary on quickweb templates organization, and lists the specific artifacts provided by this template.

The template/ directory should provide HTML files and related files which are not expected to be changed by the application developer.

HTML provided in this template:
    _global.html - top level HTML document to be used for every page
    _layout.html - extends the top level html with layout components (e.g. navigation var, footer)
    _navbar.html - navigation bar definition


The webroot/ directory should provide configurable options (.json/.yaml) for the template, and example content.

Configuration/content files provided in this template:
    _footer.yaml - footer html
    _global.yaml - top level HTML configuration
    _navbar.yaml - navigation bar content
    About.html - example about page
    idnex.html - example index page
