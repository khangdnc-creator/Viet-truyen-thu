---
name: story-from-draft
description: Develop a user's story draft into polished fiction while preserving confirmed canon. Use when the user supplies notes, outlines, summaries, rough dialogue, partial scenes, chapter drafts, or worldbuilding and asks to write, expand, revise, or continue a story.
---

# Story From Draft — v2.0

## Mission

Turn the author's draft into a complete, compelling chapter. Improve the execution rather than merely polishing the existing wording. Work across genres while preserving the author's confirmed canon, intended events, character motives, and outcomes.

**Default principle: preserve story meaning, not draft phrasing.** A rough draft is usually a specification for what happens, not a script whose sentences must be copied. This is especially important for dialogue and action scenes.

## Priority order

1. Explicit instructions in the current user message.
2. Author-confirmed canon and project files actually supplied or accessible.
3. Essential events, intended outcomes, and character intentions in the current draft.
4. Established world rules and genre requirements.
5. Assistant-created inference and invention.

Never let genre convention override canon. Do not claim to have read inaccessible files or possess persistent memory that is not available.

## Cultural and institutional modeling — mandatory for culturally grounded fiction

Before drafting, identify the setting's actual social machinery rather than applying generic “Eastern” or “Western” flavor. Route to `references/cultural-institutions.md`, `references/eastern-court-and-xianxia.md`, `references/western-feudal-polities.md`, and `references/gender-demographics.md` as relevant. Treat these as frameworks for asking the right questions, not rigid templates.

Do not assign each family, nation, sect, or culture one defining trait. Reputation is not essence: a house known for cavalry may contain rival branches, financiers, clerics, administrators, cowards, reformers, and competent infantry officers. A court, clan, sect, or kingdom is an arena of competing interests, not a single personality.

Do not add women or any other demographic category merely to make a cast look balanced. Equally, do not remove women by applying a blanket male-only rule. Populate scenes from the setting's institutions, occupation, class, period, location, plot needs, and the author's established cast. Make demographic patterns plausible for the specific scene and society, and give every character a causal reason to be present.

## Core workflow

### 1. Read and classify the draft

Identify the intended chapter outcome, required events, viewpoint, tone, character goals, setting constraints, and continuity risks. Distinguish:
- **CANON:** explicitly established or author-approved.
- **INFERENCE:** strongly implied but not confirmed.
- **INVENTION:** new material introduced to make the chapter work.
- **OPEN:** a decision that remains unresolved.

See `references/canon-and-continuity.md`.

### 2. Separate content from wording

Treat each draft element according to its function:

- **Required fact or event:** preserve.
- **Required outcome:** preserve unless the author requests a change.
- **Dialogue written as a rough note or ordinary draft line:** preserve its meaning, purpose, and necessary information, but normally rewrite the wording.
- **Exact quotation, signature line, oath, catchphrase, poem, legal wording, or line explicitly marked “keep verbatim”:** preserve exactly.
- **Distinctive phrasing that appears intentionally authored:** retain where it contributes value; do not flatten it automatically.

Do not assume every line of dialogue is sacred merely because it appears in quotation marks. Unless the user says otherwise, quoted dialogue in a rough draft is source material for adaptation, not a verbatim constraint.

### 3. Plan the chapter internally

Determine what changes from beginning to end, the causal sequence, scene order, dramatic pressure, information flow, and the ending turn. For dialogue-heavy, combat-heavy, or culturally institution-driven scenes, read the dedicated reference files before drafting:
- `references/dialogue-rewriting.md`
- `references/combat-choreography.md`

Do not expose a long plan or private reasoning. Provide only the chapter and concise material notes unless the user asks for a summary of the approach.

### 4. Draft with controlled autonomy

Preserve the draft's core events and intended result. Develop scene transitions, dialogue, characterization, setting, and action as needed. Add detail only when it improves clarity, causality, character, atmosphere, stakes, or pacing.

When the draft is skeletal, do not merely add adjectives around it. Build the missing dramatic mechanics: who wants what, what blocks them, what they try, how others respond, and what changes as a result.

### 5. Rewrite dialogue by default

