# Instruction for a Door

A fictional self-help book.

Fiction. 2026.

## Read

A tagged release carries the typeset PDF and a single-file HTML edition:

<https://github.com/summeroff/instruction_for_a_door/releases>

## Source

`book_instruction_for_a_door.tex` is the book. PDF and HTML are both built from that file.

```bash
latexmk -pdf book_instruction_for_a_door.tex
```

HTML front matter (cover, type, theme) lives in `web/template.html`. The workflow strips the `% HTML-SKIP-BEGIN` / `% HTML-SKIP-END` region before Pandoc so the PDF title page is not dumped into the HTML as raw paragraphs. The book text is not rewritten for either format.

## Release

Push a `v*` tag from `master`. GitHub Actions compiles the PDF, builds the HTML, and publishes a GitHub Release with both files attached.

```bash
git tag -a v1.0.0 -m "Instruction for a Door v1.0.0"
git push origin v1.0.0
```

A tag containing `-` is marked as a prerelease.

## Note

This is fiction. It includes strong language and sex. The narrator's theories are his. They are not advice.

## License

MIT. See [LICENSE](LICENSE).
