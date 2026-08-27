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
| [Hermes Theme Picker](https://github.com/jdtimothy/hermes-theme-picker) | Offline full-page theme picker with embedded palettes, local persistence, and optional gateway-wide sync. | [@jdtimothy](https://github.com/jdtimothy) |
| [Classic Gold Pack](https://github.com/Elevatormusic/hermes-classic-gold-pack) | Update-safe gold theme, caduceus background, telemetry tape, and settings page with a companion telemetry backend. | [@Elevatormusic](https://github.com/Elevatormusic) |
| [OpenAI Shadcn Theme](https://github.com/agentik-os/hermes-openai-shadcn) | Neutral light and dark theme with floating-panel layout polish for supported Desktop SDK builds. | [@agentik-os](https://github.com/agentik-os) |
| [Profile Identity](https://github.com/douglascorrea/hermes-profile-identity) | Per-profile titlebar chip, rail icon, chat backdrop, color override, and settings pane. | [@douglascorrea](https://github.com/douglascorrea) |
| [Profile Avatars](https://github.com/moreirawebmaster/Hermes-Profile-Avatars) | Replaces profile initials with real avatars in the session sidebar, Kanban assignees, and identity marks. | [@moreirawebmaster](https://github.com/moreirawebmaster) |
| [Persian Typography](https://github.com/omid3098/hermes-persian-typography) | Improves Persian chat typography, script direction, and streaming text while preserving code-block LTR behavior. | [@omid3098](https://github.com/omid3098) |
| [Kal'tsit Rhodes Theme](https://github.com/qazlp66/hermes-kaltsit-theme) | Dynamic glass theme, animated background, and interactive desktop pet with accessibility preferences. | [@qazlp66](https://github.com/qazlp66) |
| [Skin Studio](https://github.com/weiweiplus0527/hermes-skin-studio) | Theme editor with image palette extraction, video backgrounds, presets, and live Desktop skin updates. | [@weiweiplus0527](https://github.com/weiweiplus0527) |

### Collaboration & Workflow

| Plugin | Description | Author |
|--------|-------------|--------|
| [Buzz-Hive](https://github.com/0-CYBERDYNE-SYSTEMS-0/hermes-hive) | Native multi-profile crew room that routes work by mention through dedicated Hermes sessions. | [@0-CYBERDYNE-SYSTEMS-0](https://github.com/0-CYBERDYNE-SYSTEMS-0) |
| [Hermes OpenSpec](https://github.com/FelineStateMachine/hermes-openspec) | Spec-driven development tools plus a Desktop tab for proposals, specs, and branch diffs. | [@FelineStateMachine](https://github.com/FelineStateMachine) |
| [Agent Fleet](https://github.com/chankov/agent-fleet) | Multi-agent coding-orchestration system with a live Hermes Desktop fleet panel. | [@chankov](https://github.com/chankov) |
| [Fleet Control](https://github.com/kabuto-png/fleet-control) | Read-only fleet pane for cmux, Claude, Codex, and Hermes workers with workspace and heartbeat state. | [@kabuto-png](https://github.com/kabuto-png) |
| [GitHub Studio](https://github.com/Koktongkt/hermes-github-studio) | Native GitHub profile, repository, activity, commit, and pull-request browser using local `gh` auth. | [@Koktongkt](https://github.com/Koktongkt) |
| [Design Plugin](https://github.com/labsiqbal/hermes-design-plugin) | Editable design studio for artboards, brand guides, moodboards, layers, model-assisted candidates, and exports. | [@labsiqbal](https://github.com/labsiqbal) |

### Bots & Remote Control

| Plugin | Description | Author |
|--------|-------------|--------|
| [Hermes QR Remote](https://github.com/tuancookiez-hub/hermes-qr-remote-plugin) | Phone control surface for Desktop sessions, tool activity, and stop/send actions via a local Tailscale sidecar. | [@tuancookiez-hub](https://github.com/tuancookiez-hub) |
| [Hermes Relay](https://github.com/Codename-11/hermes-relay) | Native relay management for pairing, activity, media, and remote access inside Desktop. | [@Codename-11](https://github.com/Codename-11) |
| [Hermes Computer Viewer](https://github.com/thomasbek3/hermes-computer-viewer) | Docked live remote-desktop viewer for cloud or LAN Mac, Windows, and Linux machines. | [@thomasbek3](https://github.com/thomasbek3) |
| [Hermes Agent Dock](https://github.com/BkashJEE/hermes-agent-dock) | Floating or docked native card for direct chat with configured profiles and concurrent jobs. | [@BkashJEE](https://github.com/BkashJEE) |
| [Hermes Gateway Switcher](https://github.com/djedi/hermes-gateway-switcher) | Switches between named local, SSH, and remote OAuth gateways without closing Desktop. | [@djedi](https://github.com/djedi) |

### Usage & Session Insight

| Plugin | Description | Author |
|--------|-------------|--------|
| [Resetwatch](https://github.com/Adolanium/hermes-resetwatch) | Dashboard for remaining model-plan allowance and reset times using existing local sign-ins. | [@Adolanium](https://github.com/Adolanium) |
| [Ledgerline](https://github.com/Adolanium/hermes-ledgerline) | Live and historical cost, token, budget, and session analysis for local or remote gateways. | [@Adolanium](https://github.com/Adolanium) |
| [Session Analyzer](https://github.com/tommulkins/hermes-plugin-session-analyzer) | Sidebar and command-palette analysis of session health, tool failures, context use, and cost. | [@tommulkins](https://github.com/tommulkins) |
| [Hermes Quota Plugin](https://github.com/rarf/hermes-quota-plugin) | Provider quota and reset status-bar widget with a detailed quota view. | [@rarf](https://github.com/rarf) |
| [Hermes Status Panel](https://github.com/lzpgood123/hermes-status-panel) | Full status page for gateway, model, session, working-directory, and live gateway-event state. | [@lzpgood123](https://github.com/lzpgood123) |
| [Hermes Token Cost](https://github.com/muntasirrmahdi/hermes-token-cost) | Status-bar token counter and historical actual-versus-list-price cost panel. | [@muntasirrmahdi](https://github.com/muntasirrmahdi) |
| [Hermes API Speed Monitor](https://github.com/kouyichi/hermes-api-speed-monitor) | Status-bar time-to-first-token and output-throughput metrics for supported providers. | [@kouyichi](https://github.com/kouyichi) |
| [Hermes Memory UI](https://github.com/xraysight/hermes-memory-ui) | Read-only native memory browser for built-in and supported external memory stores. | [@xraysight](https://github.com/xraysight) |
| [Account & Resources Footer](https://github.com/agentik-os/hermes-account-resource-footer) | Gateway-scoped quota, context, CPU, RAM, disk, account-switching, and reconnect status control. | [@agentik-os](https://github.com/agentik-os) |
| [Hermes Server Stats](https://github.com/lzpgood123/hermes-server-stats) | Desktop page for read-only server health, token usage, tool/skill counts, and trends. | [@lzpgood123](https://github.com/lzpgood123) |
| [Quota HUD](https://github.com/saralilyb/quota-hud) | Local status-bar and detail page for Codex and Claude subscription quota windows and reset times. | [@saralilyb](https://github.com/saralilyb) |
| [AI Status](https://github.com/hifumi12390/hermes-ai-status-plugin) | Windows/NVIDIA sidebar page for GPU use, VRAM, temperature, RAM, and short-term trends. | [@hifumi12390](https://github.com/hifumi12390) |
| [Workspace Context](https://github.com/meviusisback/hermes-workspace-context) | Inline composer strip for active-session context use, maximum tokens, percentage, and occupancy. | [@meviusisback](https://github.com/meviusisback) |
| [Abyss](https://github.com/leviathofnoesia/hermes-abyss-plugin) | Local observability suite for traces, activity, calendars, signals, incidents, and agent graphs. | [@leviathofnoesia](https://github.com/leviathofnoesia) |

### Models & Infrastructure

| Plugin | Description | Author |
|--------|-------------|--------|
| [Turbofit](https://github.com/SouthpawIN/turbofit) | Adaptive local-inference runtime and Desktop configuration surface for hardware-fit model selection. | [@SouthpawIN](https://github.com/SouthpawIN) |
| [Ollama Usage Monitor](https://github.com/Kosello/hermes-ollama-usage-monitor) | Work-in-progress Desktop pane and chip for Ollama Cloud quota, request, history, and threshold monitoring. | [@Kosello](https://github.com/Kosello) |
| [Qdrant File Discovery](https://github.com/brunocasado/hermes-qdrant-plugin) | Project file-discovery layer with a Desktop status pill; requires Qdrant and an embedding endpoint. | [@brunocasado](https://github.com/brunocasado) |

### Projects & Development

| Plugin | Description | Author |
|--------|-------------|--------|
| [GitHermes](https://github.com/claudioorjunior/githermes) | Dockable GitHub pull-request and issue pane with reviews, checks, files, threads, and in-pane merge. | [@claudioorjunior](https://github.com/claudioorjunior) |
| [Hermes Projects](https://github.com/az1fr3/Hermes-projects-) | Project-scoped workspaces with persistent instructions, chats, and generated context files. | [@az1fr3](https://github.com/az1fr3) |

### Utility & Customization

| Plugin | Description | Author |
|--------|-------------|--------|
| [Desktop Achievements](https://github.com/asimons81/hermes-desktop-achievements) | Achievements page with a sidebar item, score chip, unlock notifications, sounds, haptics, and commands. | [@asimons81](https://github.com/asimons81) |
| [Chat Width](https://github.com/Gohans1/chat-width) | Status-bar popover for preset or custom conversation and composer widths. | [@Gohans1](https://github.com/Gohans1) |

### Media & Visualizations

| Plugin | Description | Author |
|--------|-------------|--------|
| [YouTube Player](https://github.com/chillerno1/hermes-yt-plugin) | Floating or docked keyless YouTube player using an isolated Electron webview. | [@chillerno1](https://github.com/chillerno1) |
| [Office 3D](https://github.com/oslook/hermes-desktop-plugin-office-3d) | Isometric office view showing profile busy, idle, and offline state with aggregate session, token, and cost stats. | [@oslook](https://github.com/oslook) |
| [Desktop Dashboard](https://github.com/hithithithub/hermes-desktop-dashboard) | Native Desktop sidebar shell that embeds a locally running Hermes web Dashboard. | [@hithithithub](https://github.com/hithithithub) |
| [Desktop Web Browser](https://github.com/AWhileLater/hermes-desktop-web-browser) | Embedded multi-tab browser with bookmarks, annotations, and annotation-to-agent workflow. | [@AWhileLater](https://github.com/AWhileLater) |

### Security & External Integrations

| Plugin | Description | Author |
|--------|-------------|--------|
| [Chthonios Lock](https://github.com/iacker/hermes-chthonios) | Desktop controls for sealing and unlocking a Hermes profile's credentials at rest. | [@iacker](https://github.com/iacker) |
| [VRChat Monitor](https://github.com/ggg123124/vrchat-assistant) | Desktop pane for a local VRChat monitoring and automation service; requires a separately configured VRChat account. | [@ggg123124](https://github.com/ggg123124) |

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
