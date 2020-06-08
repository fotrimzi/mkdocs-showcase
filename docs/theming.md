# Themes

There are two built-in themes and a number of community ones.

You can extend existing themes or build one from scratch.

Here are some of the more popular ones.

!!! note "Current theme: {{ config.theme.name }}"

## Material

Reference: <https://squidfunk.github.io/mkdocs-material/>

### Install & Configure

```bash
pip3 install mkdocs-material
```

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
    logo: logo
    favicon: assets/favicon.png
    navigation_depth: 2
```

### Notes

- `logo` is a path to a `.svg` file.

## Bootswatch

Reference: <https://mkdocs.github.io/mkdocs-bootswatch/>

!!! note
    Comes with a number of colour schemes.

### Install & Configure

```bash
pip3 install mkdocs-bootswatch
```

```yaml
theme: THEME
```

Where THEME is one of:

-    `cerulean`
-    cosmo
-    `cyborg` (dark)
-    `darkly` (dark)
-    `flatly`
-    `journal`
-    `litera`
-    `lumen`
-    `lux`
-    `materia` (material styling)
-    `minty`
-    `pulse`
-    `sandstone`
-    `simplex`
-    `slate` (dark)
-    `solar` (dark)
-    `spacelab`
-    `superhero` (dark)
-    `united` (Ubuntu styling)
-    `yeti`


`nav_style` can be separately changed from default `primary` to `dark` or `light`. Example:

```yaml
theme:
  name: cosmo
  nav_style: dark
```

## Extending Themes

For simple changes such as typeface and colours, use CSS files.

```
extra_css:
  - css/mytheme.css
```

For layout, override various parts of the page with your own versions.

For example, see this project's `theme/partials/footer.html` -- a copy of
the original with the "Made with.." text commented out.

Reference: <https://www.mkdocs.org/user-guide/custom-themes/>
