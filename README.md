# Flask on Docker

![CI](https://github.com/YOUR_GITHUB_USERNAME/flask-on-docker/actions/workflows/ci.yml/badge.svg)

A containerized Flask web service deployed behind Gunicorn and Nginx, with Postgres for persistence. This repo follows a multi-service “Instagram-style” stack and is designed as a production-like hello world that supports uploading and viewing images.

## Demo
> TODO: Replace with a GIF showing: start service → upload image → view image.
![Demo](img/demo.gif)

## Tech Stack
- Flask (app)
- Gunicorn (WSGI server)
- Nginx (reverse proxy)
- Postgres (database)
- Docker / Docker Compose (orchestration)
- GitHub Actions (CI build check)

## Build / Run (Development)
1. Install Docker and Docker Compose.
2. Clone this repo.
3. Follow the tutorial steps in this repo directory to create the required Docker/compose/app files.
4. Bring the services up:
   - `docker compose up --build`
5. Open the site in your browser (port/URL depends on your compose config).

To stop:
- `docker compose down`

## Security Notes
- Never commit production credentials.
- This repo explicitly ignores `.env.prod.db` (database credentials) via `.gitignore`.
