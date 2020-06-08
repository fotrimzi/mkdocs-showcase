# Admonitions

- Sphinx reference: <https://docutils.sourceforge.io/docs/ref/rst/directives.html#admonitions>
- Markdown reference: <https://python-markdown.github.io/extensions/admonition/>

## Notes

Admonition keywords are HTML `class` identifiers, so can be anything.

Most themes stylise common keywords, or they customised by overriding the style for `<div class="admonition TYPE">`.

Example: This project's `docs/css/extra.css`:

```css
{% include 'css/extra.css' %}
```

And in `mkdocs.yml`:

```yaml
extra_css:
  - css/extra.css
```

See 'mindblowing' example below.

## Install & Configure

Already installed by MkDocs.

```yaml
markdown_extensions:
    - admonition
```

## Usage

!!! tip
    The admonition body text must align with the first letter of the label.


```md
!!! note
    Here is a note.
    
    It can be multi-lined.
    
    With an empty line between.
    
    - And bullets
    - are possible.
```

!!! note
    Here is a note.
    
    It can be multi-lined.
    
    With an empty line between.
    
    - And bullets
    - are possible.

```md
!!! note "Please note"
    You can change the title.
```

!!! note "Please note:"
    You can change the title.

```md
!!! mindblowing
    Some mindblowing statement

!!! caution
    Caution

!!! danger
    Dangerous

!!! important
    Important

!!! attention
    Attention

!!! error
    Error

!!! hint
    Hint
```

!!! mindblowing
    Some mindblowing statement

!!! caution
    Caution

!!! danger
    Dangerous

!!! important
    Important

!!! attention
    Attention

!!! error
    Error

!!! hint
    Hint
