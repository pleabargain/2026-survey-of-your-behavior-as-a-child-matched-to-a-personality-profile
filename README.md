# Childhood Role Profile

Standalone web quiz that identifies which childhood family role still shapes how you show up in relationships and work. Pure HTML, CSS, and vanilla JavaScript—no build step, no dependencies, suitable for GitHub Pages.

Open [`index.html`](index.html) in a browser to start.

## What you get

After answering, the quiz reports a **primary role** plus:

- Short profile summary
- Old story vs healthier reframe
- Strengths and growth edges
- **Ten challenging growth-edge questions** (toggle on the results screen)
- **Normalized role shares** (each role’s count ÷ quiz length, summing to 100%)

Chance baseline with six roles is about **16.7%**. Shares are comparable across quiz lengths.

## Roles

| Profile | Pattern in brief |
| --- | --- |
| The Achiever | Worth tied to performance and getting it right |
| The Easygoing One | Safety through flexibility and low needs |
| The Challenged One | Identity and attention organized around struggle |
| The Peacemaker | Responsibility for harmony and mediating conflict |
| The Young Caregiver | Caregiving and being needed as the path to belonging |
| The Independent One | Autonomy, candor, and standing apart |

## Quiz lengths

Choose at the start screen:

- **12-question quiz** — quick profile (2 × 6 roles)
- **60-question quiz** — full assessment (10 × 6 roles)

Lengths are multiples of six so scores normalize cleanly as proportions. The short form is a curated subset of the full item bank.

## How to run locally

1. Open `index.html` in any modern browser (double-click or drag into a window).
2. Select **12-question** or **60-question**.
3. Answer each item; use Back/Next as needed.
4. View your primary role and normalized distribution.
5. **Retake** keeps the same length.

No install, server, or internet connection required for the quiz itself.

## GitHub Pages

1. Push this folder to a GitHub repository (keep `index.html` at the site root, or set Pages to the folder that contains it).
2. Enable **Settings → Pages → Deploy from branch**, source `main` / `/ (root)` (or `/docs` if you move files there).
3. Visit `https://<user>.github.io/<repo>/`.

## Built-in tests (on-page)

From the start screen:

- **Run scoring & similarity tests** — full pass/fail report in the page (deck sizes, unanimous roles, tie-break, **12↔60 similarity**, Monte Carlo winner agreement).
- **Run automated random test** — random answers for the current length, with validation and an HTML report.

Or open:

- `index.html?test=1` — auto-run scoring & similarity tests  
- `index.html?random=10` — auto-run 10 random trials  

**Run again** on the report screen repeats the same report type.

### Console helpers (optional)

```js
ChildhoodRoleQuiz.startQuiz(12);          // or 60
ChildhoodRoleQuiz.runTests();             // HTML report + return value
ChildhoodRoleQuiz.runRandomTest({ runs: 25, length: 12 });
ChildhoodRoleQuiz.score([0,1,2,...], deck); // scores, normalized, baseline
ChildhoodRoleQuiz.lengths;                // [12, 60]
ChildhoodRoleQuiz.roles;                  // display names
```

Similarity checks confirm that proportion-matched answer patterns produce the same winner and nearly identical normalized shares on 12- and 60-question forms (within rounding tolerance).

## Privacy

Answers are scored entirely in the browser. Nothing is uploaded; there is no account or analytics.

## Project files

| File | Purpose |
| --- | --- |
| `index.html` | Full app: UI, question bank, scoring, tests |
| `README.md` | This document |

## Disclaimer

This is a reflective self-insight tool, not a clinical diagnosis or substitute for professional care.

---

Last updated: 2026-09-09
