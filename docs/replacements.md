{%set mylocalvar = "***the value of my local var***" %}

# Replacements

Reference:

- `macros` <https://pypi.org/project/mkdocs-macros-plugin/>
- `extradata plugin` <https://github.com/rosscdh/mkdocs-markdownextradata-plugin>

## macros

Advantages:

- Parameterised replacements
- Local values in md file: `mylocalvar` is set in this file and expands to: {{ mylocalvar }}
- Include files

### Install & Configure

```bash
pip3 install mkdocs-macros-plugin
```


```yml
plugins:
    - search
    - macros
```

### Usage

!!! Warning
    Can't use both `macros` and `markdownextradata`

## markdownextradata

Advantages:

- Can import key/values from external file
- Localised definitions: key/values live in `.yml` file in same directory (needs testing).


### Install & Configure

```bash
pip3 install mkdocs-markdownextradata-plugin
```

```yaml
plugins:
    - search
    - markdownextradata
    
extra:
    version: X.Y.Z
    keyword: value
```

or in external files: (not tested)

```
plugins:
    - search
    - markdownextradata:
        data: path/to/datafiles
```

## Usage

Values for:

- `test.value1`: {{test.value1}}
- `test.value2`: {{test.value2}}

!!! warning
    Badly-formed keys or expansions will cause build errors.
