# Quiz Scene Builder

A drag-and-drop tool for building the road scenes, junctions, vehicles and road signs used in a Zimbabwe driving-school quiz app. It is a single static page (`index.html`) with no dependencies and no build step, so it works offline and on GitHub Pages.

## Use it

- Open `index.html` in any modern browser, or visit the GitHub Pages link once deployed.
- Drag items from the library onto the canvas (or click to add at the centre).
- Export each finished scene as **PNG** (2x resolution) or **SVG**.
- **Save project** downloads a `.json` file so you can reopen and edit a scene later. Scenes also autosave in the browser.

## Controls

| Action | How |
| --- | --- |
| Select several items | Ctrl/Shift/Cmd + click, or drag a box on empty space |
| Select all / clear | Ctrl+A / Esc |
| Move | Drag, or arrow keys (Shift = 10 units) |
| Copy / paste / duplicate | Ctrl+C / Ctrl+V / Ctrl+D |
| Rotate | R (Shift+R reverses), or the side panel |
| Delete | Delete or Backspace |
| Undo | Ctrl+Z |
| Zoom | Mouse wheel |
| Pan | Hold the right mouse button and drag (Space+drag or middle-drag also work) |
| Editable arrows | Pick one from the Arrows group. Drag the white dots to stretch or bend it, drag a hollow dot to add a bend, double-click a dot to remove it. Colour, thickness and smooth bends are in the side panel |
| Text labels | Extras, Text: change the text, colour and size in the side panel |
| Match road sizes | "Match road sizes" button; new roads also copy the size of existing ones |

## Deploy to GitHub Pages

1. Create a new repository on GitHub and push this folder to the `main` branch.
2. In the repository go to **Settings, Pages**, and set **Source** to **GitHub Actions**.
3. The included workflow (`.github/workflows/pages.yml`) publishes the site on every push to `main`. The link appears in the **Actions** tab and under Settings, Pages.

Prefer no workflow? Delete `.github/` and set **Source** to **Deploy from a branch** (`main`, `/ (root)`).

```bash
git init
git add .
git commit -m "Quiz scene builder"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

## Notes on the signs

Road rules follow Zimbabwe (driving on the left, white road markings). Signs are simplified redrawings based on the Zimbabwe Highway Code and the official road traffic signs chart (sign codes such as R103 or W308 are shown in the library). They are not exact copies, so check each one against the official source before using it in a question. The Highway Code is published by the Traffic Safety Council of Zimbabwe.

## Files

- `index.html` - the whole app (HTML, CSS and JavaScript)
- `.nojekyll` - tells GitHub Pages to serve the files as they are
- `.github/workflows/pages.yml` - optional automatic deployment
