Personal website for `www.jaimeo.me`.

Current structure:
- homepage at `/`
- blog at `/blog/`, currently hidden from navigation
- GitHub Pages deployment through GitHub Actions

Local development:
1. Start Docker Desktop.
2. Run `docker compose up`.
3. Open `http://127.0.0.1:4000`.

Useful Docker commands:
- `docker compose build` rebuilds the Ruby 3.3 Jekyll image.
- `docker compose run --rm site bundle exec jekyll build` verifies the site compiles.

Notes:
- `CNAME` preserves the custom domain.
- Posts live in `_posts/`.
- The Docker image uses Ruby 3.3, matching the GitHub Pages-supported Ruby line.
