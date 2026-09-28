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

## Structure

| File | Purpose |
| --- | --- |
| `index.html` | The homepage (self-contained HTML and CSS, no build step) |
| `opentelemetry-horizontal-color.png` | OpenTelemetry logo used on the homepage |

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deployment

Deployed with Netlify as a static site: no build command, publish directory is the repo root.

## Trademarks

The OpenTelemetry name and logo are trademarks of The Linux Foundation / CNCF. This is an independent learning site and is not affiliated with or endorsed by the OpenTelemetry project.
