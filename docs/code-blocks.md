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

This extension allows code blocks to be properly indented in lists.

## Install & Configure

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

## Usage

1. List item

    ```bash
    cd code-directory
    ls
    ```
   
2. Another item

    ```text
    another indented text block
    ```

## Highlight

- Extension: `codehilite`

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
  - unformatted_yaml
```

```yaml
my_yaml:
  - formatted_yaml
```

## CodeHilite

!!!note
   Don't use if already using PyMdown extensions.

Reference: <https://python-markdown.github.io/extensions/code_hilite/>

### Install & Configure

```yaml
markdown_extensions:
    - codehilite:
        linenums: true
```

## Tabbed blocks

[Tabbed blocks](#tabbed-blocks)

- Extension: `pymdownx.tabbed`
- Test: 


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
    ```
    brew install ...
    ```

=== "Ubuntu"
    ```
    apt install ...
    ```

=== "Windows"

    No such command



===! "Tab A"
    Different tab set.

=== "Tab B"
    More content.


## Executable code

==TODO==

Code can be run and the output shown with <https://pheasant.daizutabi.net/>


