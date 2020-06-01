# Including Files

Reference: <https://pypi.org/project/mkdocs-macros-plugin>

## Notes

The `macros` plugin includes a general file include feature.

### Install & Configure

See [replacements](replacements.md#install).

### Usage

{% raw %}
```
{% include '_include/include-me.md' %}
```
{% endraw %}

{% include '_include/include-me.md' %}

!!! note
    Must be a plugin listed after `table-reader`.
