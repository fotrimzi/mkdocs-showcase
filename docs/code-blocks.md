# Code Blocks

*Code blocks with options for syntax highlighting, line numbering, collapsing.*

- Sphinx references:
    - [`code-block`](https://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html#directive-code-block)
    - [`literalinclude`](https://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html#directive-literalinclude)

- MkDocs references:
    - [Fenced code blocks](https://python-markdown.github.io/extensions/fenced_code_blocks/)
    - [SuperFences](https://facelessuser.github.io/pymdown-extensions/extensions/superfences/)
    - [Tabbed blocks](https://facelessuser.github.io/pymdown-extensions/extensions/tabbed/)

## Fenced code blocks

### Install & Configure

MkDocs activates the extension by default, so no action is needed.

### Usage

Delimit code blocks with:

1. 3 backticks (standard)
2. Using [PHP Markdown syntax](https://michelf.ca/projects/php-markdown/extra/#fenced-code-blocks)

## SuperFences

This extension properly indents code blocks in lists.

### Install & Configure

```bash
brew install pygments
pip3 install pymdown-extensions
```

!!!note
   This installs the entire set of [PyMdown extensions](https://facelessuser.github.io/pymdown-extensions/).

```yaml
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

## Syntax Highlighting

Reference: <https://facelessuser.github.io/pymdown-extensions/extensions/highlight/>

### Install & Configure

```yaml
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

*Commonly used to show the same code or commands for different platforms
without cluttering the layout.*

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
