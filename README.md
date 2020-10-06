# mkdocs-showcase - MkDocs showcase/demo site with feature usage notes and examples

A small site exploring various features of MkDocs and comparing them with their equivalents
in Sphinx.

To see it, run it via a Docker container, or install MkDocs and dependencies on your own host.


## To run via [Docker](https://docs.docker.com/engine/install/):

- Clone this repository
- `cd mkdocs-showcase`
- `docker run --rm -it -p 8000:8000 -v $(pwd):/mkdocs pauljacobspercona/mkdocs-showcase`
- Open <http://localhost:8000> in a browser

## To install MkDocs

### Install Prerequisites

(Debian/Ubuntu):
   
```bash
sudo apt install -y python3 python3-pip
```

(For other platforms, see <https://www.python.org/downloads/>.)

### Check Prerequisites

```bash
python3 --version # >= 3.5
pip3 --version # >= 20.0.2
```

### Install MkDocs and Extensions, Plugins, and Themes

```bash
pip3 install mkdocs mkdocs-exclude mkdocs-macros-plugin mkdocs-material mkdocs-mermaid2-plugin mkdocs-redirects mkdocs-table-reader-plugin mkdocs-with-pdf markdown-svgbob plantuml-markdown pygments pymdown-extensions
```

### Run MkDocs

```bash
cd mkdocs-showcase
mkdocs serve
```

View the documentation by opening <http://localhost:8000> in a browser.

### Build documentation

To create a stand-alone static website:

```bash
mkdocs build
```

Open `site/index.html` in your browser.
