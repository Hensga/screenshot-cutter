# screenshot-cutter

A browser-based tool for preparing full-page screenshots for documentation and forum posts. Runs entirely client-side — no server, no uploads, no dependencies.

## What it does

- **Center-crop** the screenshot to a configurable width (default 900px), removing empty margins
- **Cut out sections** from the middle of long screenshots and stitch the remaining parts together
- **Trim header and footer** with configurable pixel values
- **Draw red rectangles** to highlight areas of interest
- **Overlay torn-paper edges** ("Fotokanten") at cut seams for a visual indicator that content was removed
- **Export** the result as a PNG

## Usage

Open `index.html` in a browser. Load a screenshot via drag & drop, file picker, or Ctrl+V paste.

### Modes

| Key | Mode | Description |
|-----|------|-------------|
| `C` | Cut | Click to place horizontal cut lines. Lines are paired — every two lines define a region to remove. Drag to reposition, double-click to delete. |
| `R` | Rect | Draw red annotation rectangles. Double-click to delete. |
| `V` | Pan | Scroll/drag the canvas for long screenshots. |

### Toolbar

- **Header / Footer** — Pixels to trim from top and bottom (defaults: 160 / 10)
- **Breite / Offset X** — Horizontal crop width and offset from center
- **Vorschau** (`P`) — Toggle preview of the final export
- **Export PNG** (`E`) — Download the result

### Fotokanten

Upload PNG images with transparency for torn-paper edges. Three slots:

- **Oben** — Overlaid at the top edge (when header is trimmed)
- **Trenner** — Overlaid at each cut seam, centered on the join
- **Unten** — Overlaid at the bottom edge (when footer is trimmed)

Each slot has a toggle to enable/disable. The images are drawn as overlays — transparent areas show the content underneath.

## License

MIT
