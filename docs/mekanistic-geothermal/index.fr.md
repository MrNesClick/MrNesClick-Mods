# Mekanistic Geothermal

![Mekanistic Geothermal](../assets/mekanistic-geothermal/logo.png){ align=right width="128" }

Un addon pour **[Mekanism](https://www.curseforge.com/minecraft/mc-mods/mekanism)** : une tête de puits géothermique
qui fore elle-même son puits et transforme l'eau en vapeur grâce à la chaleur des profondeurs, pour les turbines de
Mekanism.

!!! warning "Alpha"
    Jouable, mais attendez-vous à des bugs et à des changements d'équilibrage. Sauvegardez votre monde avant de mettre à
    jour, et [signalez ce que vous trouvez](https://github.com/MrNesClick/MrNesClick-Mods/issues/new/choose).

![Une tête de puits géothermique basique qui relâche de la vapeur](../assets/mekanistic-geothermal/media-01-hero.png)

## En bref

- **Elle fore son propre puits.** Mettez des tubages de puits en acier dans ses emplacements, réglez la profondeur
  cible et appuyez sur *Démarrer le forage* : elle descend d'un bloc à la fois, un tubage par bloc, et s'arrête à la
  cible ou sur de la lave.
- **Plus c'est profond, plus c'est chaud.** La chaleur augmente avec la profondeur, et la lave près du fond en ajoute.
  Un puits basique profond produit environ **400 mB/t** de vapeur Mekanism : bien plus que les générateurs passifs,
  bien moins qu'un réacteur à fission.
- **Une vraie machine Mekanism.** Son interface, sa configuration des faces et son éjection automatique, le
  Configurateur, les mises à niveau de vitesse et d'énergie, le contrôle redstone et la sécurité sont ceux de Mekanism.
- **Sûre par défaut.** Une soupape mécanique évacue au-dessus de 80 % de pression, le système de contrôle arrête la
  production à 90 % et quand l'eau manque, et un arrêt d'urgence coupe tout. Les éruptions sont désactivées par défaut.
- **Tout est configurable**, doux par défaut et plus exigeant si votre modpack le veut.

![La colonne de tubage qui descend jusqu'à un lac de lave](../assets/mekanistic-geothermal/media-02-column.png)

## Pour aller plus loin

- [Prise en main](getting-started.md) : de la recette à la vapeur dans une turbine, étape par étape.
- [La tête de puits](wellhead.md) : forage, chaleur et vapeur, interférence, épuisement, démontage.
- [Sécurité](safety.md) : pression, soupape de sécurité, arrêt automatique, arrêt d'urgence, éruptions.
- [Améliorations](upgrades.md) : ce que font les mises à niveau de vitesse et d'énergie, et leur prix.
- [Adaptateur logique](logic-adapter.md) : des signaux redstone depuis un puits, et son entrée d'arrêt d'urgence.
- [Configuration](config.md) : toutes les options, avec leur valeur par défaut.
- [Commandes](commands.md) : les commandes d'opérateur.

## Prérequis

| Minecraft | Loader | Mekanism | Optionnel |
|---|---|---|---|
| 1.21.1 | NeoForge 21.1.194+ | 10.7.19+ | Mekanism Generators (sa turbine industrielle transforme la vapeur en énergie) |

## Téléchargement

[CurseForge](https://www.curseforge.com/minecraft/mc-mods/mekanistic-geothermal) ·
[Signaler un bug](https://github.com/MrNesClick/MrNesClick-Mods/issues/new?template=3-mekanistic-geothermal-bug.yml)
