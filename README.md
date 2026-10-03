# AI Fluency for K–12 Educators · Course Interactives

Pre-LMS review build. HTML interactives for the AI Fluency course developed in collaboration between Anthropic and the TFA Reinvention Lab.

Live gallery: **https://zacklinger.github.io/ai-fluency-interactives**

---

## Modules

Every module has its interactive, and the gallery ([`index.html`](index.html)) links them all.

| Module | Interactive | File |
|--------|-------------|------|
| 01 | You already have a head start | [`module-01/placement.html`](module-01/placement.html) |
| 02 | Read carefully | [`module-02/timeline.html`](module-02/timeline.html) |
| 03 | What AI carries with it | [`module-03/ethics.html`](module-03/ethics.html) |
| 04 | The 4D Framework | [`module-04/framework.html`](module-04/framework.html) |
| 05 | What's Worth Delegating | [`module-05/delegation.html`](module-05/delegation.html) |
| 06 | Conduct the Symphony | [`module-06/telephone.html`](module-06/telephone.html) |
| 07 | Designing with AI | [`module-07/designing.html`](module-07/designing.html) |
| 07 | The 4D Workflow | [`module-07/orbit.html`](module-07/orbit.html) |
| 08 | Your Fluency, Mapped | [`module-08/hand.html`](module-08/hand.html) |

[`When-Properties-Collide-standalone.html`](When-Properties-Collide-standalone.html) is an early standalone prototype, not linked from the gallery.

Building a new interactive? Read [`course-content.md`](course-content.md) for module objectives, transcripts, and the phrases to use verbatim, and [`CLAUDE.md`](CLAUDE.md) for the design system.

## Local preview

```bash
python -m http.server 8000
# then open http://localhost:8000
```

GitHub Pages builds the gallery from `main`, so every merge to `main` is a deploy.

## Notes

- No dependencies, no build step. Pure HTML/CSS/JS.
- All interactives are self-contained single files — safe to share as standalone links.
- Fonts load from Google Fonts. Requires internet connection to render correctly.
- Not for distribution outside the design team.
