# Cyber Threat Exposure Map

[![Pages](https://github.com/SDCofA/cyber-exposure-map/actions/workflows/pipeline.yml/badge.svg)](https://github.com/SDCofA/cyber-exposure-map/actions/workflows/pipeline.yml)

Public vulnerability and exposure signals centered on CISA KEV data.

**Live dashboard:** https://sdcofa.github.io/cyber-exposure-map/

## Run locally

```bash
python -m pip install -r requirements.txt
python pipeline/cyber_exposure_map_pipeline.py
python -m http.server 8000
```

Open `http://localhost:8000`. Direct `file://` access cannot fetch `data/output.json` in modern browsers.

## Automation

GitHub Actions refreshes public data every six hours and deploys the static dashboard to GitHub Pages. AI briefs are optional: configure `OPENROUTER_API_KEY` as a repository Actions secret. Without it, core collection and dashboard deployment remain available.

## Data notice

Source availability varies. The dashboard identifies its generation time and operating mode in `data/output.json`. Treat indicators as decision-support signals, not verified ground truth.

## Brand

Published by SDCofA, the endorsed analytical unit of Monarch Castle Technologies. See [BRAND.md](BRAND.md) for approved asset use.
