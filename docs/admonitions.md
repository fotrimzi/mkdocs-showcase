# Admonitions

Reference: <https://python-markdown.github.io/extensions/admonition/>

## Notes

The keywords are HTML `class` identifiers, so can be anything.

Most themes stylise common keywords, or they customised by overriding the style for `<div class="admonition TYPE">`.

Example:

```css
/* Custom styling for admonitions */
div.mindblowing .admonition-title {
    background-color: #ffff2f;
    font-size: 4em;
}
div.caution .admonition-title {
    background-color: #aa0303;
    color: #ffffff;
    font-size: 2em;
}
```

## Install & Configure

Already installed by MkDocs.

```yaml
markdown_extensions:
    - admonition
```

## Usage

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