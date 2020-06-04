# References and Links

!!! see "See also"
    [redirects](redirects.md)

## Notes

All files and section headers in a file are accessible by default.

To make a section anchor, section titles down-cased, punctuation is removed,
and spaces are replaced with the separator character.

For example: (Section text at end of file:)

```md
# 1. A TEST SECTION
A test section linked from above.
Some test content.

Lorem ipsum ...
```

and can be accessed in the same document with:

```md
[Link to bookmark text](#1-a-test-section)
```

[Link to bookmark text](#1-a-test-section)


## Permalinks 

Permalinks are symbols at the end of section titles linking directly to that page and section.

MkDocs lets you turn this on or off, and choose the symbol.

### Configuration

Reference: <https://python-markdown.github.io/extensions/toc/>

```yaml
markdown_extensions:
    - toc:
        permalink: True
        permalink_title: Link to this section
        anchorlink: True
        separator: "_"
```

- `anchorlink` - Makes titles links to themselves.
- `permalink_title` - Tool-tip text for the permalink.
- `separator` - Character to replace spaces with (default `-`).









## 1. A TEST SECTION
A test section linked from above.
Some test content.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. <a href="http://loripsum.net/" target="_blank">Expectoque quid ad id, quod quaerebam, respondeas.</a> Cum ageremus, inquit, vitae beatum et eundem supremum diem, scribebamus haec. Sed nimis multa. At coluit ipse amicitias. Collatio igitur ista te nihil iuvat.

Ergo adhuc, quantum equidem intellego, causa non videtur fuisse mutandi nominis. <a href="http://loripsum.net/" target="_blank">Quorum sine causa fieri nihil putandum est.</a> Septem autem illi non suo, sed populorum suffragio omnium nominati sunt. Summus dolor plures dies manere non potest? <mark>Hoc loco tenere se Triarius non potuit.</mark> Quodsi ipsam honestatem undique pertectam atque absolutam. Omnia contraria, quos etiam insanos esse vultis. Quamquam ab iis philosophiam et omnes ingenuas disciplinas habemus;

<mark>Duo Reges: constructio interrete.</mark> <a href="http://loripsum.net/" target="_blank">Paria sunt igitur.</a> De quibus cupio scire quid sentias. Id est enim, de quo quaerimus. Quo modo autem optimum, si bonum praeterea nullum est? Ut in geometria, prima si dederis, danda sunt omnia.

