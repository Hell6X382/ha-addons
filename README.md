# Add-ons Home Assistant

Dépôt d'extensions (apps) Home Assistant personnelles.

## Ajouter le dépôt dans Home Assistant

**Paramètres > Modules complémentaires > Boutique > ⋮ > Dépôts**, ajouter :

```
https://github.com/Hell6X382/ha-addons
```

## Extensions

| Extension | Description |
|---|---|
| [Squeeze Plex Hub](squeeze_plex_hub) | Diffuse Plexamp vers les lecteurs Squeezebox / Lyrion, à partir de l'image officielle [onmomo/squeeze-plex-hub](https://github.com/onmomo/squeeze-plex-hub) |

## Mises à jour automatiques

Le workflow [`update-squeeze-plex-hub.yml`](.github/workflows/update-squeeze-plex-hub.yml) vérifie chaque nuit Docker Hub.
Quand une nouvelle version de l'image officielle est publiée (arm64 + amd64), il met à jour `version` dans
`squeeze_plex_hub/config.yaml`. Home Assistant détecte la nouvelle version et l'installe si l'option
**Mise à jour automatique** de l'extension est activée.

Pour revenir à une version précédente : remettre l'ancien numéro dans `config.yaml` puis reconstruire l'extension.
