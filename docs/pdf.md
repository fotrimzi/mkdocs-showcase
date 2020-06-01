# Creating PDF Output

[Option 1](#option-1-mkdocs-mk2pdf-plugin)

- Plugin: <https://github.com/HaoLiuHust/mkdocs-mk2pdf-plugin>
- Test: **FAIL** Some bug fixes needed:

in plugin.py, change `utils.string_types` to `str`
in renderer.py change `latex-engine` to `pdf-engine`

[Option 2](#option-2-mkdocs-pdf-export-plugin)

- Plugin: <https://github.com/zhaoterryy/mkdocs-pdf-export-plugin>
- Test: **PASS**

## About

Sphinx excels at creating multi-format outputs, including LaTeX to create
properly typeset PDF documents.

## Option 1 - mkdocs-mk2pdf-plugin

### Install

```
pip3 install mkdocs-mk2pdf-plugin
```

### Configure

```
plugins:
    - mk2pdf-export:
        enabled_if_env: ENABLE_PDF_EXPORT
```



## Option 2 - mkdocs-pdf-export-plugin

- Ref: <https://github.com/zhaoterryy/mkdocs-pdf-export-plugin>
- Uses <http://weasyprint.org/> Install: <https://weasyprint.readthedocs.io/en/latest/install.html>

!!!note
   Can only use [material theme](https://github.com/squidfunk/mkdocs-material).

### Install

```
brew install cairo pango gdk-pixbuf
pip3 install weasyprint
pip3 install mkdocs-pdf-export-plugin
```

### Configure

```
plugins:
    - search
    - pdf-export
    - combined: true
```

For further styling, use CSS:

```css
@page {
    size: a4 portrait;
    margin: 25mm 10mm 25mm 10mm;
    counter-increment: page;
    font-family: "Roboto","Helvetica Neue",Helvetica,Arial,sans-serif;
    white-space: pre;
    color: grey;
    @top-left {
        content: '© 2018 My Company';
    }
    @top-center {
        content: string(chapter);
    }
    @top-right {
        content: 'Page ' counter(page);
    }
}
```

Add the file name to `extra_css`.

Reference: <https://drafts.csswg.org/css-page-3/>
