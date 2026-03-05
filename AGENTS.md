## Cursor Cloud specific instructions

This is a Jekyll static site (Minimal Mistakes theme v4.24.0) serving as a personal portfolio. No backend services, databases, or Docker are needed.

### Services

| Service | Command | Notes |
|---|---|---|
| Jekyll dev server | `bundle exec jekyll serve --host 0.0.0.0 --port 4000` | Main service; serves site at http://localhost:4000 |
| JS build (optional) | `npm run build:js` | Only needed when editing JS source files in `assets/js/` |

### Caveats

- Gems are installed to `vendor/bundle` (via `bundle config set --local path 'vendor/bundle'`) to avoid system permission issues.
- `_config.yml` changes are **not** picked up by Jekyll's live reload; you must restart the server.
- The `docs/` directory is a separate Minimal Mistakes documentation sub-site excluded from the main build — ignore it for this site's development.
- SCSS compilation produces deprecation warnings from the vendored Susy library (`_sass/minimal-mistakes/vendor/susy/`); these are harmless.
- There is no test suite or linter configured in this repository.
