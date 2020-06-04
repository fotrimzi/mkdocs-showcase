{%set mylocalvar = "***the value of my local var***" %}

# Replacements (Variables, Substitutions)

Reference: <https://pypi.org/project/mkdocs-macros-plugin/>

## Notes

Sphinx has the `.. replace::` directive to create replaceable string tokens.

The equivalent in markdown/MkDocs can be done with the `macros` plugin.

## Install & Configure

```bash
pip3 install mkdocs-macros-plugin
```

In `mkdocs.yml`:

```yaml
plugins:
    - search
    - macros


extra:
  test:
    value1: VALUE-ONE
    value2: VALUE-TWO
```

or


In `mkdocs.yml`:

```yaml
plugins:
    - search
    - macros:
        include_yaml: ['extra.yml']
```

In `extra.yml`:

```yaml
extra:
  test:
    value1: VALUE-ONE
    value2: VALUE-TWO
```

## Usage

Values for:

- `test.value1`: {{test.value1}}
- `test.value2`: {{test.value2}}

!!! warning
    Badly-formed keys or expansions will cause build errors.
