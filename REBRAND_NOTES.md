# Aquila Agent — Rebrand Notes

This checkout is a rebranded fork of the MIT-licensed **Hermes Agent** desktop app
(originally by Nous Research). Product identity is now **Aquila Agent**, developed
by **Savez**, with a satin gold (#f5c518) visual identity.

## What was rebranded

- **Product identity** — `apps/desktop/package.json`: name `aquila`, productName
  `Aquila Agent`, author `Savez`, appId `com.savez.aquila`, executable `Aquila`,
  installer/DMG/NSIS names, macOS bundle names, Linux maintainer.
- **All user-facing strings** in `apps/desktop`, `apps/shared`, and
  `apps/bootstrap-installer` — window titles, i18n catalogs (en/ja/zh/zh-hant),
  overlays, settings, onboarding (≈1,580 replacements).
- **Deep-link protocol** — `hermes://` → `aquila://` (scheme registered as `aquila`).
- **Default theme** — the built-in default skin is now **Aquila Gold**
  (`apps/desktop/src/themes/presets.ts` + `src/styles.css` seed variables):
  lacquered gold `#F5C518` primary, deep gold `#C99E06` accents, warm ivory light
  mode, lacquered near-black gold dark mode.
- **Icons/logos** — `assets/icon.png/.ico/.icns` and `public/apple-touch-icon.png`
  regenerated as a satin-gold "A" mark (script: procedural, no external assets).
  Legacy Hermes/Nous mascot images removed from `public/`.
- **Agent identity** — `hermes_cli/default_soul.py` default persona now introduces
  itself as "Aquila Agent … created by Savez".
- Internal shared package renamed `@hermes/shared` → `@aquila/shared`.

## What was deliberately kept (functional, not branding)

- **MIT LICENSE** file and upstream copyright — required by the license.
- **`HERMES_*` environment variables** and `HERMES_HOME` — they cross the
  Electron ↔ Python backend boundary; renaming breaks the backend contract.
- **Backend paths** (`~/.hermes`, `%LOCALAPPDATA%\hermes\hermes-agent`), the
  `hermes` CLI command, Python module names — backend internals.
- **Bootstrap/update URLs** pointing at `github.com/NousResearch/hermes-agent` —
  the desktop app installs/updates its backend from that repo. Point these at a
  Savez fork if you publish one (`apps/desktop/electron/bootstrap-runner.ts`,
  `update-remote.ts`).
- **"Nous Portal"** provider mentions — that is a live third-party service name
  (like "OpenAI"), not self-branding.
- `@nous-research/ui` — external npm dependency.
- `_LEGACY_TEMPLATE_SOULS` strings in `default_soul.py` — byte-exact fingerprints
  used to detect old files; must not change.

## Placeholders to fill in

- Linux package maintainer email: `support@savez.example` in
  `apps/desktop/package.json` → replace with a real address before publishing.
