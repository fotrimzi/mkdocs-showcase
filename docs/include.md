# Including Files

Reference: <https://pypi.org/project/mkdocs-macros-plugin>

## Notes

The `macros` plugin includes a general file include feature.

### Install & Configure

```bash
pip3 install mkdocs-macros-plugin
```

In `mkdocs.yml`:

```yaml
plugins:
    - search
    - macros
```

### Usage

{% raw %}
```
{% include '_include/include-me.md' %}
```
{% endraw %}

{% include '_include/include-me.md' %}

!!! note
    Must be a plugin listed after `table-reader`.
