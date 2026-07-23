# FoxSuda GitHub Pages

Public portfolio, game pages, privacy policies, and advertising verification files
for FoxSuda projects.

## Structure

```text
/
├── index.html
├── assets/site.css
├── games/
│   └── idle-swarm/index.html
├── privacy/
│   └── idle-swarm/index.html
└── app-ads.txt
```

## Add another game

1. Choose a permanent lowercase kebab-case slug, for example `new-game`.
2. Create `games/new-game/index.html`.
3. Create `privacy/new-game/index.html`.
4. Reuse `/assets/site.css` and the shared header/footer markup.
5. Add the game card and navigation links to `/index.html`.
6. Add only verified product and privacy facts. Do not invent store links,
   release dates, support contacts, or data practices.
7. Update `app-ads.txt` only when the advertising seller information changes.

## Local link check

Serve the repository root instead of opening HTML files directly:

```powershell
python -m http.server 8080
```

Then open `http://localhost:8080/` and verify:

- `/`
- `/games/idle-swarm/`
- `/privacy/idle-swarm/`
- `/app-ads.txt`

The site uses root-relative links because it is deployed at
`https://foxsuda.github.io/`.
