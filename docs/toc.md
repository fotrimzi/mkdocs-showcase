# Tables of Contents (ToC)

- Sphinx reference: <https://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html#directive-toctree>
- Markdown reference: <https://python-markdown.github.io/extensions/toc/>

## Notes

MkDocs ToC is defined in one place, in the `nav:` element of the `mkdocs.yml` file.
For large numbers of files, this can be overwhelming.

Compare with Sphinx which distributes ToC definitions (as files containing `toctree`) 
across the document set. This makes it easier to organise groups of 
document subsets, either as directories each having their own `index.rst` file, or with several
files with distinct `toctree` elements. But it is harder to keep track of the document structure 
(the global section Toc).

!!! note "No global TOC"

    The `[TOC]` element only lists heading in a page.

    There is no global (site-wide) ToC available without coding.

## Install & Configure

```yaml
markdown_extensions:
    - toc:
        baselevel: 2
        toc_depth: 2
```

Options:

- `permalink`: Set to `True` to enable the permalink character (at end of title text). Default is `&para;`. Value can be a character instead.

- `permalink_title`: Text to show when hovering over permalink.

 - `anchorlink`: Set `True` to make all headings self-link (PMM style).
 
Setting `baselevel: 0` and `toc_depth: 1` gives the same results
as Sphinx but the main title is no longer a heading. The solution is:

```yaml
    - toc:
        baselevel: 1
        toc_depth: "2-2"
```
