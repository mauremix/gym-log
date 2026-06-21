# Gym Log Handoff

## Purpose

Continue the domain-grilling session for a mobile-first training log application. The user currently logs workouts in iPhone Notes and wants a better UX plus structured queries to see progress over time.

## Current Artifacts

- Workspace: `/Users/maurolopez/Code/gym-log`
- Initial product notes: `/Users/maurolopez/Code/gym-log/README.md`
- Domain glossary created during this session: `/Users/maurolopez/Code/gym-log/CONTEXT.md`
- Git state at handoff: `CONTEXT.md` is untracked and contains all resolved domain terms so far.

Do not duplicate the glossary contents in the next chat. Read `CONTEXT.md` first and continue updating it inline as terms are resolved.

## Conversation Summary

The session used `$grill-with-docs` to turn the README into a sharper domain model. The major resolved decisions are captured in `CONTEXT.md`, including:

- Canonical hierarchy is `Block -> Mesocycle -> Microcycle -> Session`.
- `Cycle`, `Week`, and `Session Day` are avoided as domain terms.
- Sessions are actual performed training days, not planned workouts.
- Sessions are one per calendar date and belong to the active Microcycle for that date.
- Blocks, Mesocycles, and Microcycles are Monday-Sunday aligned.
- Microcycles are fixed Monday-Sunday weeks and are not date-edited individually.
- Mesocycles and Blocks vary in whole child periods, with numbered labels only.
- Components are fixed to `Upper`, `Lower`, `Core`, and `Rehab`; each appears at most once per Session.
- Exercises are reusable movements and each Exercise belongs to exactly one Component.
- Logs are performed instances of one Exercise at one required Weight in a Session.
- Within the same Session, `Exercise + Weight` identifies one Log; more Sets at the same Weight merge into that Log.
- Weight is required, stored in kilograms, and `0kg` represents unweighted exercise.
- Sets record reps and optional RIR.
- The note-like Log Protocol is a first-class input method.

## Where To Resume

The last answered question was:

> Should the app preserve your shorthand text protocol as a first-class input method?

The user answered yes, and `Log Protocol` was added to `CONTEXT.md`.

The next unanswered question was:

> Should the Log Protocol be the primary way to add Logs, or one option alongside a structured form?

Recommended answer from prior session:

> Primary input should be the shorthand text protocol. The app can parse it, preview structured output, and let the user correct mistakes. A structured form can exist later, but it should not be the main flow at first.

Ask this question first in the next session unless the user redirects.

## Suggested Skills

- `grill-with-docs`: Continue the one-question-at-a-time interview and update `CONTEXT.md` inline as terms are resolved.
- `to-prd`: Use later if the user asks to turn the clarified domain and UX decisions into a PRD.
- `to-issues`: Use after a PRD or plan exists and the user wants implementation tickets.
- `prototype`: Use if the user wants to explore mobile-first input flows before building the real app.
- `tdd`: Use when implementation starts and the user wants test-first development.

## Notes For Next Agent

- Keep using one question at a time, with a recommended answer.
- If the user uses `Mycrocycle` or `mycrocycle`, gently normalize to canonical `Microcycle`.
- Continue treating `CONTEXT.md` as a glossary only, not a product spec.
- No ADR has been created yet. Only propose one if a future decision is hard to reverse, surprising without context, and a real trade-off.
- No sensitive data appeared in the conversation.
