# Symbols & Icons

Reference: 

- <https://python-markdown.github.io/extensions/smarty/>
- <https://facelessuser.github.io/pymdown-extensions/extensions/smartsymbols/>

## Notes

Certain markdown consrtucts can be automatically recognised and converted into symbols.

For example, `---` renders an [em-dash](https://en.wikipedia.org/wiki/Dash#Em_dash).

There are two extensions. They can be used together.

## Install & Configure

### Smarty

`smarty` is already installed by MkDocs.

In `mkdocs.yml`:

```yaml
markdown_extensions:
    - smarty
```

### SmartSymbols

```yaml
markdown_extensions:
    - pymdownx.smartsymbols
```

## Usage

Smarty will replace these into typographical HTML entity equivalents:

```
' (Single quotes) '

" (Double quotes) "

<< (Chevrons/angled quotes) >>

... (ellipsis)

-- (en-dash)

--- (em-dash)
```

' (Single quotes) '

" (Double quotes) "

<< (Chevrons/angled quotes) >>

!!! note
    Angle quotes conversion is off by default. See this project's `mkdocs.yml` file.

... (ellipsis)

-- (en-dash)

--- (em-dash)





SmartSymbols will replace these symbols
with typographical equivalents.

(All are converted by default. Each can be independently suppressed with options
to the plugin.)

```
(tm) (Trademark)

(c) (Copyright)

(r) (Registered)

c/o (Care of/carry over)

+/- (Plus/Minus)

--> (Right arrow)

<-- (Left arrow)

<--> (Double arrow)

=/= (Not equals)

1/4, 1/2, 1/3, etc. (Fractions)

1st, 2nd, etc. (Superscripted ordinal numerals)

```

(tm) (Trademark)

(c) (Copyright)

(r) (Registered)

c/o (Care of/carry over)

+/- (Plus/Minus)

--> (Right arrow)

<-- (Left arrow)

<--> (Double arrow)

=/= (Not equals)

1/4, 1/2, 1/3, etc. (Fractions)

1st, 2nd, etc. (Superscripted ordinal numerals)


## Emoticons

Reference: [Short codes](https://emojipedia.org)

### Install & Configure

```sh
pip3 install pymdown-extensions
```

```yaml
markdown_extensions:
    - pymdownx.emoji
```

### Usage

```
:smile:

:information_source:

:warning:

:gear:

:traffic_light:

:hammer:
```



:smile:

:information_source:

:warning:

:gear:

:traffic_light:

:hammer:

