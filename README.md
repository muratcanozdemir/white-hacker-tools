# ops://cheatsheets

Practitioner-grade command references for security, infrastructure, and platform engineering.  
Live at: `https://<you>.github.io/<repo>/`

## Posts

| File | Topic |
|---|---|
| `index.html` | Hub / landing page |
| `pentest.html` | White Hat Hacker Tools |
| `kubernetes.html` | Kubernetes Debugging Toolkit |

## Setup (one-time)

1. **Enable GitHub Pages via Actions**  
   Repo → Settings → Pages → Source → **GitHub Actions**

2. Push to `main` — the workflow runs automatically.

## Local preview

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Adding a new post

1. Create `<topic>.html` (copy structure from an existing page)
2. Add a card to `index.html` under `<div class="posts">`
3. Push — deploys in ~60s

## Structure

```
.
├── index.html          # hub
├── pentest.html        # white hat tools
├── kubernetes.html     # k8s debug toolkit
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml
```
