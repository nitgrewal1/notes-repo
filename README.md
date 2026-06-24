# Notes

Personal knowledge base — cybersecurity, finance, and mythology notes, mixing Markdown writeups with interactive HTML tools.

## Structure

| Folder                                        | Contents                                                                           |
| --------------------------------------------- | ---------------------------------------------------------------------------------- |
| [`cybersecurity/`](./cybersecurity/README.md) | eJPTv2 / PNPT prep — networking, web exploitation, CTF writeups, interactive tools |
| `assets/`                                     | Shared images and diagrams referenced by notes                                     |

## Conventions

- Filenames: lowercase, hyphen-separated — `sql-injection-basics.md`, not `SQL Injection Notes.md`
- Sequential notes get a number prefix — `01-nmap-basics.md`, `02-smb-enum.md`
- Every folder has its own `README.md` acting as a mini table of contents
- `.html` files are self-contained (no external build step) so they render directly on GitHub Pages

## Viewing HTML notes/tools

`.md` files render automatically on GitHub. To view the `.html` files as actual pages (not raw code), enable **GitHub Pages**:

1. Repo → **Settings** → **Pages**
2. Source: `Deploy from a branch` → `main` → `/ (root)`
3. Your HTML tools will be live at `https://<username>.github.io/<repo>/path/to/file.html`

## Setup

```bash
git clone <this-repo-url>
cd notes-repo
```
