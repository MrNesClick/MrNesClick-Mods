# The wellhead

The **Basic Geothermal Wellhead** is a Mekanism machine: it is built on Mekanism's own machine framework, so its
interface, tabs, side configuration, auto-eject, Configurator modes, upgrades, redstone control, security and Jade
display work as on Mekanism's machines.

![The wellhead's main screen](../assets/mekanistic-geothermal/media-03-interface.png)

## The interface

- **Gauges**: water (left) and steam (right), and the energy bar.
- **Status screen**: production, steam rate and temperature, exhaustion, pressure (and the valve when it vents or
  cannot), drill state and progress, depth. Hover it for the details: tier max rate, control system, interference,
  water demand.
- **Casing slots**, **target depth** (arrows, Shift: ±10, mouse wheel), **Start drilling** and **Emergency stop**
  buttons, and the **debris** slots.
- **Tabs**: Mekanism's side configuration, transporter, upgrades, security and redstone control, plus the **guide**,
  heat and energy tabs.

![Mekanism's side configuration](../assets/mekanistic-geothermal/media-05-side-config.png)

## Drilling

- The drill goes down one block at a time under the wellhead (40 ticks and 4,000 FE per block by default) and puts a
  Steel Well Casing in each hole. Every block it digs goes to the debris slots; take them out by hand or through an
  item output face.
- It stops at the **target depth**, or when it meets **lava**: the lava then heats the well (the drilling step of the
  guide counts as done).
- It waits, and says why, when it runs out of energy or casings, when the debris slots are full, or on a block it may
  not break (unbreakable, blacklisted, or protected by a claim: the drill acts with its owner's permissions).
- **Caves**: each air block crossed takes a casing and the energy of a drilled block, so the column stays continuous.
- **Repairs**: if a casing of the column is removed, the wellhead puts it back by itself (no button needed). While a
  casing is missing, the well produces no steam.

## Heat and steam

The temperature of a well depends on the **absolute Y of its bottom** and on the dimension:

| Dimension | Temperature | Production multiplier |
|---|---|---|
| Overworld | 100 °C at Y 0 and above, rising linearly to 250 °C at Y −60 | ×1 |
| Nether | 180 °C at any depth | ×0.6 |
| End | no steam | — |

Water boils above 100 °C: the **temperature factor** goes from 0 at 100 °C to 1 at 250 °C. Lava source blocks within
2 blocks of the bottom add 2 °C each, up to 50 °C.

**Steam rate** = max rate (400 mB/t for the Basic tier, ×2 with 8 Speed upgrades) × temperature factor
× (1 − interference) × (1 − exhaustion), limited by the water available. The wellhead uses 1/0.95 mB of water per mB of
steam (5 % blowdown). Boiling is passive: it needs no energy (energy only powers the drill and the control system).

| Source | Steam | Best energy through a Mekanism turbine |
|---|---|---|
| Basic well at Y −60, alone and fresh | 400 mB/t | 1,600 FE/t |
| Basic well at Y −30 | 200 mB/t | 800 FE/t |
| Basic well in the Nether | 128 mB/t | 512 FE/t |
| Smallest Mekanism fission reactor (0.1 mB/t burn) | 2,000 mB/t | 8,000 FE/t |

## Interference

Wells too close to each other share the heat. Each neighbour that **produced in the last 3 seconds** within
**24 blocks** costs 25 % × (1 − distance / 24): two wells side by side lose up to 25 % each, wells 24 blocks apart lose
nothing. The total is capped at 75 % and recalculated every 5 seconds. Hover the status screen to see it.

## Exhaustion

A column slowly **exhausts** under heavy load and **recovers at rest**. It is shown on the main screen, coloured like the
damage of Mekanism's fission reactor (green, yellow, orange, dark red by quarters of the maximum).

- At full load, it grows by 1 % of the rate per Minecraft day, up to **15 %** (about 15 days of continuous
  production, 7.5 with 8 Speed upgrades: the extra steam counts in the load).
- At rest, it recovers 5 % per day. A well under 83 % of its tier's rate never wears.
- It belongs to the **column**, not to the wellhead: breaking and replacing the wellhead does not reset it, and an
  unloaded well recovers while you are away.

## Dismantling

Like Mekanism's machines, a broken wellhead keeps its energy, water, upgrades, casings, settings, side configuration and
redstone mode in the item; the steam is released. The casings stay in the ground: a new wellhead placed on the column
takes it over without drilling again.
