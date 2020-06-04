# Redirects

Reference: <https://pypi.org/project/mkdocs-redirects>

## Notes

Redirects are needed to avoid diminished domain ranking 
caused by broken links (references to URLs that no longer exist),
in turn resulting from moved or renamed files.

## Install & Configure

```bash
pip3 install mkdocs-redirects
```

```yaml
plugins:
    - redirects:
        redirect_maps:
            'old.md': 'new.md'
            'old/file.md': 'new/file.md'
            'some_file.md': 'http://external.url.com/foobar'
```

## Usage

Example configuration:

```
plugins:
    - redirects:
        redirect_maps:
          'doesnotexist.md': 'redirects.md'
```

Open <http://localhost:8000/doesnotexist.html> in another browser window.

It will redirect to this page.


Confirm by opening <http://localhost:8000/reallydoesnotexist.html> 
which will render a 404 page.
