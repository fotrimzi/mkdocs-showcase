# Code Blocks

## Built-In

Reference: [built-in](https://python-markdown.github.io/extensions/fenced_code_blocks/)

### Install & Configure

Fenced code blocks are already included in MkDocs as a markdown extension.

### Usage

!!!tip
   Code with double curly braces should be
   bounded with 

   {% raw %}
   ```
   {% raw %} {{ something }} ... {% endraw % }
   ```
   {% endraw %} 


   to prevent interpretation.


## SuperFences

Reference: <https://facelessuser.github.io/pymdown-extensions/extensions/superfences/>

This extension properly indents code blocks in lists.

### Install & Configure

```bash
brew install pygments
pip3 install pymdown-extensions
```

!!!note
   This installs the entire set of PyMdown extensions.

```
markdown_extensions:
    - pymdownx.superfences
```

### Usage

1. List item

    ```text
    # An indented code block
    ```
   
2. Another item

    ```text
    # Another indented text block
    ```

## Highlight

Reference: <https://facelessuser.github.io/pymdown-extensions/extensions/highlight/>

### Install & Configure

```
markdown_extensions:
    - pymdownx.highlight:
        linenums: true
```

### Usage

```bash
# here is a test
time ls -lRt
```

```
my_yaml:
  - unhighlighted_yaml
```

```yaml
my_yaml:
  - highlighted_yaml
```

## Tabbed blocks

Reference: <https://facelessuser.github.io/pymdown-extensions/extensions/tabbed/>


### About

Tabbed blocks are commonly used show the same code or commands for different platforms
without cluttering the layout.

### Install & Configure

```
markdown_extensions:
    - pymdownx.tabbed
```

### Usage

```
=== "macOS"
    Some code
=== "Ubuntu"
    Some code

===! "Tab A"
    Different tab set.

=== "Tab B"
    More content.
```

=== "macOS"
    Something for macOS
=== "Ubuntu"
    Something for Ubuntu

===! "Tab A"
    A different tab set.

=== "Tab B"
    More content.
