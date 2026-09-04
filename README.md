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

### Commandes

`WASD` pour se déplacer, souris pour regarder, clic gauche pour miner/attaquer,
clic droit pour poser, `1` à `7` pour choisir un objet et `E` pour l'établi.
