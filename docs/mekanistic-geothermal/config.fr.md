# Configuration

Chaque mécanique, débit et seuil de Mekanistic Geothermal est configurable. Les valeurs par défaut sont douces ; un
modpack peut rendre le mod plus difficile ou plus facile, ou désactiver n'importe quelle mécanique.

## Fichiers

| Fichier | Côté | Contenu |
|---|---|---|
| `config/mekanismgeothermal-server.toml` | Serveur (synchronisé avec les joueurs) | Tout ce qui change le jeu : tiers, forage, chaleur, production, sécurité, éruptions, interférence, épuisement, améliorations, adaptateur |
| `config/mekanismgeothermal-client.toml` | Chaque joueur | Affichage du guide |

Le fichier serveur est créé avec ses valeurs par défaut au premier lancement du jeu ou du serveur. Pour des réglages
propres à un seul monde, copiez le fichier dans `<monde>/serverconfig/mekanismgeothermal-server.toml` et modifiez cette
copie.

Les modifications du fichier serveur sont **rechargées pendant la partie** : pas besoin de redémarrer.

!!! tip "Pourcentages"
    Les ratios s'écrivent de 0 à 1 : `0.8` vaut 80 %. La pression est le taux de remplissage du réservoir de vapeur de
    la tête de puits.

Les tableaux ci-dessous reprennent le fichier de config tel qu'il est écrit, donc en anglais, comme ses commentaires.

## Options du serveur

--8<-- "mekanistic-geothermal/server.md"

## Options du client

--8<-- "mekanistic-geothermal/client.md"
