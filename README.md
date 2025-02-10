# National PID recommendations for research - Sweden

This repository is for collaborative work on creating recommendations for persistent identifiers (PIDs)
used in the research sector.

The partnering organisations having been involved in this work this far are:
- Swedish National Data Service
- Swedish Research Council
- National Library of Sweden
- SciLifeLab

## About this repository

The repository contains the sources to build a web resource using the static site generator MkDocs.

Texts may be edited as individual Markdown (.md) files.
If you know the basics of Markdown you should have no trouble editing or suggesting changes.

References are handled in BibTeX format and the source file is in *refs.bib*.

## Instructions for building the static site

If you want to build the web resource locally you may do so by installing a MkDocs environment:

1. Install a basic Python 3 environment on your operating system of choice. Install the *virtualenv* package if not already available.
2. Using the shell, make a virtual environment for MkDocs in a folder of your choice (you may of course pick something other than *my-pid-site*):

`python3 -m venv my-pid-site`

3. Activate the virtual environment in your shell (OS/shell dependent):

Unix-compatible:

`source my-pid-site/bin/activate`

Windows:

`.\my-pid-site\Scripts\activate`

4. Install the requirements using pip (make sure the venv is activated first):

`pip3 install mkdocs mkdocs-bibtex mkdocs-windmill`

5. Navigate to the folder where the repository has been cloned or pulled.

To update HTML files with the latest changes:
`mkdocs build`

To host a local web server with the latest changes:
`mkdocs serve`
The address to the local web site should appear in the shell window i.e. `Serving on http://127.0.0.1:8000/`

If you are using `mkdocs serve` local changes should be updated automatically when refreshing the browser.