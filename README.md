# Promotion Document Editor

An AI-powered editor that critiques promotion documents — the written cases managers build to recommend employees for advancement. It reviews each section against specific quality standards and returns targeted, actionable feedback.

**This editor critiques. It does not rewrite.** It points at what's weak, explains why, and hands it back to you to fix.

## Who it's for

Managers writing promotion documents, and anyone providing formal promotion feedback. Works for any company, any role, any level.

## Why it critiques instead of rewrites

Writing is thinking. The discipline of putting a promotion case into words forces the manager to confront whether the evidence actually supports the decision. When the writing is hard — when you can't articulate next-level impact or find a strong example for a key criterion — that difficulty is information. It might mean the writing needs work. It might mean the case isn't ready. Either way, an editor that rewrites the document for you produces a better document but skips the thinking. This editor makes you do both.

## What it reviews

| Section | What it checks |
|---|---|
| **Scope of Role** | Is it about the job, not the person? Is it specific to this role, not generic? |
| **Promotion Assessment** | Is it balanced, objective, criteria-focused, and specific? Does it stand on its own? |
| **Growth Areas** | Are they present, honest, specific, and accompanied by a remediation plan? |
| **Feedback** | Is it balanced (both strengths and growth areas)? Is there a clear vote? |

## Setup

### Required (works out of the box)
Drop this folder into a Claude project. That's it. The editor will critique writing quality, specificity, objectivity, balance, and structure for any promotion document or feedback draft.

### Optional (makes it better)
For company-specific critique, fill in these templates:

- **`reference/company-values.template.md`** — Add your organization's values or leadership principles. Rename to `company-values.md`. The editor will then check whether performance examples connect to your values vocabulary.
- **`reference/leveling-guide.template.md`** — Add the leveling expectations for the relevant role and level. Rename to `leveling-guide.md`. The editor will then check whether the assessment evaluates against the right criteria.

Without these files, the editor still delivers strong critique on every other dimension. Rules that require company-specific context will note they were not assessed.

## How to use it

Paste or upload your draft (full document or a single section) and tell the editor which section it is. Examples:

- "Here's my Scope of Role section. Review it."
- "This is the Promotion Assessment for an L5 to L6 Software Engineer. Critique it."
- "I'm providing promotion feedback for a colleague. Review my draft."
- "Review my full promo doc."

The editor returns:
1. **Section reviewed** — which section
2. **Overall assessment** — does it meet its purpose?
3. **Rules not assessed** — any rules skipped because optional template files weren't provided
4. **Specific findings** — each with the passage, the rule violated, why it fails, and what to fix
5. **What's working** — what to keep doing

Each finding cites a numbered rule (e.g., R5, R8, W3). These are defined in `reference/rubric.md` if you want to understand the reasoning behind a critique.

## Self-check before submitting

Want to build the muscle yourself? Use `reference/writing-quality-checklist.md` as a self-check before submitting to the editor. It walks through every quality dimension — balanced, objective, specific, criteria-focused — as plain-language questions you can evaluate your own draft against. See how many issues you can catch on your own, then let the editor find what you missed. Over time, you'll internalize the standards and need the editor less.

## Folder structure

```
promo-doc-editor/
  identity.md              — Who the editor is and what it reviews
  rules.md                 — How the editor operates (critique stance, output format, template handling)
  examples.md              — What good and bad critique looks like
  reference/
    rubric.md                     — The evaluation criteria (18 content rules + 5 writing rules)
    writing-quality-checklist.md  — Self-check and verification sweep checklist
    section-guide.md              — What each section should accomplish
    company-values.template.md    — Template: add your org's values
    leveling-guide.template.md    — Template: add your role/level expectations
```
