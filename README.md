# Claude Portfolio UI Experiments

**One resume. Seven different websites.**

I'm Rahul Brahmbhatt, a freelance solution architect. I experimented with [Claude](https://claude.ai) to build my portfolio in many different UI styles. The content never changed (same resume, same sections, same projects). Only the design prompt did.

This repo holds all seven portfolios, a homepage that previews them, and the exact prompt behind each one, so you can ask Claude to create a beautiful website for you too.

**Live demo:** `https://barotrahulh123.github.io/claude-portfolio-ui-experiments/`

## What's inside

| Style | File | The idea |
| --- | --- | --- |
| Terminal | [`terminal.html`](terminal.html) | Dark developer workspace. Terminal-window hero, skills shown as API endpoints, experience as a CI/CD pipeline. |
| Claymorphism | [`clay.html`](clay.html) | Soft, puffy pastel shapes with double shadows, as if moulded from clay. |
| Spatial UI | [`spatial.html`](spatial.html) | visionOS-style frosted glass windows with 3D tilt, floating widgets and a side dock. |
| Liquid glass | [`liquid-glass.html`](liquid-glass.html) | Translucent glass that bends what's behind it (SVG refraction), plus a morphing cursor lens. |
| Skeuomorphic | [`skeuomorphic.html`](skeuomorphic.html) | Real-world materials: stitched leather, brass, riveted metal, legal pads and a corkboard. |
| Brutalism | [`brutalism.html`](brutalism.html) | Thick borders, hard offset shadows and loud flat colour. |
| Maximalism | [`maximalism.html`](maximalism.html) | Dense patterns, a sunburst hero, ticket-stub experience cards and tilted marquees. |

[`index.html`](index.html) is the homepage. It shows a live thumbnail of each style, opens the full page on click, and has a copy button under every prompt.

## Every portfolio has the same sections

- **Hero** with the name and role. The text rises from the bottom to the top as the page loads.
- **Capabilities**, grouped by area: APIs, client apps, cloud, data, AI/LLM, security, billing and testing.
- **Experience**, four roles from 2016 to today.
- **Projects**, five shipped products.
- **Contact**, plus a footer with education, certification and languages.

## Run it locally

There is no build step and there are no dependencies. Everything is plain HTML and CSS with a little JavaScript.

```bash
git clone https://github.com/barotrahulh123/claude-portfolio-ui-experiments.git
cd claude-portfolio-ui-experiments
python3 -m http.server 8000
```

Then open <http://localhost:8000>. Double-clicking `index.html` also works. Keep all the files in the same folder so the previews and links resolve.

## Make your own

1. Open the homepage and pick a style.
2. Copy its prompt with the copy icon. All seven are also in [`PROMPTS.md`](PROMPTS.md).
3. Paste it into Claude and replace `[PASTE YOUR RESUME HERE]` with your own details.

To invent a new style, swap the style paragraph in any prompt for your own idea (vaporwave, Swiss print, retro arcade, paper craft) and keep the rest.

## Reuse a page

Each page is a single self-contained HTML file. To reuse one:

1. Copy the file you like.
2. Replace the resume content (name, roles, projects, links). The text is in the HTML body, with no framework to untangle.
3. Change colours in the `:root` block at the top of the `<style>` tag.

## Deploy

**GitHub Pages**

1. Open **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, then select `main` and `/ (root)`.
3. The site goes live at `https://barotrahulh123.github.io/claude-portfolio-ui-experiments/`.

**Netlify or Vercel:** import the repo and deploy it as a static site with no build command. The publish directory is the repo root.

## Notes

- Fonts load from Google Fonts, so previews need an internet connection to look exactly right.
- The liquid glass refraction works in Chromium browsers (Chrome, Edge). Other browsers show a plain frosted look instead.
- All animations respect `prefers-reduced-motion`.
- Every page is responsive down to phone width and has visible keyboard focus.

## Author

**Rahul Brahmbhatt**, Freelancer and Solution Architect, Ahmedabad, India.
Node.js · React · AWS serverless · AI/LLM integration

- GitHub: [github.com/barotrahulh123](https://github.com/barotrahulh123)
- Portfolio: [rahulweb.netlify.app](https://rahulweb.netlify.app)

## License

MIT. See [LICENSE](LICENSE). The resume content (name, work history, contact details) is mine, so please replace it with your own if you reuse a page.
