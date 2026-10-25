# Sécurité

La **pression** d'un puits est le taux de remplissage de son réservoir de vapeur (64 000 mB pour le tier basique). Elle
monte quand la vapeur n'a nulle part où aller. Trois systèmes la maîtrisent, et un quatrième arrête tout.

| Pression | Ce qui se passe |
|---|---|
| 80 % | La **soupape de sécurité** s'ouvre et évacue de la vapeur (s'il y a de l'air juste au-dessus de la tête de puits). |
| 90 % | L'**arrêt automatique** coupe la production. |
| sous 50 % | La production redémarre. |
| 100 % | Plein : si rien ne soulage le puits, une **éruption** peut se produire (désactivée par défaut). |

## Soupape de sécurité

- C'est la **face du haut** de la tête de puits, et elle a besoin d'**air juste au-dessus**. Un bloc à cet endroit
  l'obstrue : l'interface et l'adaptateur logique le signalent.
- Elle est **mécanique** : elle fonctionne sans énergie (`valveNeedsEnergy` change cela).
- Elle évacue au plus la moitié du débit de vapeur max, et seulement jusqu'à 80 % : elle ralentit une montée de
  pression, elle ne masque pas une sortie bouchée.

## Système de contrôle

Le système de contrôle consomme un peu d'énergie (20 FE/t pour le tier basique, ×4 avec 8 mises à niveau de vitesse,
÷10 avec 8 mises à niveau énergétiques). Sans énergie il ne peut pas agir, et l'écran principal l'indique.

- **Arrêt automatique** : coupe la production à 90 % de pression et la relance sous 50 %.
- **Verrou de manque d'eau** : quand le réservoir d'eau est à sec, la production attend qu'il remonte au-dessus de
  10 %, au lieu de hoqueter.

Sans énergie, les deux sont relâchés et la production continue (l'ébullition elle-même est passive).

## Arrêt d'urgence

Le bouton rouge **Arrêt d'urgence** de l'interface (ou un adaptateur logique en mode entrée) arrête le forage et la
production, même sans énergie. Le puits reste arrêté jusqu'à ce que quelqu'un le **réarme** avec le même bouton.
L'arrêt est enregistré avec la tête de puits, mais pas conservé dans son objet quand elle est démontée.

## Comparateur

Un comparateur à côté de la tête de puits lit la pression : 0 à vide, 8 à 50 %, 15 quand le réservoir est plein.

## Éruptions (désactivées par défaut)

Un serveur peut les activer (`[eruption] mode`) : `STEAM_JET` (des brûlures autour du haut du puits, la moitié de la
vapeur relâchée) ou `EXPLOSION`. Une éruption demande un puits à **pleine pression, chauffé et alimenté en eau**, que
rien ne soulage : soupape obstruée, désactivée ou sans énergie, et arrêt automatique désactivé ou sans énergie. Après
30 secondes à pleine pression, chaque seconde a 2 % de chances (environ 50 secondes en moyenne). Avec l'explosion, la
tête de puits est projetée sous forme d'objet qui garde son contenu, et les tubages restent en place.
