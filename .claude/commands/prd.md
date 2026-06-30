Generate a Product Requirements Document (PRD) for a Keepr feature.

## Context you must load first

Before writing anything, read `CLAUDE.md` in the project root so every decision aligns with:
- Keepr's brand voice (anti-corporate, anti-fine-print — never use: organize, productivity, seamless, peace of mind, declutter)
- The target customer (25–45, gadget/appliance buyers who've lost money on missed warranties)
- The tech stack (React / Next.js, GPT-4o vision, freemium SaaS)
- The circular learning feedback loop spec
- The development principle: ship the smallest thing that saves the user money or time

## What to ask the user (if not already provided in $ARGUMENTS)

If the user did not describe the feature in `$ARGUMENTS`, ask:
1. What is the feature? (one sentence)
2. What user problem does it solve?
3. Any constraints or things it must NOT do?

Then wait for their answers before writing the PRD.

## PRD format to output

Write the PRD in this exact structure:

---

# PRD: [Feature Name]

**Status:** Draft  
**Author:** Keepr Team  
**Date:** [today's date]

---

## 1. Problem

[2–3 sentences. Frame it from the user's perspective, in Keepr's brand voice. The user is being wronged by companies or by friction — name the specific pain.]

---

## 2. Goal

[One sentence. What does this feature accomplish? Start with a verb. No fluff.]

**Success looks like:** [One concrete, measurable outcome — e.g. "Users file 40% more warranty claims within 7 days of purchase."]

---

## 3. Who it's for

[One sentence describing the specific user scenario — not a persona template, a real situation.]

---

## 4. User Stories

Write 2–4 user stories in this format:
> As a [specific Keepr user], when [trigger], I want to [action] so that [outcome that saves them money or time].

Keep them concrete. Avoid vague actors like "the user" — use "someone who just bought a TV" or "someone whose warranty expires in 3 days."

---

## 5. Acceptance Criteria

A numbered checklist. Each item must be:
- Testable (pass/fail)
- Specific (no "works correctly" or "loads fast")
- Written from the user's perspective, not the engineer's

---

## 6. AI / Extraction Notes

[Only include this section if the feature touches GPT-4o extraction, the circular learning loop, or confidence scoring. Otherwise omit.]

- What fields are extracted or affected?
- What confidence threshold gates this feature?
- Does this generate correction data? If so, how is it logged?

---

## 7. Out of Scope

A short list of things this feature explicitly does NOT do. Be direct.

---

## 8. Open Questions

List any unresolved decisions that a developer or designer would hit. Flag what's blocking vs. what can be decided later.

---

## 9. Technical Notes

[Optional. Only include if there's a non-obvious constraint — a specific API behaviour, a Next.js routing consideration, a GPT-4o prompt structure, etc. Skip if nothing is surprising.]

---

## Writing rules for this PRD

- Match Keepr's brand voice throughout — even acceptance criteria should feel human
- Never use the forbidden words (organize, productivity, seamless, peace of mind, declutter)
- Every feature justification must trace back to saving the user money or time
- Do not pad sections — if a section has nothing meaningful to say, omit it
- The problem section always frames the company/system as the antagonist, not the user's forgetfulness
