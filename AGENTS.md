# Project Overview

Personal blog/portfolio site for Ashish Santikari, a Software Engineer based in Berlin, Germany. Serves as a micro-blogging platform with technical articles, professional portfolio, labs section, and privacy policy.

- **Domain:** https://ashishsantikari.info
- **Repository:** https://github.com/ashishsantikari/ideas

# Tech Stack

| Technology | Version | Purpose |
|---|---|---|
| Hugo | 0.155.3 | Static site generator |
| PaperMod | v8.0+ | Theme (git submodule from github.com/adityatelange/hugo-PaperMod) |
| Netlify | — | Hosting & deployment |
| Utterances | — | GitHub issue-based comments |
| Fuse.js | — | Client-side search (bundled with PaperMod) |
| Google Tag Manager | — | Analytics (loaded after cookie consent) |

# Project Structure

```
/
├── archetypes/posts/index.md     # Blog post template
├── assets/css/extended/          # Custom CSS (loaded after theme CSS)
│   ├── custom-styles.css         # Cookie notice styling
│   ├── labs.css                  # Labs page cards
│   ├── pastel-gradient.css       # Main visual theme (gradients, glassmorphism)
│   └── resume.css                # Resume page layout
├── content/
│   ├── archive.md                # Archived posts listing
│   ├── labs.md                   # Labs/projects page
│   ├── privacy.md                # Privacy policy
│   ├── resume.md                 # Resume page (draft: true — hidden)
│   ├── search.md                 # Search page
│   └── posts/                    # Blog posts (each in own dir with index.md)
├── data/
│   ├── labs.yaml                 # Labs projects data
│   └── resume.yaml               # Resume structured data
├── hugo.yaml                     # Main Hugo configuration
├── layouts/
│   ├── _default/
│   │   ├── baseof.html           # Base template (GTM noscript, custom partials)
│   │   ├── labs.html             # Labs page layout
│   │   ├── list.html             # Homepage + section listings
│   │   ├── privacy.html          # Privacy page layout
│   │   └── resume.html           # Resume page layout
│   ├── archives.html             # Archived posts listing
│   ├── partials/
│   │   ├── comments.html         # Utterances integration
│   │   ├── cookie_consent.html   # GDPR cookie banner
│   │   ├── extend_head.html      # ServiceWorker unregistration
│   │   └── footer.html           # Custom footer with Privacy link
│   └── shortcodes/iframe.html    # Responsive iframe shortcode
├── netlify.toml                  # Netlify deploy config
├── themes/PaperMod/              # Git submodule (do not modify)
└── .tool-versions                # Hugo version pin (asdf)
```

# Commands

| Command | Description |
|---|---|
| `hugo server` | Start local dev server with live reload |
| `hugo --gc --minify` | Production build |

# Key Configuration (hugo.yaml)

- **Theme:** PaperMod
- **BaseURL:** https://ashishsantikari.info
- **Pagination:** 5 posts per page
- **ProfileMode:** Enabled (homepage shows profile with buttons to /posts/)
- **Social Icons:** Twitter, StackOverflow, GitHub, LinkedIn
- **Search:** Fuse.js (client-side, PaperMod built-in)
- **Comments:** Utterances (repo: ashishsantikari/ideas, issueTerm: pathname)
- **Navigation:** Posts → Archive → Tags → Labs
- **Syntax highlighting:** `noClasses: false` (CSS-based)

# Content Conventions

- Posts live in `content/posts/<slug>/index.md`
- Post frontmatter: `title`, `date`, `draft`, `tags`, optional `archived: true`, `cover`, `canonicalURL`, `comments: false`
- Archived posts (`archived: true`) excluded from section lists but shown on /archives/
- Archetype: `archetypes/posts/index.md`

# Custom Features

- **Iframe shortcode:** `{{< iframe src="URL" height="500" class="custom" >}}`
- **Utterances:** Comment system with automatic dark/light theme switching via MutationObserver
- **Cookie consent:** GDPR banner; Google Tag Manager loads only after acceptance (31-day persistence)
- **Pastel gradient theme:** Light mode = blue tones, dark mode = red/magenta tones, glassmorphism effects
- **Labs page:** Data-driven via `data/labs.yaml`; cards with title, version, status, description, links, tags
- **Resume page:** Data-driven via `data/resume.yaml`; currently hidden (draft: true)
- **Archives:** Separate page for posts with `archived: true`, grouped by year/month

# Deployment (Netlify)

- **Publish directory:** `public`
- **Build command:** `hugo --gc --minify`
- **Hugo version:** 0.155.3
- **Contexts:** production, split1, deploy-preview, branch-deploy
- **Redirects:** `/npmjs/*` → `/npmjs/` (200)

# Git Workflow

- **Branch patterns:** `feat/*`, `fix/*`, `blog/*`, or descriptive names
- **Commit style:** Loose conventional commits — `feat:`, `fix:`, `chore:`, `blog:`, or descriptive lowercase
- **Main branch:** `main`
- **Theme:** PaperMod pinned as git submodule (do not modify directly)

# Conventions

- No Node.js/package.json — pure Hugo + Go templates
- Vanilla CSS (no preprocessor) via Hugo Pipes in `assets/css/extended/`
- Custom layouts override PaperMod defaults by matching file paths in `layouts/`
- Do not modify files under `themes/PaperMod/` (submodule)
