# Campfire protection

A lit campfire stops hostile mobs from spawning naturally around it. Light one in your camp or your base, and the
night stays quiet around it.

![Same night, two identical camps: monsters everywhere on the left, none around the lit campfire on the right](../assets/mcnesclick/campfire-comparison.png)

## The protected zone

By default, **16 blocks around the campfire and 8 blocks above and below it**. The zone is flat on purpose: a campfire
in your base does not protect the whole cave system underneath.

![The protected zone around a campfire, dark corners included](../assets/mcnesclick/campfire-zone.png)

## What it blocks, and what it does not

- It blocks the **natural spawning of hostile mobs**, even in dark corners of the zone.
- Mobs that **walk in** from outside are not pushed away.
- **Monster spawners and trial spawners (Minecraft 1.21+) keep working** by default, so mob farms are not broken. An option blocks them
  too.
- Passive mobs are never affected.
- Soul campfires protect like regular ones, and unlit campfires do not protect. Both can be changed.
- Some mobs can be left out of the protection, for example creepers or slimes.

The protection runs on the server: on a multiplayer server, the server's config decides.

**Configurable** in [`[campfire_protection]`](config.md#campfire_protection): on or off, radius, height, lit campfires
only, soul campfires, spawners and excluded mobs.
