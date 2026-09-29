# LivingPanda Pi SoloHost Probe

Minimal, intentionally isolated compatibility probe for Pi Desktop SoloHost.

## Purpose

Verify the complete path:

`LivingPanda source -> GitHub -> GHCR -> Pi SoloHost -> local Pi Desktop UI`

## Safety boundary

This probe has:

- no database
- no API keys
- no Commander control
- no host filesystem mounts
- no privileged Docker access
- no private LivingPanda data

## Local test

```powershell
docker compose -f docker-compose.local.yml up -d --build
```

Open `http://127.0.0.1:18080`.

## Pi SoloHost package

The `package/` directory contains:

- `docker-compose.yml`
- `config_options.yml`

The published image is:

`ghcr.io/livingpanda-online/livingpanda-pi-solohost-probe:0.1.0`

Version: **0.1.0**
