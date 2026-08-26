# AtlasOmnia Community Plugins

A curated list of community-made plugins for the [Hermes desktop client](https://hermes-agent.nousresearch.com/docs), maintained by [AtlasOmnia](https://github.com/AtlasOmnia).

Each entry links to a plugin maintained in its own repository. Plugins are **listed, not audited** — review any plugin's code before running it on your machine.

---

## What are desktop plugins?

Hermes desktop plugins are single plain-JavaScript files (ESM) that the desktop app loads at runtime. No build step, no repo changes — drop a folder into `~/.hermes/desktop-plugins/` and the app picks it up within seconds, hot-reloading on every save.

Plugins can add:

- **Status bar chips** (`statusBar.left` / `statusBar.right`)
- **Layout panes** (docked left/right/bottom, or full pages)
- **Command palette commands** (⌘K) and rebindable keybinds
- **Full pages** with sidebar navigation entries
- **Themes** and UI contributions

Full SDK reference: the `website/docs/developer-guide/desktop-plugin-sdk.md` file in the Hermes Agent repository, plus the `hermes-desktop-plugins` skill if you run Hermes yourself.

## Installing a plugin

1. Create a folder named after the plugin under `~/.hermes/desktop-plugins/` (e.g. `~/.hermes/desktop-plugins/my-plugin/`).
2. Copy that plugin's `plugin.js` into the folder.
3. The plugin loads automatically. If it doesn't appear, open the command palette (⌘K) → **Reload desktop plugins**.
4. Manage (enable/disable) installed plugins in **Settings → Plugins**.

> Some plugins ship an optional Python backend (`plugin_api.py`). Those go under `~/.hermes/plugins/<id>/dashboard/` instead — check the linked repo's README for its specific install steps.

---

## The list

Every entry below was verified against a public repository containing a native Hermes Desktop `plugin.js` that imports `@hermes/plugin-sdk`. Listings are still **not security audits**. Review source and each project's install instructions before use.

### Appearance

| Plugin | Description | Author |
|--------|-------------|--------|
| [Codex Skin](https://github.com/FPSUnleashed/hermes-codex-skin) | Codex-inspired light and dark chat styling while retaining Hermes' native behavior. | [@FPSUnleashed](https://github.com/FPSUnleashed) |
| [Appearance Hub](https://github.com/Heybinshao/hermes-appearance-hub) | Status-bar appearance controls for themes, typography, texture, density, scale, and window effects. | [@Heybinshao](https://github.com/Heybinshao) |
| [Theme Lab](https://github.com/0-CYBERDYNE-SYSTEMS-0/theme-lab) | Builds and fine-tunes Hermes Desktop color themes from an image and color controls. | [@0-CYBERDYNE-SYSTEMS-0](https://github.com/0-CYBERDYNE-SYSTEMS-0) |

### Bots & Remote Control

| Plugin | Description | Author |
|--------|-------------|--------|
| [Hermes QR Remote](https://github.com/tuancookiez-hub/hermes-qr-remote-plugin) | Phone control surface for Desktop sessions, tool activity, and stop/send actions via a local Tailscale sidecar. | [@tuancookiez-hub](https://github.com/tuancookiez-hub) |

### Usage & Session Insight

| Plugin | Description | Author |
|--------|-------------|--------|
| [Resetwatch](https://github.com/Adolanium/hermes-resetwatch) | Dashboard for remaining model-plan allowance and reset times using existing local sign-ins. | [@Adolanium](https://github.com/Adolanium) |
| [Ledgerline](https://github.com/Adolanium/hermes-ledgerline) | Live and historical cost, token, budget, and session analysis for local or remote gateways. | [@Adolanium](https://github.com/Adolanium) |
| [Session Analyzer](https://github.com/tommulkins/hermes-plugin-session-analyzer) | Sidebar and command-palette analysis of session health, tool failures, context use, and cost. | [@tommulkins](https://github.com/tommulkins) |

### Tasks & Notes

| Plugin | Description | Author |
|--------|-------------|--------|
| [Hermes Todo](https://github.com/DanBennettUK/hermes-todo) | Profile-scoped task board shared across Hermes Desktop, CLI, REST API, and agents. | [@DanBennettUK](https://github.com/DanBennettUK) |
| [Hermes Tasks](https://github.com/itsbeaudean/hermes-tasks) | Local task workflow with areas, task state, and a small Desktop plugin plus optional backend. | [@itsbeaudean](https://github.com/itsbeaudean) |
| [Hermes Sticky Notes](https://github.com/VGFreakXBL/hermes-sticky-notes) | Profile-scoped sticky notes inside Hermes Desktop, including movable and stackable notes. | [@VGFreakXBL](https://github.com/VGFreakXBL) |

Row format:
```
| [Plugin Name](repo-url) | One-line description of what it adds to the desktop app | [@author](author-url) |
```

---

## Submitting your plugin

Want your plugin listed? Open a pull request — it's a 30-second review.

1. Fork this repo.
2. Add one row to the table under the right category (create a category heading if none fit):

   ```
   | [Your Plugin](https://github.com/you/your-plugin) | What it adds to the Hermes desktop app | [@yourhandle](https://github.com/yourhandle) |
   ```

3. Open the PR against `main`.

**Requirements:**

- Your repo must be a real, working Hermes desktop plugin (single ESM `plugin.js`, loads via `@hermes/plugin-sdk`).
- The description must state what it actually does — no marketing shells or branding-only repos.
- Your repo must be public and have a README explaining what it does and how to install it.
- No obfuscated code, credential harvesting, or undisclosed network calls. Listings get reviewed; violations get delisted.

We may reorder or recategorize rows for consistency, and we'll reach out before removing anything.

---

## License

This list: [MIT](LICENSE). Each linked plugin keeps its own license — check the linked repo.
