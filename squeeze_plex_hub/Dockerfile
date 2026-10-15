# BUILD_VERSION est fourni par le Supervisor de HA : c'est la "version" de config.yaml
ARG BUILD_VERSION
FROM onmomo/squeeze-plex-hub:${BUILD_VERSION}

# Les réglages de l'app (lecteurs masqués, paires stéréo) sont stockés dans /app/config :
# on les redirige vers /data, le stockage persistant de l'extension (conservé aux mises à jour et sauvegardé par HA)
CMD ["sh", "-c", "mkdir -p /data/config && rm -rf /app/config && ln -s /data/config /app/config && exec node /app/server/index.mjs"]
