# CLAUDE.md - cnvas.github.io

GitHub Pages site that hosts program schedule images for VRTV. The timetable image is referenced from inside VRChat.

## Common Commands

```bash
# No build step — images are pushed directly

# Typical update workflow
git checkout -b feature/timetable-YYYYMMDD
# Replace docs/vrtv/timetable.png with updated image
git add docs/vrtv/timetable.png
git commit -m "Timetable update for YYYY-MM-DD"
git push -u origin feature/timetable-YYYYMMDD
gh pr create
```

## Architecture

### Directory Structure

```
docs/                   # GitHub Pages public directory
└── vrtv/
    └── timetable.png   # Weekly program schedule image (1450x2048 PNG)
```

### Key Conventions

- **Deployment**: Automatic via GitHub Pages from `docs/` directory on `main` branch
- **Update frequency**: Weekly (every ~7 days)
- **Branch naming**: `feature/timetable-YYYYMMDD`
- **Workflow**: Always merged via PR, never direct commits to `main`
- **Content URL**: `https://cnvas.github.io/vrtv/timetable.png`
