# LivingPanda Pi Utility

Canonical LivingPanda source for the Pi Desktop SoloHost utility.

## v0.2.0

Adds a mobile-friendly, read-only local dashboard for:

- Pi Node TCP reachability on ports 31401–31403
- this SoloHost container's own runtime health
- allow-listed LivingPanda data-worker health

It deliberately does **not** mount the Docker socket, mount host directories, run privileged, or connect to Commander control.

## Architecture

- Canonical source: `LivingPanda-Online/LivingPanda-Pi-SoloHost-Probe`
- Public distribution image: `ghcr.io/noorelahmanifestofinal/livingpanda-pi-solohost-probe:0.2.0`
- Public distribution repo: `noorelahmanifestofinal/LivingPanda-Pi-SoloHost-Probe-Public`

## Local test

```powershell
docker compose -f docker-compose.local.yml up -d --build
```

Open `http://127.0.0.1:18081`.

## Security boundary

No database credentials, API keys, Commander commands, Docker socket, privileged mode, or host filesystem mounts.
