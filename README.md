# Promotion Document Editor

You've spent months developing someone for the next level. Now the case has to survive on paper — read by reviewers who don't know your employee, don't share your context, and won't take your word for it. The document is the decision surface, and most promotion docs fail not because the employee isn't ready, but because the writing doesn't prove it.

The same mistakes show up everywhere: opinions where evidence should be, current-level performance dressed up as next-level readiness, vague impact claims with no data, growth areas missing entirely, and jargon that shuts out anyone outside the team.

This editor catches those mistakes before your reviewers do. Paste your draft, get back a critique that points at the exact passages that don't work, cites the specific standard they violate, and tells you what to fix. It won't rewrite anything for you — that's by design.

Works for managers writing the promotion document and for anyone asked to provide promotion feedback. Works for any company, any role, any level. Plug in your organization's values and leveling guide for company-specific critique, or use it out of the box for writing quality alone.

## Where this comes from

This tool is built on years of helping managers write strong promotion cases. The rubric, the section guide, the examples of what works and what doesn't — all of it comes from conducting focus groups with managers, collecting hundreds of real promotion documents, and distilling the patterns that separated cases that landed from cases that didn't. This editor is that expertise, packaged so an AI can apply it to your draft in real time.

## Why it critiques instead of rewrites

Writing is thinking. The discipline of putting a promotion case into words forces you to confront whether the evidence actually supports the decision. When the writing is hard — when you can't articulate next-level impact or find a strong example for a key criterion — that difficulty is information. It might mean the writing needs work. It might mean the case isn't ready. Either way, an editor that rewrites the document for you produces a better document but skips the thinking. This editor makes you do both.

## What it reviews

| Section | What it checks |
|---|---|
| **Scope of Role** | Is it about the job, not the person? Is it specific to this role, not generic? |
| **Promotion Assessment** | Is it balanced, objective, criteria-focused, and specific? Does it stand on its own? |
| **Growth Areas** | Are they present, honest, specific, and accompanied by a remediation plan? |
| **Feedback** | Is it balanced (both strengths and growth areas)? Is there a clear vote? |

Your doc doesn't need to use these exact section names. The editor maps your content to the relevant criteria regardless of how your organization structures its promotion documents.

## Setup

### Works out of the box
Drop this folder into a Claude project (or point Claude Code at this folder). That's it. The editor will critique writing quality, specificity, objectivity, balance, and structure for any promotion document or feedback draft.

### Customize for your company
Two template files in `customize/` let you plug in your organization's specific context:

- **`customize/company-values.md`** — Your organization's values or leadership principles. The editor checks whether performance examples connect to your values vocabulary.
- **`customize/leveling-guide.md`** — The leveling expectations for the relevant role and level. The editor checks whether the assessment evaluates against the right criteria.

Without these files, the editor still delivers strong critique on every other dimension. Rules that require company-specific context will note they were not assessed. Fill them in and the editor calibrates to your org automatically.

## How to use it

Paste or upload your draft (full document or a single section) and tell the editor which section it is:

- "Here's my Scope of Role section. Review it."
- "This is the Promotion Assessment for an L5 to L6 Software Engineer. Critique it."
- "I'm providing promotion feedback for a colleague. Review my draft."
- "Review my full promo doc."

The editor returns structured critique: which sections were reviewed, an overall assessment, specific findings (each with the passage, the rule violated, why it fails, and what to fix), what's working, and a priority order for revisions. Every finding cites a numbered rule from the rubric — R5, R8, W3 — so you can trace the reasoning. See the [landing page example section](index.html#example) for a full input/output pair — a sample draft and the editor's actual critique.

## Self-check

Want to build the muscle yourself? Use `reference/writing-quality-checklist.md` before submitting to the editor. It walks through every quality dimension as plain-language questions you can evaluate your own draft against. Over time, you'll internalize the standards and need the editor less.

## Structure

```
promo-doc-editor/
  CLAUDE.md          Entry point — where everything lives and how to start
  CONTEXT.md         Run contract — step-by-step sequence for a review session
  identity.md        Who the editor is and what it reviews
  rules.md           How the editor operates (critique stance, output format)
  examples.md        What good and bad critique looks like
  reference/
    CONTEXT.md             What this folder is and when it's read
    rubric.md              The evaluation criteria (18 content rules + 5 writing rules)
    section-guide.md       What each section should accomplish
    writing-quality-checklist.md   Self-check and verification sweep
  customize/
    CONTEXT.md             What this folder is and how to use it
    company-values.md      Template: add your org's values
    leveling-guide.md      Template: add your role/level expectations
  reviews/
    CONTEXT.md             What this folder is and naming conventions
    _template.md           Frontmatter and structure for saved critiques
```
