# NEOCRAFT

Prototype de jeu de survie en blocs jouable directement dans un navigateur, sans dépendance ni compilation.

## Lancer le jeu

```bash
python3 -m http.server 8080
```

Ouvrez ensuite `http://localhost:8080`. Choisissez une graine et créez ou rejoignez un monde.

## Fonctions

- Terrain déterministe et biomes générés depuis la graine.
- Déplacement en vue 3D, destruction et pose de blocs.
- Inventaire, établi, recettes de planches et d'épée.
- Cycle jour/nuit, faim, points de vie et monstres nocturnes.
- Synchronisation locale entre onglets via `BroadcastChannel` (même graine).
- Sauvegarde de la position, inventaire et modifications du monde dans `localStorage`.
- Interface adaptative pour ordinateur, tablette et téléphone, avec commandes tactiles et prise en charge clavier/souris.

### Jouer sur tous les appareils

Le jeu fonctionne dans un navigateur récent sur ordinateur, tablette et téléphone. Sur écran tactile, utilisez le pavé directionnel en bas à gauche pour vous déplacer, faites glisser le doigt sur le monde pour regarder autour de vous, puis utilisez les boutons à droite pour miner, poser un bloc ou ouvrir l’établi. Le rendu limite automatiquement sa résolution interne sur les écrans très denses pour préserver les performances.

### Paramètres, langues et commandes administrateur

Le bouton **⚙** ouvre les paramètres pendant une partie. L’interface des paramètres est disponible en français, anglais et espagnol ; le choix est conservé dans le navigateur.

L’**espace code** active les commandes administrateur pour l’onglet courant avec le code `2464`. Appuyez sur `Entrée` pour ouvrir la console, puis utilisez notamment :

- `/help` — afficher l’aide des commandes.
- `/day` ou `/night` — régler l’heure.
- `/give <objet> <quantité>` — ajouter jusqu’à 64 objets (`wood`, `stone`, `grass`, `dirt`, `plank`, `sword`, `apple`).
- `/heal`, `/tp <x> <z>` ou `/clear` — soigner, se téléporter ou vider l’inventaire.

L’activation est limitée à la session locale de l’onglet : elle n’est ni sauvegardée ni synchronisée avec les autres joueurs.

### Commandes

`WASD` pour se déplacer, souris pour regarder, clic gauche pour miner/attaquer,
clic droit pour poser, `1` à `7` pour choisir un objet et `E` pour l'établi.
