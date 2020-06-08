# mkdocs-showcase - MkDocs showcase/demo site with feature usage notes and examples

## Install

### Install Prerequisites

(Debian/Ubuntu):
   
```bash
sudo apt install -y python3 python3-pip
```

For other platforms, see <https://www.python.org/downloads/>

### Check Prerequisites

```bash
python3 --version # >= 3.5
pip3 --version # >= 20.0.2
```

### Install MkDocs and Extensions, Plugins, and Themes

```bash
pip3 install mkdocs
pip3 install mkdocs-exclude
pip3 install mkdocs-macros-plugin
pip3 install mkdocs-material
pip3 install mkdocs-redirects
pip3 install mkdocs-table-reader-plugin
pip3 install pymdown-extensions
pip3 install pygments
```

### Run MkDocs

```bash
cd mkdocs-showcase
mkdocs serve
```

### View the documentation

Open <http://localhost:8000>

### Build documentation

To create a stand-alone static website:

```bash
mkdocs build
```

Open `site/index.html` in your browser.

