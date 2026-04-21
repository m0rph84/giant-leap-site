# AGENTS.md

## Project context

- This repository is a static site built with Hugo.
- The active theme is `blowfish`, included as a git submodule under `themes/blowfish`.
- The site represents the `Giant Leap` Star Citizen org.
- The current visual direction is black/gold, custom branded, and should stay consistent with the existing org identity.

## Working rules

- Prefer editing existing Hugo configuration and overrides instead of changing theme internals directly.
- Keep changes inside project-owned paths such as `config/`, `content/`, `assets/`, and `layouts/`.
- Avoid reintroducing Blowfish demo content, demo menus, or unused sample sections.
- Use the current multilingual setup only for `it` and `en`.
- Do not reintroduce other languages unless explicitly requested.

## Hugo configuration notes

- Main Hugo configuration lives in `config/_default/hugo.toml`.
- Only the mounted content paths in `config/_default/hugo.toml` are part of the intended site build.
- Taxonomy and term pages are disabled.
- The homepage uses `layout = "custom"`.
- The main article section is `diario-di-bordo`.

## Frontend and content notes

- The homepage is implemented in `layouts/partials/home/custom.html`.
- Recent articles are customized in `layouts/partials/recent-articles/main.html`.
- Brand styling is defined in `assets/css/custom.css` and the `giantleap` color scheme.
- Keep the language switcher working for ITA/ENG and preserve the selected language in homepage body links.
- If removing or renaming a section, update all related menus, homepage links, content mounts, and translations together.

## Validation

- Preferred local build command:
  - `C:\Users\al.TEAM\AppData\Local\Microsoft\WinGet\Links\hugo.exe --minify --cleanDestinationDir`
- Preferred local dev server command:
  - `C:\Users\al.TEAM\AppData\Local\Microsoft\WinGet\Links\hugo.exe server --disableFastRender`
- After structural content or navigation changes, verify:
  - build completes successfully
  - no stale homepage links remain
  - IT and EN both resolve correctly

## Additional reference

- Also use the file `claude.md` to gather information when it exists and is relevant.
- If `claude.md` is missing, continue with the repository sources above without blocking.
- For site design decisions, refer to the projects we will share through Figma or Canvas.
