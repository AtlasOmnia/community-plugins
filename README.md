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

### Panes & Dashboards

| Plugin | Description | Author |
|--------|-------------|--------|

*No entries yet — be the first!*

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
