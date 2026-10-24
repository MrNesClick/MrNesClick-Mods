# Commands

Operator commands (permission level 2), for server admins and modpack makers. `<pos>` is the position of a wellhead
or an adapter.

| Command | What it does |
|---|---|
| `/mekanismgeothermal debug <pos>` | Drilling, heat, production, tanks, safety, upgrades and faces of a wellhead; link and state of an adapter |
| `/mekanismgeothermal target <pos> <y>` | Target depth (absolute Y) |
| `/mekanismgeothermal drill <pos> <start\|stop>` | The Start and Pause drilling buttons |
| `/mekanismgeothermal emergency <pos> <stop\|reset>` | Emergency stop and manual reset |
| `/mekanismgeothermal upgrades <pos> <speed> <energy>` | Installed upgrade counts (0 to 8) |
| `/mekanismgeothermal redstone <pos> <disabled\|high\|low>` | Redstone control of a wellhead |
| `/mekanismgeothermal security <pos> <public\|private\|trusted>` | Access mode of a wellhead or an adapter |
| `/mekanismgeothermal face <pos> <energy\|fluid\|chemical\|item> <front\|back\|left\|right\|bottom> <mode>` | A face's mode in Mekanism's side configuration (`none`, `input`, `output`, `input_output`...) |
| `/mekanismgeothermal face <pos> <type> eject <on\|off>` | Auto-eject of one kind of transfer |
| `/mekanismgeothermal adapter <pos> link <well pos>` | Links an adapter to a well |
| `/mekanismgeothermal adapter <pos> unlink` | Unlinks it |
| `/mekanismgeothermal adapter <pos> condition <condition> [inverted]` | Its condition, optionally inverted |
| `/mekanismgeothermal exhaustion <pos> <value>` | Exhaustion of the column at that X/Z (0 to 1) |
