# Safety

The **pressure** of a well is the fill ratio of its steam tank (64,000 mB for the Basic tier). It rises when the steam
has nowhere to go. Three systems keep it under control, and a fourth stops everything.

| Pressure | What happens |
|---|---|
| 80 % | The **safety valve** opens and vents steam (if there is air right above the wellhead). |
| 90 % | The **automatic shutdown** stops production. |
| under 50 % | Production restarts. |
| 100 % | Full: if nothing relieves the well, an **eruption** may happen (disabled by default). |

## Safety valve

- It is the **top face** of the wellhead, and it needs **air right above it**. A block there obstructs it: the
  interface and the logic adapter say so.
- It is **mechanical**: it works without energy (`valveNeedsEnergy` changes that).
- It vents at most half of the max steam rate, and only down to 80 %: it slows a pressure rise, it does not hide a
  blocked output.

## Control system

The control system uses a little energy (20 FE/t for the Basic tier, ×4 with 8 Speed upgrades, ÷10 with 8 Energy
upgrades). Without energy it cannot act, and the main screen says so.

- **Automatic shutdown**: stops production at 90 % pressure and restarts it under 50 %.
- **Low-water lock**: when the water tank runs dry, production waits until it is back over 10 %, instead of
  sputtering.

Without energy, both are released and production goes on (boiling itself is passive).

## Emergency stop

The red **Emergency stop** button of the interface (or a logic adapter in input mode) stops drilling and production,
even without energy. The well stays stopped until someone **resets** it with the same button. The stop is saved with
the wellhead, but not kept in its item when it is dismantled.

## Comparator

A comparator next to the wellhead reads the pressure: 0 when empty, 8 at 50 %, 15 when full.

## Eruptions (disabled by default)

A server can enable them (`[eruption] mode`): `STEAM_JET` (burn damage around the top of the well, half of the steam
released) or `EXPLOSION`. An eruption needs a well at **full pressure, heated and fed with water**, that nothing relieves:
valve obstructed, disabled or unpowered, and automatic shutdown disabled or unpowered. After 30 seconds at full
pressure, each second has a 2 % chance (about 50 seconds on average). With the explosion, the wellhead is blown off as
an item that keeps its contents, and the casings stay in place.
