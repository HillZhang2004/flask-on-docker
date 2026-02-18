# Flask on Docker

![CI](https://github.com/HillZhang2004/flask-on-docker/actions/workflows/ci.yml/badge.svg)

A containerized Flask web service deployed behind Gunicorn and Nginx, with Postgres for persistence. This repo follows a multi-service “Instagram-style” stack and is designed as a production-like hello world that supports uploading and viewing images.

## Demo
TODO: Replace with a GIF showing: start service → upload image → view image.

![Demo](img/demo.gif)

## Tech Stack
- Flask (app)
- Gunicorn (WSGI server)
- Nginx (reverse proxy)
- Postgres (database)
- Docker / Docker Compose (orchestration)
- GitHub Actions (CI build check)

## Build / Run (Development)
1. Clone this repo.
2. Bring services up:
   - `docker compose up --build`
3. Open the site in your browser (port/URL depends on your compose config).
4. Stop services:
   - `docker compose down`

## Security Notes
- Do not commit production credentials.
- This repo ignores `.env.prod.db` via `.gitignore`.
