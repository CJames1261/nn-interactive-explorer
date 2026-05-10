# Neural Network Regression — Interactive Explorer

An educational, single-page interactive web tool that walks data science learners through a complete neural network training cycle — one step at a time.

Built for **data analysts, statisticians, and ML beginners** who understand statistics but are new to deep learning.

## What it covers

A full forward pass → loss → backward pass → weight update cycle, broken into 16 click-through steps grouped by phase:

- **Intro** — The mountain-in-fog analogy for gradient descent
- **Data Prep** — StandardScaler explained with a real Ad Spend → Revenue example
- **Forward Propagation** — Each layer's weighted sum and ReLU activation, step by step
- **Loss** — Mean Squared Error, in plain English
- **Backward Propagation** — Backprop conceptually (for stats/data analyst audiences) plus the full gradient walk
- **Weight Update** — Gradient descent applied to all 22 parameters

## Features

- **Interactive slider** — Change the input feature (Ad Spend) and watch every value update across the network
- **Drag-and-drop neurons** — Reposition any neuron in the visualization to fix label overlaps or rearrange the layout
- **"From Forward Pass" reference cards** — On every backward step, see exactly which forward-pass values are being plugged into the current formula and which step they came from
- **Color-coded phase bar** — 16 step dots grouped by phase, each phase with its own color
- **Mountain analogy callbacks** — The fog/mountain metaphor for gradient descent threaded through the loss, gradient, and update steps
- **Plain-English variable definitions** — Every formula starts with a section defining each variable in terms a data analyst would recognize
- **Dead-neuron visualization** — When ReLU kills a neuron, its connections show as dashed red lines so values never appear "floating"

## Running locally

The project is a self-contained single HTML file. Open `index.html` in any modern browser, or serve it locally:

```bash
python -m http.server 8765
# then visit http://localhost:8765
```

If you use [Claude Code](https://claude.com/claude-code), the included `.claude/launch.json` lets you start the dev server with one command.

## Tech

- **No build step, no dependencies** — vanilla HTML, CSS, and JavaScript in a single file
- **SVG visualizations** for both the mountain analogy and the network diagram
- **Inline math** computed live in the browser — every value you see is calculated on the fly from the current slider position

## Educational design

The app is intentionally opinionated about pedagogy:

- Real-world framing (Ad Spend → Revenue) instead of abstract `sin(2πx)`
- StandardScaler instead of generic "normalization" so it matches what learners see in scikit-learn
- Variable definitions BEFORE the math, every time
- Plain-English commentary aimed at people who know regression but not deep learning
- Mountain-in-fog analogy used consistently — loss is altitude, gradient is slope, learning rate is step size

## License

MIT — see [LICENSE](LICENSE).
