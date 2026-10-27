# WDCTS 華府台灣學校 — new website preview (v1)

Static redesign of https://wdcts.org — six pages: Home, Programs, Admissions, Calendar, Student Life, About.
Plain HTML + images, no build step. Served with GitHub Pages.

## Design source (`design/`)

`design/*.dc.html` are the source files of the Claude design canvas ("WDCTS 首頁三風格", A-version pages + mobile wrappers) and `design/canvas.json` is its layout index. The site pages are exported from them:

| Canvas source | Site page |
|---|---|
| `Main.dc.html` | `index.html` |
| `Programs.dc.html` | `programs.html` |
| `Admissions.dc.html` | `admissions.html` |
| `Calendar.dc.html` | `calendar.html` |
| `StudentLife.dc.html` | `student-life.html` |
| `About.dc.html` | `about.html` |

Export differences (expected): `*.dc.html` links → `*.html`, `/_blob/<id>` images → `images/…`, `{{accent}}` → `#B8432F`, plus `<head>` meta tags and `target="_blank"` on external links.

**Rule: every design change goes into both the `.dc.html` source and the matching `.html` page in the same commit,** and the canvas is republished from `design/` after merging to `main`.

## Design review

`.claude/skills/design-taste-frontend/` (tasteskill v2) — see `VENDORED.md` there for the brand exceptions (palette, tile motif).
