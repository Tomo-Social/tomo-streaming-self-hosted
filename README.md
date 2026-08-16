# Tomo Streaming Self-hosted

Despliegue independiente de la red social Tomo. Requiere Docker en un worker Linux y una API key de al menos 24 caracteres.

```bash
cp .env.example .env
docker compose up -d
curl http://localhost:8090/health
curl http://localhost:8090/api/v1/stream-servers
```

Configura únicamente los recursos disponibles. Cámara usa V4L2; escritorio usa X11; audio usa PulseAudio. Para producción añade TLS, TURN, una red privada para Docker y un proxy que exponga `/signaling` mediante WebSocket.
