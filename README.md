# Rajin Uddin, Portfolio

My personal site, built around a 3D retro computer you can type into.

**Live:** [rajin-portfolio.vercel.app](https://rajin-portfolio.vercel.app)

## What it does

- **3D scene:** A Three.js model of a vintage computer, with a custom GLSL shader that gives its screen CRT scanlines and barrel distortion.
- **Working terminal:** The screen runs a small shell over a virtual file system. Try `help`, `ls`, `cat`, `whoami`, `skills`, `open github` or `resume`.
- **Standard sections:** Projects, about and contact are regular HTML beside the scene, so recruiters can skip the terminal.
- **Fallbacks:** Devices without WebGL get a plain mobile layout, and the camera respects `prefers-reduced-motion`.

## Tech

| Area | Choice |
|---|---|
| Language | TypeScript |
| Build | Vite |
| 3D | Three.js, GLSL shaders (`vite-plugin-glsl`) |
| Hosting | Vercel |

The site sets strict security headers in `vercel.json`, including a Content Security Policy that only allows scripts and styles from its own origin.

## Run it locally

Requires Node.js 18 or newer.

```bash
git clone https://github.com/razinn70/Rajin-Portfolio.git
cd Rajin-Portfolio
npm install
npm run dev
```

`npm run build` type checks and builds to `dist/`. `npm run preview` serves that build.

## Project layout

```
src/
  scene/      Three.js scene, camera and resize handling
  computer/   3D computer model, screen renderer, CRT shader
  shaders/    GLSL vertex and fragment shaders
  terminal/   Shell, commands, history and virtual file system
  ui/         Loading screen, navigation, project cards, about, contact
  data/       Projects, skills, experience and personal details
  styles/     CSS by section
public/
  resume/     Resume PDF served by the resume command
```

To update content, edit the files in `src/data/`. The terminal and the page sections both read from them.

## Contact

[muddinal@uoguelph.ca](mailto:muddinal@uoguelph.ca) · [LinkedIn](https://linkedin.com/in/rajinu) · [GitHub](https://github.com/razinn70)
