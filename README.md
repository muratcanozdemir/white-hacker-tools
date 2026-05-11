# ops://cheatsheets

Practitioner-grade command references for security, infrastructure, and platform engineering.  
No fluff. No vendor marketing. Commands that people with production scars actually use.

Live at: `https://<you>.github.io/<repo>/`

---

## Published

| File | Topic | Tools | Phases |
|---|---|---|---|
| `pentest.html` | White Hat Hacker Tools | 23 | recon · web · network · exploit · post-exploit · password · wireless |
| `kubernetes.html` | Kubernetes Debugging Toolkit | 18 | inspect · network · security · health · rbac · storage |
| `terraform.html` | IaC & Terraform Ecosystem | 14 | validate · plan · security · cost · state · docs |
| `observability.html` | Observability & SRE Toolkit | 17 | metrics · logs · traces · profiling · ebpf · incident |
| `container-security.html` | Container Security Toolkit | 15 | image · build · registry · signing · runtime · supply chain |
| `go.html` | Go Developer Toolkit | 18 | build · test · profile · debug · lint · modules · release |
| `python.html` | Python Packaging & CI | 16 | env · packaging · quality · rust/ffi · publish · ci |
| `git.html` | Git & Repo Hygiene | 17 | history · forensics · security · hooks · large repos · workflow |
| `network.html` | Network Diagnostics | 18 | dns · tcp/udp · http · grpc · tls · load |
| `slurm.html` | SLURM & HPC Toolkit | 17 | submit · monitor · debug · arrays · dependencies · resources |
| `postgres.html` | PostgreSQL Operations | 18 | psql · backup · performance · maintenance · security · replication |
| `aws.html` | AWS CLI — Production Surface | 28 | auth · compute · storage · networking · secrets · observability · data/platform |
| `azure.html` | Azure CLI — Production Surface | 28 | auth · compute · storage · networking · secrets · observability · data/platform |
| `gcp.html` | GCP CLI — Production Surface | 28 | auth · compute · storage · networking · secrets · observability · data/platform |
| `digitalocean.html` | DigitalOcean CLI — Production Surface | 24 | auth · droplets · kubernetes · storage · networking · databases · apps |
| `linode.html` | Linode CLI — Production Surface | 22 | auth · linodes · kubernetes · storage · networking · databases |
| `hetzner.html` | Hetzner CLI — Production Surface | 22 | auth · servers · networks · storage · load balancers · firewalls |
| `vps-hardening.html` | VPS Hardening — Fresh to Secure | 23 | access · firewall · updates · brute-force · hardening · detection · verify |
| `kong.html` | Kong API Gateway | 22 | connect · services · routes · plugins · upstreams · deck · inspect |
| `mulesoft.html` | MuleSoft — Production Surface | 20 | deploy · ci/cd · api manager · runtime · observability · governance |
| `nginx.html` | Nginx as API Gateway | 20 | config · upstream · rate limiting · auth · tls/mtls · observability |

---

## Up next

Open roadmap. Suggestions welcome.

---

## Setup (one-time)

1. **Enable GitHub Pages via Actions**  
   Repo → Settings → Pages → Source → **GitHub Actions**

2. Push to `main` — workflow deploys automatically.

3. If an old `gh-pages` branch exists and the wrong page is served:
   ```bash
   git push origin --delete gh-pages
   git commit --allow-empty -m "trigger pages redeploy"
   git push origin main
   ```

## Local preview

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Structure

```
.
├── index.html                  # hub / landing page
├── pentest.html
├── kubernetes.html
├── terraform.html
├── observability.html
├── container-security.html
├── go.html
├── python.html
├── git.html
├── network.html
├── slurm.html
├── postgres.html
├── aws.html
├── azure.html
├── gcp.html
├── digitalocean.html
├── linode.html
├── hetzner.html
├── vps-hardening.html
├── kong.html
├── mulesoft.html
├── nginx.html
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml
```

## Adding a new post

1. Create `<topic>.html` — copy structure from an existing page, change accent colour
2. Add a card to `index.html` under `<div class="posts">`
3. Push — deploys in ~60s

## Design principles

- Single self-contained HTML files — no build step, no framework, no CDN beyond one Google Fonts request
- Each page has a distinct accent colour — visual identity per domain
- Filter by phase, copy-to-clipboard per command block
- Ordered steps where sequence matters (VPS hardening), unordered elsewhere
- Commands that get used, not commands that fill space
- Honest about what doesn't belong — every page has an explicit exclusion callout
