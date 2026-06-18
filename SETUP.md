# Profile setup

## 1. Copy the generated files

The profile repository should contain:

```text
.
├── .github/workflows/metrics.yml
├── assets/
│   ├── cyberpunk-workspace.png
│   ├── pixel-accent.gif
│   └── pixel-coder.gif
├── README.md
└── SETUP.md
```

## 2. Add the Metrics token

Create a GitHub Personal Access Token for the Metrics workflow.

For public-only metrics, no additional repository scope is necessary. To count private contributions, grant the token access to the private repositories you want included. The workflow intentionally keeps the recent-activity panel public-only so private repository names are not displayed.

Add it to the `matejapp/matejapp` repository:

1. Open **Settings → Secrets and variables → Actions**.
2. Choose **New repository secret**.
3. Name it `METRICS_TOKEN`.
4. Paste the token and save it.

Never commit the token to the repository.

## 3. Generate the SVG panels

Open **Actions → Profile metrics → Run workflow**.

The workflow creates and commits:

- `metrics-calendar.svg`
- `metrics-languages.svg`
- `metrics-activity.svg`

Until the workflow runs successfully, those three images will appear as missing in the profile preview.

## 4. Review before publishing

Check the README on both GitHub light and dark themes. If the metrics panels expose a language or activity you do not want highlighted, adjust the corresponding plugin options in `.github/workflows/metrics.yml`.

## Asset credits

- `cyberpunk-workspace.png` is an original generated asset created for this profile.
- The two animated accents were selected from [Anmol-Baranwal/Cool-GIFs-For-GitHub](https://github.com/Anmol-Baranwal/Cool-GIFs-For-GitHub).
- Metrics are generated with [lowlighter/metrics](https://github.com/lowlighter/metrics).
