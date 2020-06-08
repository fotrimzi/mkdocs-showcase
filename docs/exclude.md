# Excluding Files

Reference: <https://github.com/apenwarr/mkdocs-exclude>

## Notes

MkDocs scans `docs` and warns about any markdown files not in `nav:`.

We can explicitly ignore these with an exclude pattern.

!!! note
    An alternative is to explicitly include required files using <https://github.com/supcik/mkdocs-select-files>

## Install & Configure

```bash
pip3 install mkdocs-exclude
```

```yaml
plugins:
  - exclude:
      glob:
        - exclude/this/path/*
        - "*.tmp"
        - "*.pdf"
        - "*.gz"
      regex:
        - '.*\.(tmp|bin|tar)$'
```
