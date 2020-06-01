# Themes

There are two built-in themes and a number of community ones.

You can extend existing themes or build one from scratch.

Here are the best ones.

!!! note
    Current theme: {{ config.theme.name }}

## Material

- Theme: `mkdocs-material` <https://squidfunk.github.io/mkdocs-material/>
- Test: **PASS**

### Install

```bash
pip3 install mkdocs-material
```

### Configure

```yaml
theme: 
    name: material
    palette:
        scheme: default
        primary: indigo
        accent: indigo
    font:
        text: Roboto
        code: Roboto Mono
    icon:
        logo: logo
    favicon: assets/favicon.png
    navigation_depth: 2
```

## Bootswatch

- Theme(s): `mkdocs-bootswatch` <https://mkdocs.github.io/mkdocs-bootswatch/>
- Test: **PASS**

!!! note
    Comes with a number of colour schemes.

### Install

```bash
pip3 install mkdocs-bootswatch
```

### Configure

```yaml
theme: THEME
```

THEME can be one of:

-    cerulean
-    cosmo
-    cyborg (dark)
-    darkly (dark)
-    flatly
-    journal
-    litera
-    lumen
-    lux
-    materia (material styling)
-    minty
-    pulse
-    sandstone
-    simplex
-    slate (dark)
-    solar (dark)
-    spacelab
-    superhero (dark)
-    united (Ubuntu styling)
-    yeti


`nav_style` can be separately changed from default `primary` to `dark` or `light`. Example:

```yaml
theme:
  name: cosmo
  nav_style: dark
```

## Bootstrap

- Theme: `mkdocs-bootstrap` <https://mkdocs.github.io/mkdocs-bootstrap/>
- Test: **FAIL** Doesn't render properly

### Install

```
pip3 install mkdocs-bootstrap
```

### Configure

```
theme:
    name: bootstrap
```

# Extending Themes

For simple changes such as typeface and colours, use CSS files.

```
extra_css:
  - css/mytheme.css
```
