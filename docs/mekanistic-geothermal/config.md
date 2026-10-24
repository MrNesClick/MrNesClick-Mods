# Configuration

Every mechanic, rate and threshold of Mekanistic Geothermal is configurable. The defaults are mild; a modpack can make
the mod harder or easier, or turn any mechanic off.

## Files

| File | Side | What it holds |
|---|---|---|
| `config/mekanismgeothermal-server.toml` | Server (synced to the players) | Everything that changes the game: tiers, drilling, heat, production, safety, eruptions, interference, exhaustion, upgrades, adapter |
| `config/mekanismgeothermal-client.toml` | Each player | Display of the guide |

The server file is created with its defaults the first time the game or the server starts. To use different settings
in one world only, copy the file to `<world>/serverconfig/mekanismgeothermal-server.toml` and edit that copy.

Changes to the server file are **reloaded while the game runs**: no restart needed.

!!! tip "Percentages"
    Ratios are written from 0 to 1: `0.8` is 80 %. The pressure is the fill ratio of the wellhead's steam tank.

## Server options

--8<-- "mekanistic-geothermal/server.md"

## Client options

--8<-- "mekanistic-geothermal/client.md"
