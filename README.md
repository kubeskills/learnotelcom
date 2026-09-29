# learnotelcom

[![Netlify Status](https://api.netlify.com/api/v1/badges/fb40bc90-dc4d-4af3-8fea-4a917fafa981/deploy-status)](https://app.netlify.com/projects/learnotel/deploys)

[learnOTel.com](https://learnOTel.com) | Learn OpenTelemetry

A simple static site that points visitors to resources for learning [OpenTelemetry](https://opentelemetry.io/).

## Resources featured

- [OpenTelemetry Astronomy Shop Demo](https://github.com/open-telemetry/opentelemetry-demo)
- [Training](https://opentelemetry.io/training/)
- [Awesome OpenTelemetry](https://github.com/magsther/awesome-opentelemetry)
- [OpenTelemetry Collector](https://github.com/open-telemetry/opentelemetry-collector)
- [OpenTelemetry Documentation](https://opentelemetry.io/docs/)
- [Mastering OpenTelemetry and Observability](https://www.wiley.com/en-us/shop/general-introductory-computer-science/mastering-opentelemetry-and-observability-enhancing-application-and-infrastructure-performance-and-avoiding-outages-p-9781394253135)

## Structure

| File | Purpose |
| --- | --- |
| `index.html` | The homepage (self-contained HTML and CSS, no build step) |
| `opentelemetry-horizontal-color.png` | OpenTelemetry logo used on the homepage |
| `kubeskills-horizontal-logo.png` | KubeSkills logo used in the footer, linking to kubeskills.com |
| `_redirects` | Netlify redirect rules (e.g. `/demo-arch` to the OpenTelemetry demo architecture docs) |
| `CLAUDE.md` | Guidance for Claude Code when working in this repo |
| `.claude/settings.json` | Claude Code project settings (deny rules for `.env*` and `.netlify/`) |
| `.gitignore` | Files git should ignore (OS/editor files, `.netlify/`, `.env*`) |

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deployment

Deployed with Netlify as a static site: no build command, publish directory is the repo root.

## Trademarks

The OpenTelemetry name and logo are trademarks of The Linux Foundation / CNCF. This is an independent learning site and is not affiliated with or endorsed by the OpenTelemetry project.
