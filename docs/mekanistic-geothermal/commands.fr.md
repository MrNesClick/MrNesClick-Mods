# Commandes

Commandes d'opérateur (niveau de permission 2), pour les administrateurs de serveur et les créateurs de modpacks.
`<pos>` est la position d'une tête de puits ou d'un adaptateur.

| Commande | Ce qu'elle fait |
|---|---|
| `/mekanismgeothermal debug <pos>` | Forage, chaleur, production, réservoirs, sécurité, améliorations et faces d'une tête de puits ; liaison et état d'un adaptateur |
| `/mekanismgeothermal target <pos> <y>` | Profondeur cible (Y absolu) |
| `/mekanismgeothermal drill <pos> <start\|stop>` | Les boutons Démarrer et Suspendre le forage |
| `/mekanismgeothermal emergency <pos> <stop\|reset>` | Arrêt d'urgence et réarmement manuel |
| `/mekanismgeothermal upgrades <pos> <speed> <energy>` | Nombre d'améliorations installées (0 à 8) |
| `/mekanismgeothermal redstone <pos> <disabled\|high\|low>` | Contrôle redstone d'une tête de puits |
| `/mekanismgeothermal security <pos> <public\|private\|trusted>` | Mode d'accès d'une tête de puits ou d'un adaptateur |
| `/mekanismgeothermal face <pos> <energy\|fluid\|chemical\|item> <front\|back\|left\|right\|bottom> <mode>` | Le mode d'une face dans la configuration des faces de Mekanism (`none`, `input`, `output`, `input_output`...) |
| `/mekanismgeothermal face <pos> <type> eject <on\|off>` | Éjection automatique d'un type de transfert |
| `/mekanismgeothermal adapter <pos> link <well pos>` | Lie un adaptateur à un puits |
| `/mekanismgeothermal adapter <pos> unlink` | Le délie |
| `/mekanismgeothermal adapter <pos> condition <condition> [inverted]` | Sa condition, éventuellement inversée |
| `/mekanismgeothermal exhaustion <pos> <value>` | Épuisement de la colonne à ce X/Z (de 0 à 1) |
