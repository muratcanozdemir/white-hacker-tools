# White Hat Hacker Tools — Cheat Sheet

Filterable, single-page reference for penetration testing tools.  
Live at: `https://<you>.github.io/<repo>/`

## Setup (one-time)

1. **Enable GitHub Pages via Actions**  
   Repo → Settings → Pages → Source → **GitHub Actions**

2. Push to `main` — the workflow runs automatically.

## Local preview

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Structure

```
.
├── index.html                    # entire site — self-contained
└── .github/
    └── workflows/
        └── deploy.yml            # Pages deployment workflow
```

## Legal

Use only against systems you own or have explicit written authorisation to test.
