# Configuration

Everything in MCNesclick is set in a single file, `config/mcnesclick.toml`, in the game or server folder. It is the same
file on every loader and every Minecraft version.

- The file is created on first launch, with a comment above every option. A missing key is added back with its default
  value.
- An invalid value is reported in the log and replaced by the default until you fix it.
- **When changes apply**: recipes, effects, apple drops and campfire protection on `/reload` (or when the world or
  server restarts). Hunger and saturation need a restart of the game or server.
- **On a server**, the server's file is the one that counts. Players should use the same hunger and saturation values,
  so that the item tooltips match.

## Effects

The emerald and diamond apples take a list of effects, each written `"effect_id seconds level"`:

```toml
effects = ["minecraft:haste 300 2", "minecraft:night_vision 300 1"]
```

- `level` 1 is level I, 2 is level II, and so on (up to 256).
- `seconds` goes from 1 to 86400 (one day).
- Any effect id works, modded ones too. `[]` gives no effect.
- An invalid entry or an unknown effect is reported once in the log, then ignored.

## Options

--8<-- "mcnesclick/config.md"

## For modpack makers

Every recipe is a standard data-pack recipe, so you can replace it with a data pack, **KubeJS** or **CraftTweaker**
without any extra mod:

| Recipe id | What |
|---|---|
| `mcnesclick:emerald_apple` | emerald apple (crafting table) |
| `mcnesclick:diamond_apple` | diamond apple (crafting table) |
| `mcnesclick:cooked_apple_from_smelting`, `_from_smoking`, `_from_campfire_cooking`, `_from_blasting` | cooked apple |

A data pack overrides one by putting a file at `data/mcnesclick/recipe/<id>.json` (`recipes/` before Minecraft 1.21).
Hunger, saturation and effects come from `config/mcnesclick.toml`: ship your own copy with the pack.
