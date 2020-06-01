# Problems

## Lost Images

Problem: Images are lost when converting if the image/figure is indented. For example, see <https://www.percona.com/doc/percona-monitoring-and-management/2.x/glossary-terminology.html#pmm-version>

Solution: Unindent the source material and re-export.

## Maintaining URLs and Bookmarks

Problem: Almost every section is independently bookmarked. These must be maintained to avoid breaking links into 
the documentation.

Some are standard ones:

`.. _PMM-version:`

Some are embedded in titles:

```
`PMM Version <glossary-terminology.html#pmm-version>`_
```

It is these ones that are visible in the HTML and bookmarkable.

Solution: 

1. Build a catalogue of existing bookmark names so they can be compared with migrated ones.
2. Should include paths to images.
3. Make sure all titles use the same bookmarks.


## Tables

Tables don't export properly from sphinx's MD exporter.

Problem: There are not many but even the basic form of reST table fails to convert properly.

Solutions: 

- Manually fix them? 
- Convert them into CSV and use <https://github.com/timvink/mkdocs-table-reader-plugin>

