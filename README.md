# Netlify Snippets for Sublime Text

[![Package Control](https://img.shields.io/packagecontrol/dt/Netlify.svg?style=flat-square)](https://packagecontrol.io/packages/Netlify)
[![Sublime Text](https://img.shields.io/badge/Sublime%20Text-3%2F4-ff9800.svg?style=flat-square&logo=sublimetext&logoColor=white)](https://www.sublimetext.com/)
[![License](https://img.shields.io/github/license/renzojohnson/Netlify.svg?style=flat-square)](LICENSE)

125 curated snippets for Netlify development — netlify.toml, CLI, Functions, Edge Functions, Forms, Blobs, Image CDN, Build Plugins, and Deployment.

**Author:** [Renzo Johnson](https://renzojohnson.com)

> This is an unofficial community package and is not affiliated with Netlify Inc.

## Installation

### Package Control (recommended)

1. Open Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`)
2. Type **Install Package**
3. Search for **Netlify**

### Manual

Clone into your Sublime Text `Packages` directory:

```bash
# macOS
cd ~/Library/Application\ Support/Sublime\ Text/Packages
git clone https://github.com/renzojohnson/Netlify.git

# Linux
cd ~/.config/sublime-text/Packages
git clone https://github.com/renzojohnson/Netlify.git

# Windows
cd %APPDATA%\Sublime Text\Packages
git clone https://github.com/renzojohnson/Netlify.git
```

## Usage

Type `nt:` and browse the autocomplete menu, then press **Tab** to expand.

| Prefix | Category | Count |
|--------|----------|-------|
| `nt:toml:` | netlify.toml config | 25 |
| `nt:flat:` | _redirects & _headers | 8 |
| `nt:cli:` | CLI commands | 20 |
| `nt:fn:` | Serverless Functions | 18 |
| `nt:edge:` | Edge Functions | 15 |
| `nt:form:` | Forms & Identity | 10 |
| `nt:blob:` | Blobs & Storage | 8 |
| `nt:img:` | Image CDN | 5 |
| `nt:plugin:` | Build Plugins | 8 |
| `nt:deploy:` | Deployment & CI | 8 |

### TOML Snippets Requirement

The 25 `nt:toml:*` snippets (plus `nt:img:config` and 3 deploy snippets) require a **TOML syntax package** for autocomplete to work in `.toml` files. Sublime Text does not include TOML syntax by default.

**Install via Package Control:** search for **TOML** (by jasonwilliams).

Without a TOML syntax package, Sublime Text opens `.toml` files as Plain Text and TOML-scoped snippets will not appear in autocomplete.

## Snippet Reference

### netlify.toml Config (`nt:toml:*`) — 25 snippets

| Trigger | Description |
|---------|-------------|
| `nt:toml:init` | netlify.toml — minimal starter |
| `nt:toml:full` | netlify.toml — full config scaffold |
| `nt:toml:build` | Build command and publish directory |
| `nt:toml:build:env` | Build environment variables |
| `nt:toml:redirect` | Redirect rule |
| `nt:toml:redirect:splat` | Redirect with splat wildcard |
| `nt:toml:redirect:proxy` | Proxy redirect (200 rewrite) |
| `nt:toml:redirect:country` | Country-based redirect |
| `nt:toml:redirect:role` | Role-based redirect (Identity) |
| `nt:toml:redirects` | Multiple redirect rules |
| `nt:toml:header` | Custom header rule |
| `nt:toml:headers` | Security + CORS headers |
| `nt:toml:headers:cache` | Cache-Control headers |
| `nt:toml:plugin` | Build plugin |
| `nt:toml:plugins` | Multiple build plugins |
| `nt:toml:functions` | Functions configuration |
| `nt:toml:edge` | Edge function declaration |
| `nt:toml:context:production` | Production context override |
| `nt:toml:context:branch` | Branch deploy context override |
| `nt:toml:context:preview` | Deploy preview context override |
| `nt:toml:dev` | Local dev server config |
| `nt:toml:processing` | Post-processing (CSS/JS/HTML/images) |
| `nt:toml:spa` | SPA fallback redirect |
| `nt:toml:pretty` | Build config with pretty URLs |
| `nt:toml:env` | Build environment variables |

### Flat Config Files (`nt:flat:*`) — 8 snippets

| Trigger | Description |
|---------|-------------|
| `nt:flat:redirect` | _redirects — single rule |
| `nt:flat:redirect:splat` | _redirects — splat wildcard |
| `nt:flat:redirect:proxy` | _redirects — proxy rewrite |
| `nt:flat:spa` | _redirects — SPA fallback |
| `nt:flat:redirect:country` | _redirects — country-based |
| `nt:flat:header` | _headers — custom header rule |
| `nt:flat:headers:security` | _headers — security headers |
| `nt:flat:headers:cache` | _headers — cache control |

### CLI Commands (`nt:cli:*`) — 20 snippets

| Trigger | Description |
|---------|-------------|
| `nt:cli:deploy` | Deploy to draft URL |
| `nt:cli:deploy:prod` | Deploy to production |
| `nt:cli:deploy:dir` | Deploy specific directory |
| `nt:cli:dev` | Start local dev server |
| `nt:cli:dev:live` | Live share dev server |
| `nt:cli:env:set` | Set environment variable |
| `nt:cli:env:get` | Get environment variable |
| `nt:cli:env:list` | List environment variables |
| `nt:cli:env:unset` | Remove environment variable |
| `nt:cli:env:import` | Import env vars from file |
| `nt:cli:sites:create` | Create new site |
| `nt:cli:sites:list` | List all sites |
| `nt:cli:link` | Link directory to site |
| `nt:cli:build` | Build locally with Netlify config |
| `nt:cli:functions:create` | Scaffold a new function |
| `nt:cli:functions:serve` | Serve functions locally |
| `nt:cli:open` | Open site or admin (open:site, open:admin) |
| `nt:cli:logs` | Tail function logs |
| `nt:cli:blobs:set` | Set a blob value |
| `nt:cli:login` | Authenticate CLI |

### Serverless Functions (`nt:fn:*`) — 18 snippets

| Trigger | Description |
|---------|-------------|
| `nt:fn:handler` | Functions v2 handler |
| `nt:fn:get` | GET handler |
| `nt:fn:post` | POST handler |
| `nt:fn:crud` | Multi-method handler (GET/POST/PUT/DELETE) |
| `nt:fn:scheduled` | Scheduled function (cron) |
| `nt:fn:background` | Background function (name file *-background.mts) |
| `nt:fn:stream` | Streaming function response |
| `nt:fn:context` | Function with context (geo, IP, params) |
| `nt:fn:env` | Environment variable access (Netlify.env) |
| `nt:fn:cors` | CORS-enabled function |
| `nt:fn:redirect` | Redirect response |
| `nt:fn:json` | JSON response |
| `nt:fn:error` | Error response |
| `nt:fn:cookies` | Cookie handling |
| `nt:fn:params` | URL search params extraction |
| `nt:fn:dynamic` | Dynamic route params |
| `nt:fn:form` | Form data handler |
| `nt:fn:fetch` | External API fetch proxy |

### Edge Functions (`nt:edge:*`) — 15 snippets

| Trigger | Description |
|---------|-------------|
| `nt:edge:handler` | Edge Function handler (typed) |
| `nt:edge:geo` | Geolocation from context |
| `nt:edge:rewrite` | Rewrite request URL (return URL object) |
| `nt:edge:redirect` | Geo-based redirect |
| `nt:edge:transform` | Transform response HTML |
| `nt:edge:cookies` | Cookie read/write (context.cookies API) |
| `nt:edge:next` | Pass through to origin (context.next) |
| `nt:edge:ab` | A/B testing with cookie bucketing |
| `nt:edge:auth` | Auth check at the edge |
| `nt:edge:headers` | Add response headers at the edge |
| `nt:edge:json` | JSON response from edge |
| `nt:edge:cache` | Fine-grained CDN cache control |
| `nt:edge:ip` | Client IP from context |
| `nt:edge:log` | Request logging middleware |
| `nt:edge:basic:auth` | Basic auth at the edge |

### Forms & Identity (`nt:form:*`) — 10 snippets

| Trigger | Description |
|---------|-------------|
| `nt:form:html` | Netlify Form (HTML with honeypot) |
| `nt:form:ajax` | AJAX form submission (include form-name) |
| `nt:form:file` | Form with file upload |
| `nt:form:success` | Form with success redirect |
| `nt:form:react` | React form for Netlify |
| `nt:form:submission` | submission-created event function |
| `nt:form:identity:widget` | Identity widget init |
| `nt:form:identity:login` | Identity login |
| `nt:form:identity:signup` | Identity signup |
| `nt:form:identity:user` | Get current Identity user |

### Blobs & Storage (`nt:blob:*`) — 8 snippets

| Trigger | Description |
|---------|-------------|
| `nt:blob:store` | Get blob store |
| `nt:blob:get` | Get blob value |
| `nt:blob:get:json` | Get blob as JSON |
| `nt:blob:set` | Set blob value |
| `nt:blob:set:json` | Set blob as JSON |
| `nt:blob:delete` | Delete blob |
| `nt:blob:list` | List blobs in store |
| `nt:blob:metadata` | Blob with metadata |

### Image CDN (`nt:img:*`) — 5 snippets

| Trigger | Description |
|---------|-------------|
| `nt:img:html` | Image CDN transform (HTML) |
| `nt:img:url` | Image CDN transform URL |
| `nt:img:responsive` | Responsive Image CDN (srcset) |
| `nt:img:remote` | Remote image via CDN |
| `nt:img:config` | Image CDN remote patterns (netlify.toml) |

### Build Plugins (`nt:plugin:*`) — 8 snippets

| Trigger | Description |
|---------|-------------|
| `nt:plugin:scaffold` | Build plugin scaffold |
| `nt:plugin:prebuild` | onPreBuild hook |
| `nt:plugin:build` | onBuild hook |
| `nt:plugin:postbuild` | onPostBuild hook |
| `nt:plugin:success` | onSuccess hook |
| `nt:plugin:error` | onError hook |
| `nt:plugin:cache` | Cache save/restore pattern |
| `nt:plugin:fail` | Fail build with message |

### Deployment & CI (`nt:deploy:*`) — 8 snippets

| Trigger | Description |
|---------|-------------|
| `nt:deploy:github` | GitHub Actions deploy workflow |
| `nt:deploy:hook` | Trigger deploy hook |
| `nt:deploy:cli` | Deploy via CLI (CI/CD) |
| `nt:deploy:monorepo` | Monorepo config with ignore |
| `nt:deploy:ignore` | Ignore builds (skip deploy) |
| `nt:deploy:env:context` | Environment per deploy context |
| `nt:deploy:notification` | deploy-succeeded event function |
| `nt:deploy:status` | Build plugin status message |

## Related Packages

- [Vercel](https://packagecontrol.io/packages/Vercel) — 140 snippets for Vercel development

## Links

- [Package Control](https://packagecontrol.io/packages/Netlify)
- [GitHub](https://github.com/renzojohnson/Netlify)
- [Issues](https://github.com/renzojohnson/Netlify/issues)
- [Author](https://renzojohnson.com)

## License

MIT License. Copyright (c) 2026 [Renzo Johnson](https://renzojohnson.com).
