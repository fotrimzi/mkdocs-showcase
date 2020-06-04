# Tables

Reference: <https://github.com/timvink/mkdocs-table-reader-plugin>

## Install & Configure

```bash
pip3 install mkdocs-table-reader-plugin
```

```yaml
plugins:
  - search
  - table-reader
```

!!! important
    Conflict with `macros` plugin, so must be declared before it.

## Usage

{% raw %}
``{{`` ``read_table('docs/features.csv', sep=',')`` ``}}``
{% endraw %}

{{ read_table('docs/features.csv', sep=',') }}
