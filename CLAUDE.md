# YSMS - Your Side My Side Research

## Project Overview
An art project disguised as a fictional research institute website. "Your Side My Side Research" presents itself as an "Institute for Emotional Response Research" conducting an "Audiovisual Stimulus Response Study."

## Architecture
- **Single-page static site** — one `index.html` file, no build step, no dependencies
- **Hosting**: Netlify (auto-deploys from `main` branch) + GitHub Pages
- **Backend**: Google Apps Script receives emotion + email submissions via GET request to a Google Sheet

## Key Components

### Frontend (`index.html`)
- **Header**: ASCII-art styled logo with institute branding
- **Visitor counter**: Randomized fake participant count (500–1000) that increments on interaction
- **Video player**: Loads video from `yoursidemyside.com/videos/YSMS-research-artefact-1.mp4`
- **Questionnaire**: Three emotion buttons — Euphoric, Dismal, Blank
- **Email collection form**: Appears after emotion selection, optional
- **Aggregate data table**: Shows fictional response distribution, revealed after voting

### Data Flow
1. User selects an emotion → in-memory counter updates, UI reveals email form + data table
2. User optionally submits email → GET request sent to Google Apps Script URL
3. Google Apps Script logs emotion + email to a Google Sheet

## Styling
- Monochrome, editorial aesthetic (black, white, grays)
- Courier New monospace for data/UI elements
- Georgia serif for headings
- Responsive — mobile layout switches buttons/inputs to stacked column

## Development
No build tools required. Just edit `index.html` and push.

```bash
# Deploy
git add -A && git commit -m "description" && git push
```

## Important Notes
- The Google Apps Script URL in the code is a live endpoint — do not share publicly or abuse
- Video is hosted externally at yoursidemyside.com
- The visitor count and aggregate data are fictional — they randomize on each page load
- Copyright line reads "© 1979" as part of the art direction
