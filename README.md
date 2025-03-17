# Tatanako's homepage

A simple homepage for Tatanako, made with Nuxt.

This Project based on [vitesse-nuxt](https://github.com/antfu/vitesse-nuxt).

## How to use

### Development

```bash
git clone https://github.com/tatanakots/tatanako-homepage.git
pnpm i
pnpm dev
```

### Production

```bash
git clone https://github.com/tatanakots/tatanako-homepage.git
docker build -t tatanako-homepage .
docker run -d -p 80:3000 tatanako-homepage
```

## Known Issues

 - It sometimes throws `ERROR: failed to solve: archive/tar: unknown file mode ?rwxr-xr-x` when building the docker image on Windows by Docker Desktop.
 