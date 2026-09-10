# ahemtiaz.github.io

Source for my academic homepage: <https://ahemtiaz.github.io>

Hand-written HTML and CSS. No framework, no build step, no dependencies — edit
`index.html` or `style.css`, commit, push, and GitHub Pages serves it.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole page. Sections: hero, news, publications, research, experience, projects, education. |
| `style.css` | All styling. Theme tokens live at the top of the file. |
| `cv.pdf` | Compiled CV, linked from the hero and footer. **Replace this whenever you update `resume.tex`.** |

## Editing notes

- **Theme.** Light is the base definition on `:root`. Dark is defined twice: once
  under `@media (prefers-color-scheme: dark)` (guarded so a manual light choice
  wins) and once under `:root[data-theme="dark"]` (so the toggle wins). If you
  add a colour, define it in all three places or it will break in one mode.
- **News.** Newest first. Keep it to four or five items — a stale news list is
  worse than none.
- **Publications.** Tags are `[C#]` for conference/workshop and `[J#]` for
  journal, matching `resume.tex`. Keep the two in sync.
- **Adding a publication:** copy an `<article class="pub">` block, and remember
  `<span class="me">` around your own name and `<span class="badge">` for status.

## Local preview

```bash
python -m http.server 8099
```

Then open <http://localhost:8099>.
