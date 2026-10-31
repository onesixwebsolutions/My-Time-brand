# My-Time-brand (private)

Proprietary One Six brand assets for DayGrid. **Keep this repository private.**

Consumed by the main repo (`onesixwebsolutions/My-Time`) as the git submodule `branding/`.
`src/DayGrid.Web/scripts/sync-brand.mjs` copies these files into the Angular app before every
build, start and test run. Without access to this repo the app builds with neutral placeholder
logos instead.

| Path | Copied to | Purpose |
|---|---|---|
| `assets/brand/*` | `src/DayGrid.Web/src/assets/brand/` | logos, app icons (see `assets/brand/README.md` for geometry and colours) |
| `assets/brand/logo-glyph.svg` | same | white mark drawn on the gradient tile in the sidebar and auth pages |
| `favicon.ico` | `src/DayGrid.Web/src/favicon.ico` | browser tab icon |
| `design/DayGrid-Mockup.html` | not copied | original interactive design mockup |

Files the app references by name (keep these names when updating the artwork):
`favicon.ico`, `assets/brand/logo-tile.svg`, `assets/brand/logo-glyph.svg`,
`assets/brand/apple-touch-icon.png`.

After changing assets here: commit and push this repo, then in the main repo run
`git submodule update --remote branding` and commit the new submodule pointer.
