# amlmarketplaces/llamaindex

Claude Code marketplace federating all `@amlplugins/llamaindex-*` plugins.

## Install

Add to your project's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "aml-llamaindex": {
      "source": { "source": "github", "repo": "amlmarketplaces/llamaindex" }
    }
  },
  "enabledPlugins": {
      "llamaindex-anthropic@aml-llamaindex": true,
      "llamaindex-google@aml-llamaindex": true,
      "llamaindex-meta@aml-llamaindex": true,
      "llamaindex-openai@aml-llamaindex": true
    }
}
```

Then launch Claude Code in the project. The marketplace is fetched from `amlmarketplaces/llamaindex`, cached under `~/.claude/plugins/cache/aml-llamaindex/`, and each enabled plugin is loaded from its `amlplugins` source repo.

## Plugins (4 total)

- `llamaindex-anthropic` — [@amlplugins/llamaindex-anthropic](https://github.com/amlplugins/llamaindex-anthropic)
- `llamaindex-google` — [@amlplugins/llamaindex-google](https://github.com/amlplugins/llamaindex-google)
- `llamaindex-meta` — [@amlplugins/llamaindex-meta](https://github.com/amlplugins/llamaindex-meta)
- `llamaindex-openai` — [@amlplugins/llamaindex-openai](https://github.com/amlplugins/llamaindex-openai)

## Related

- npm packages: `@amlplugins/llamaindex-*` published to GitHub Packages (`https://npm.pkg.github.com`).
- Aggregating parent: [`amlmarketplaces/aml`](https://github.com/amlmarketplaces/aml) — federates every `@amlplugins/*` plugin under a single marketplace.
- AML topology: see `.claude/rules/definitions/ageni.md` § "GitHub Topology" — this repository is a Tier-4 HUB-INSTANCE under the `amlmarketplaces/` Tier-3 HUB-ORGANIZATION.

> Built by `.claude/skills/aml/metateam/marketplace/test/cross-org-amlmarketplaces-batch.mjs`.