Unless explicitly instructed to preserve dialogue verbatim:
- retain the **communicative payload** (facts, intent, threat, promise, decision, emotional turn);
- rebuild the line to fit the speaker, relationship, power dynamic, context, subtext, and rhythm;
- allow natural interruption, evasion, silence, disagreement, and indirect answers;
- avoid copying the draft's syntax or sentence structure when the task is to expand or rewrite;
- do not simply replace a few words with synonyms and call it a rewrite;
- do not invent a new revelation, promise, threat, or decision merely to make the exchange more dramatic.

Use `references/dialogue-rewriting.md`.

### 6. Construct combat as a causal sequence

Combat must be legible in space and plausible in time. Before and during drafting, track:
- objective and immediate stakes;
- participants, equipment, terrain, visibility, distance, and obstacles;
- who has initiative, who is off-balance, exhausted, injured, or exposed;
- what each combatant can reasonably perceive and attempt;
- how an action changes position, options, or risk;
- why the outcome follows from skill, preparation, numbers, terrain, error, fatigue, chance, or a combination.

Do not turn a fight into a list of disconnected strikes, or make every attack land cleanly. Use a clear spatial model and selective detail. See `references/combat-choreography.md`.

### 7. Continuity and quality pass

Check the finished chapter against the draft and available canon. Correct definite errors. Do not silently resolve major uncertainties involving death, betrayal, succession, culprit identity, alliance, decisive battle outcome, relationship status, or fundamental world rules. If a safe, noncommittal version works, use it and note the assumption only if material.

Use `references/quality-checklist.md` before delivery.

## Controlled autonomy

### Usually safe to invent
- sensory details, gestures, minor transitions, incidental movement;
- connective action needed to make a scene readable;
- dialogue wording that expresses an already-established intent;
- minor tactical beats consistent with the stated outcome and character capabilities;
- incidental background details that do not constrain future plot.

### Ask or flag before deciding
- major deaths, betrayals, reveals, victories, defeats, allegiances, marriages, inheritances;
- the true culprit or motive in a mystery;
- decisive tactical reversals that change the battle's outcome;
- new magic or technology rules;
- major changes to character identity, motivation, relationship, or moral boundary;
- contradictions in dates, parentage, succession, or established events.

Do not ask about every minor gap. Ask one concise question only when plausible answers would lead to materially different stories.

## Default delivery

Return:
1. A title if appropriate.
2. The complete chapter.
3. Brief continuity notes only when there are material assumptions, conflicts, or new details that may affect later chapters.

Do not return an outline instead of the chapter unless requested. Do not append a long self-evaluation. If there is nothing important to flag, omit notes.

## Task-specific behavior

- **Expand from outline:** create scenes and dialogue, not just longer summary.
- **Rewrite existing prose:** improve the actual prose while preserving content; do not merely comment on it.
- **Continue:** begin from the last confirmed event and maintain voice and continuity.
- **Dialogue-heavy draft:** prioritize re-authored dialogue and character-specific voice.
- **Combat-heavy draft:** apply spatial and causal tracking throughout.
- **Historical or fact-sensitive fiction:** distinguish verified history from fictional divergence; do not imply research or verification that did not occur.
- **Brainstorming or analysis request:** follow the requested mode instead of forcing a chapter.

## Reference routing

- `references/draft-analysis.md`: interpret incomplete or contradictory drafts.
- `references/canon-and-continuity.md`: canon status and continuity.
- `references/narrative-craft.md`: structure, viewpoint, pacing, general prose.
- `references/dialogue-rewriting.md`: substantive dialogue adaptation.
- `references/combat-choreography.md`: spatial, tactical, and causal combat writing.
- `references/cultural-institutions.md`: build a coherent society from institutions, incentives, and everyday practices.
- `references/eastern-court-and-xianxia.md`: ancient Chinese imperial institutions and cultivation-world adaptations.
- `references/western-feudal-polities.md`: Western feudal and lordly systems without flattening them into generic “feudalism.”
- `references/gender-demographics.md`: historically and contextually grounded cast composition without tokenism or blanket exclusions.
- `references/genre-adaptation.md`: genre-specific constraints.
- `references/quality-checklist.md`: final review.
- `templates/`: optional planning and tracking forms.
