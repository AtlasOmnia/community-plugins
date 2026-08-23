# Community Plugin Listing — PR Checklist

Thank you for submitting your plugin! To keep review fast (usually same-day):

- [ ] Added one row to the table in `README.md` under the right category
  - Format: `| [Plugin Name](repo-url) | One-line description | [@handle](author-url) |`
- [ ] The linked repo is **public**
- [ ] The repo contains a real Hermes desktop plugin (single ESM `plugin.js` using `@hermes/plugin-sdk`)
- [ ] The repo has a README covering what it does and how to install it
- [ ] The description states what the plugin actually does
- [ ] No obfuscated code, credential access, or undisclosed network calls

A maintainer will verify the repo exists and loads as a desktop plugin, then merge.
