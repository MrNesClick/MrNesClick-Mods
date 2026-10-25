# Adaptateur logique géothermique

Une sortie redstone pour **une condition** d'un puits lié, ou une entrée redstone qui enclenche son arrêt d'urgence.

![L'interface de l'adaptateur logique](../assets/mekanistic-geothermal/media-06-logic-adapter.png)

## Liaison

- **Posez-le contre une tête de puits** : il se lie tout seul.
- Ou, de plus loin (même dimension, jusqu'à 64 blocs par défaut) : faites un clic droit sur la tête de puits avec un
  **Configurateur** de Mekanism, puis sur l'adaptateur. Un clic droit accroupi le délie.

L'adaptateur est **hors ligne**, sans signal, tant que le chunk de son puits n'est pas chargé. Son écran affiche la
liaison (en ligne, hors ligne, pas de tête de puits, trop loin, non lié), la pression du puits, son débit de vapeur et
son état, et la sortie.

## Conditions

Choisissez la condition dans la liste de l'adaptateur ; **Inversé** émet un signal quand la condition est fausse.

| Condition | Signal tant que |
|---|---|
| Désactivé | jamais (aucune sortie) |
| Production | le puits produit de la vapeur |
| Forage | la foreuse travaille (forage ou réparation) |
| Forage bloqué | la foreuse attend : énergie, tubages, déblais pleins, lave, bloc interdit ou protégé |
| Cible atteinte | la foreuse a atteint la profondeur cible |
| Haute pression | la pression atteint le seuil de la soupape (80 %) |
| Soupape ouverte | la soupape de sécurité évacue de la vapeur |
| Soupape obstruée | un bloc posé sur la tête de puits empêche la soupape d'évacuer |
| Arrêt automatique | l'arrêt de haute pression bloque la production |
| Manque d'eau | la production attend de l'eau |
| Énergie faible | le système de contrôle ou la foreuse manque d'énergie |
| Colonne endommagée | un tubage manque dans la colonne |
| Déblais pleins | l'inventaire des déblais est plein |
| Plus de tubages | la foreuse n'a plus de tubages |
| Arrêt d'urgence | l'arrêt d'urgence est enclenché |
| Entrée d'arrêt d'urgence | aucune sortie : un signal redstone sur l'adaptateur enclenche l'arrêt d'urgence du puits |

En mode entrée, l'arrêt d'urgence s'enclenche sur le front montant du signal ; réarmer le puits pendant que le signal
reste actif ne le réenclenche pas.

## Sécurité

L'adaptateur utilise la sécurité de Mekanism, comme la tête de puits : seuls son propriétaire et les joueurs de
confiance (ou tout le monde, s'il est public) peuvent l'ouvrir ou le lier.
