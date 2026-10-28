# kramdown

kramdown-dialect Markdown-to-HTML converter (superset of Markdown, inline attribute lists).

## Install

```bash
go get github.com/go-kramdown/kramdown
```

Requires Go 1.26.4 or newer. `CGO_ENABLED=0`.

## Task lists (GFM dialect)

Task lists (`- [x] done`, `- [ ] todo`) are not part of kramdown's own syntax: the
reference gem, and go-kramdown by default, print `[x]` literally. Select the GFM
dialect (`kramdown-parser-gfm`) to render checkboxes, byte-identical to the gem:

```go
o := kramdown.DefaultOptions()
o.Input = "GFM"
html := kramdown.ToHTML("- [x] done\n- [ ] todo\n", &o)
```

## Links

- Source: <https://github.com/go-kramdown/kramdown>
- API reference: <https://pkg.go.dev/github.com/go-kramdown/kramdown>

!!! note
    See the module's README for full, up-to-date details.
