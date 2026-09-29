# LivingPanda Pi SoloHost Probe

Canonical LivingPanda source for the minimal Pi Desktop SoloHost compatibility probe.

## Architecture

- Canonical source: `LivingPanda-Online/LivingPanda-Pi-SoloHost-Probe`
- Public distribution image: `ghcr.io/noorelahmanifestofinal/livingpanda-pi-solohost-probe:0.1.0`
- Public distribution repo: `noorelahmanifestofinal/LivingPanda-Pi-SoloHost-Probe-Public`

The separate public distribution image exists because the LivingPanda-Online organization intentionally blocks public package visibility.

## Safety boundary

This probe contains no database, API keys, Commander access, host filesystem mounts, privileged Docker access, or private LivingPanda data.

## Local test

```powershell
docker compose -f docker-compose.local.yml up -d --build
```

Open `http://127.0.0.1:18080`.

## Pi SoloHost package

The `package/` directory contains the validated `docker-compose.yml` and `config_options.yml`.
