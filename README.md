# OmniMMI Viewer

Case-by-case web viewer for the [OmniMMI](https://github.com/OmniMMI/OmniMMI) benchmark — ships with a 12-sample representative subset (2 per task).

**Live site:** https://jxb1st.github.io/omnimmi-viewer/

## Tasks

- **Action Prediction (AP)** — predict the next action from a short video clip
- **Dynamic State Grounding (SG)** — multi-turn QA about state changes
- **Multiturn Dependency Reasoning (MD)** — multi-turn QA where later turns depend on earlier ones
- **Proactive Alerting (PA)** — decide when the model should proactively alert
- **Proactive Turntaking (PT)** — decide when the model should take the turn
- **Speaker Identification (SI)** — identify who is speaking

## Contents

- `index.html` — single-file viewer
- `omnimmi/<task>.json` — filtered to 2 samples per task
- `omnimmi/videos/` + `omnimmi/clips/` — re-encoded 480p mp4s (h264 CRF 28 / AAC 64k / faststart)
- `file_durations.json` — duration lookup
- `selection_report.md` — which samples were picked

## Local preview

```bash
cd omnimmi-viewer
python3 -m http.server 8000
# open http://localhost:8000/
```

## Full benchmark

This viewer is a browseable sampler. For the full dataset and evaluation code, see the official [OmniMMI repo](https://github.com/OmniMMI/OmniMMI).
