# Felicia Falck

Official website for Felicia Falck — Nordic Folk, Medicine Music, and Vispop from Bohuslän, Sweden.

## Live Site

`feliciafalck.com`

## Structure

```
.
├── index.html      # Main site (single-page, no build step)
├── favicon.svg     # Site icon
├── deploy.sh       # Deployment script
└── README.md
```

No build process — pure HTML/CSS/JS.

## Deployment

The site is hosted on a VPS via **Docker + Caddy**, served as static files.

To deploy:

```bash
./deploy.sh
```

This copies `index.html` and `favicon.svg` to `~/services/feliciafalck/site/` and reloads Caddy.

### Infrastructure

- **Reverse proxy / HTTPS:** Caddy (Docker container)
- **Config:** `~/services/caddy/Caddyfile`
- **Docker Compose:** `~/services/docker-compose.yml`
- **Site files:** `~/services/feliciafalck/site/`

## Local Development

```bash
python3 -m http.server 8000
# open http://localhost:8000
```
