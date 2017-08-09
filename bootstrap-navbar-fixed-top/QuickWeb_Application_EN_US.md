
# QuickWeb Application Structure

## Startup
During application startup, content from the 'webroot' directory will be scanned, and directories/files will be mapped to features and urls per the following rules.

### Static files
Content from directories which contain a file named '.static' will be served statically. This should be used for images, css, js and other downloadable static artifacts.

### Template based content (HTML/Markdown)
*.html and *.md files will be mapped to the quickweb template engine handler. Their names «without the extension» will be used for the url mapping. Filenames with a leading '_' will be ignored, they should be used for fragments which can be included by other templates. All templates will be automatically extended from a '\_base.html' template «unless they contain an explicit extend».

    e.g. webroot/About.html will be available as /About

### Controllers
*.py files will be mapped to python code http handlers, their names «without the extension» will be used for the url mapping.

    e.g: webroot/Calc.py will be available as /Calc/

### Navigation
When found, the file '_navigation.yaml' must contain the links and optionally the links titles that should be provided on the navigation component.