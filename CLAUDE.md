# AI Fluency for K-12 Educators - Course Interactives

Pre-LMS review build. HTML interactives for the AI Fluency course (Anthropic x TFA Reinvention Lab).

Live gallery: https://zacklinger.github.io/ai-fluency-interactives

## Course content

Read `course-content.md` for the full course context before building any interactive:
- All 8 module learning objectives
- Video transcripts and key quotes
- The Ms. Okafor scenario (used in Modules 5 & 6)
- Exercise formats that interactives are meant to spark
- Key phrases to use verbatim in interactive copy

Also add the source PDF to the repo root if you have it locally:
`AI_Fluency_for_K-12_Educators_Course__Content___Project_Tracker.pdf`

## Local dev

```bash
python -m http.server 8000
```

No build step. No dependencies. Pure HTML/CSS/JS.

## Design system

All interactives use the Anthropic light theme:

- --bg: #faf9f5 (warm off-white)
- --surface: #f0eee6 (slightly darker warm white)
- --dark: #141413 (near-black warm text)
- --muted: rgba(20,20,19,0.42)
- --border: rgba(20,20,19,0.1) at 0.5px
- --coral: #d97757 (primary accent)
- --blue: #6a9bcc (in review status)
- --green: #3d6b4f
- --amber: #9a6e2a

Fonts: DM Sans (UI/headings, 400/500/600), Source Serif 4 (body/insight, 400)
Rules: No italics. No bold except labels. Borders always 0.5px. No box shadows except active buttons.

## Module status

| # | Title | Interactive | Status |
|---|-------|-------------|--------|
| 01 | Intro to AI Fluency | Constellation sandbox | Final |
| 02 | AI Capabilities & Limits | Hallucination reader | In review |
| 03 | Pedagogy, AI & You | - | Pending |
| 04 | The 4D Framework | - | Pending |
| 05 | Ethical Focus: Delegation & Diligence | - | Pending |
| 06 | Quality Focus: Description & Discernment | Symphony particles | In review |
| 07 | Tying It All Together | - | Pending |
| 08 | Closure & Enrichment | - | Pending |

## Known issues

### module-01/placement.html
- Panel bounce: .pleft needs min-height:175px (tallest node measured). FIXED in current file.
- Badge clip: .status-badge must be on .stage outside .card (not inside overflow:hidden card). FIXED.

### module-02/timeline.html
- Text corruption: JS strings had smart quotes/em dashes mangled by btoa encoding chain. FIXED - pure ASCII now.

### module-06/telephone.html
- Lightbulb geometry: dome arc PI->2*PI is correct (upper semicircle). Neck horizontal ridges only - no vertical edges (cause drip streams).
- 5th button illumination: gradual glow via glowCurrent lerp at rate 0.018/frame.

## Critical encoding rule

When building HTML locally and pushing via GitHub API:
- Never use Unicode in JS string literals that go through btoa()
- Use -- instead of em dash, straight quotes, &mdash; only in HTML portion
- Working locally = no encoding chain = use normal characters freely

## 4D Framework

- Description: telling AI what you need (product/process/performance)
- Discernment: evaluating AI output critically
- Delegation: deciding what to hand off vs keep
- Diligence: professional responsibility (FERPA, accuracy, transparency)

Inner loop: Description <-> Discernment (daily interactions)
Outer loop: Delegation <-> Diligence (professional responsibility)

## Interactive design principles

From whiteboard (https://ai-fluency-course-whiteboard.vercel.app/):
1. Empowerment / Action - teachers leave feeling capable
2. Value + Relevance - connects to daily work
3. Trust + Safety - no gotcha moments
4. Augmentation - AI is a tool, teacher stays in control
5. Engaging / Not Boring - novel, quick-hitting, surprising
6. Baseline Knowledge - meets teachers where they are

Interactive = spark before the exercise. Under 2 min. No score. No wrong answer.
