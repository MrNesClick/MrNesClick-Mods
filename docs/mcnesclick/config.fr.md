# Configuration

Tout MCNesclick se règle dans un seul fichier, `config/mcnesclick.toml`, dans le dossier du jeu ou du serveur. C'est le
même fichier sur tous les loaders et toutes les versions de Minecraft.

- Le fichier est créé au premier lancement, avec un commentaire au-dessus de chaque option. Une clé manquante est
  rajoutée avec sa valeur par défaut.
- Une valeur invalide est signalée dans le log et remplacée par la valeur par défaut tant que vous ne la corrigez pas.
- **Quand les changements s'appliquent** : recettes, effets, pommes des feuilles et feu de camp protecteur avec
  `/reload` (ou au redémarrage du monde ou du serveur). La faim et la saturation demandent un redémarrage du jeu ou du
  serveur.
- **Sur un serveur**, c'est le fichier du serveur qui compte. Les joueurs devraient avoir les mêmes valeurs de faim et
  de saturation, pour que les infobulles des objets correspondent.

## Effets

Les pommes d'émeraude et de diamant prennent une liste d'effets, chacun écrit `"id_effet secondes niveau"` :

```toml
effects = ["minecraft:haste 300 2", "minecraft:night_vision 300 1"]
```

- Le `niveau` 1 est le niveau I, 2 le niveau II, et ainsi de suite (jusqu'à 256).
- Les `secondes` vont de 1 à 86400 (un jour).
- N'importe quel identifiant d'effet fonctionne, y compris ceux des mods. `[]` ne donne aucun effet.
- Une entrée invalide ou un effet inconnu est signalé une fois dans le log, puis ignoré.

## Options

Le tableau reprend le fichier de config tel qu'il est écrit, donc en anglais, comme ses commentaires.

--8<-- "mcnesclick/config.md"

## Pour les créateurs de modpacks

Chaque recette est une recette de datapack standard : vous pouvez la remplacer avec un datapack, **KubeJS** ou
**CraftTweaker**, sans autre mod :

| Identifiant de recette | Quoi |
|---|---|
| `mcnesclick:emerald_apple` | pomme d'émeraude (table de craft) |
| `mcnesclick:diamond_apple` | pomme de diamant (table de craft) |
| `mcnesclick:cooked_apple_from_smelting`, `_from_smoking`, `_from_campfire_cooking`, `_from_blasting` | pomme cuite |

Un datapack en remplace une en plaçant un fichier dans `data/mcnesclick/recipe/<id>.json` (`recipes/` avant
Minecraft 1.21). La faim, la saturation et les effets viennent de `config/mcnesclick.toml` : fournissez votre propre
copie avec le pack.
