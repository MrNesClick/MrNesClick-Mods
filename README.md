# MrNesClick's Minecraft mods

Bug reports, suggestions and documentation for the Minecraft mods by MrNesClick. The source code is not public: this
repository holds the issues and the documentation site.

**Documentation: https://mrnesclick.github.io/MrNesClick-Mods/**

| Mod | What it does | Download |
|---|---|---|
| **Flux Networks Extended** | Addon for Flux Networks: Herculean, Gargantuan and Ultimate Flux Plugs and Points, upgrade kits, Mekanism integration | [CurseForge](https://www.curseforge.com/minecraft/mc-mods/flux-networks-extended) |
| **MCNesclick** | Small, vanilla-friendly and fully configurable survival additions | [CurseForge](https://www.curseforge.com/minecraft/mc-mods/mcnesclick) |
| **Mekanistic Geothermal** (alpha) | Addon for Mekanism: a self-drilling geothermal wellhead that turns water into steam for Mekanism turbines | [CurseForge](https://www.curseforge.com/minecraft/mc-mods/mekanistic-geothermal) |

## Documentation

The site is built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) from `docs/` and `mkdocs.yml`, and
published on GitHub Pages by the Pages workflow on every push to `main`. Locally:
`pip install -r requirements.txt`, then `mkdocs serve` (preview on http://127.0.0.1:8000) or `mkdocs build --strict`.

English pages are `page.md`, their French translations `page.fr.md` next to them (served under `/fr/`): a change to one
goes to the other.

When a mod is released, refresh its configuration reference from the mod repository (next to this one), then review
the diff and update the pages if options changed:

```sh
python3 tools/sync_config.py mekanistic-geothermal   # or flux-networks-extended, mcnesclick, all
```

## Report a bug or suggest something

1. Search the [existing issues](../../issues?q=is%3Aissue) first: your problem may already be known.
2. [Open a new issue](../../issues/new/choose) and pick the form for your mod.
3. Give the versions asked by the form and, for a crash or an error, the log: upload `logs/latest.log` or the crash
   report from `crash-reports/` to [mclo.gs](https://mclo.gs) and paste the link.

Reports in English or French are welcome.

---

**FR** : signalements de bugs et suggestions pour les mods Minecraft de MrNesClick. Cherche d'abord dans les issues
existantes, puis ouvre une issue avec le formulaire de ton mod. Les rapports en français sont les bienvenus.
