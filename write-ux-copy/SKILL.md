---
name: write-ux-copy
description: Write and review concise, high-quality interface copy for desktop and product applications. Use whenever creating or changing user-facing UI text: buttons, menus, labels, dialogs, errors, settings, tooltips, empty states, onboarding, permissions, notifications, search, commands, or status messages. Favors Apple-like restraint, clarity, contextual awareness, and platform conventions. Treats copy as part of the interaction design, not prose added afterward.
---

# Interface copy

Write interface copy with the restraint and precision expected from exceptionally well-designed products.

Think Apple, Linear, Figma, Raycast, Arc, Notion, and other interfaces where the words feel inevitable: short, calm, precise, consistent, and subordinate to the product.

Great interface writing disappears into the interface.

The goal is not to make the product sound clever, conversational, friendly, or impressive. The goal is to make the product immediately understandable.

## Core doctrine

### The best copy may be no copy

Before rewriting text, ask whether it should exist.

The interface already communicates through:

* position
* hierarchy
* icons
* control types
* selection
* grouping
* window and panel titles
* surrounding content
* progress indicators
* disabled states
* animations
* platform conventions

Do not restate what the interface already makes clear.

Prefer, in this order:

1. No text
2. Label
3. Short phrase
4. Sentence
5. Multiple sentences

Move down this list only when the previous level is insufficient.

If removing text does not create meaningful ambiguity, remove it.

Do not fill empty space with explanation.

## What great interface copy feels like

It should be:

* **Clear** — understood on the first pass
* **Brief** — no word can be removed without losing meaning
* **Specific** — names the action, object, problem, or consequence
* **Contextual** — assumes what the interface already communicates
* **Consistent** — one term for one concept
* **Calm** — no unnecessary urgency or personality
* **Natural** — sounds like something a thoughtful human would say
* **Useful** — helps the user understand, decide, act, or recover

When these conflict:

**Clarity beats brevity.
Brevity beats personality.
Consistency beats variety.**

## Think in PACE

Before writing a screen or important state, consider four things.

### Purpose

What does the user actually need to understand or do?

The hierarchy of the words should match the hierarchy of the interface.

Primary information belongs in:

* the title
* the primary label
* the primary action

Secondary copy should only add information that changes understanding or behavior.

### Anticipation

What will the user wonder or try next?

Answer the important question before it becomes friction.

Useful:

`Upload failed`

`File exceeds the 10 MB limit.`

`Choose file`

Not useful:

`An error occurred during the upload process.`

Anticipation does not mean explaining every future step. Reveal information when it becomes relevant.

### Context

How much does the user already know from the interface and the action they just took?

A menu item may need only:

`Duplicate`

A dialog opened from a project may need:

`Delete project?`

It usually does not need:

`Are you sure you want to delete the currently selected project?`

Desktop applications provide unusually rich context. Use it.

### Empathy

Write for the person trying to accomplish something, not for the system reporting its internal state.

Prefer:

`Couldn't connect to GitHub`

over:

`OAuth provider authentication failure`

But empathy is not cheerfulness. In frustrating or serious moments, calm precision is more respectful than personality.

## Delete before you rewrite

For every string, ask:

1. Does the user need this information?
2. Do they need it now?
3. Is it already communicated elsewhere?
4. Does it change what they will understand or do?
5. Can the design communicate it better than text?

If the answer does not justify the copy, remove it.

Do not use copy to compensate for a confusing interface when the interaction can be improved instead.

The best error message is often preventing the error.

The best confirmation dialog is often making the action undoable instead.

The best instruction is often making the control obvious.

## Assume interface context

Do not make every string independently self-explanatory.

Inside a project menu:

`Rename`

not:

`Rename this project`

Inside a dialog titled `Delete project?`:

`Delete`

not:

`Delete project`

Inside a search field in the command palette:

`Search commands`

not:

`Type here to search through available commands`

Inside Git settings:

`Disconnect`

not:

`Disconnect your GitHub account`

unless multiple accounts or services make the object ambiguous.

Context removes words.

Use it.

## Information hierarchy

A polished interface does not give every piece of information equal weight.

Use this hierarchy:

#### Level 1 — Action or state

The essential information.

`Connection lost`

`Delete workspace?`

`No results`

#### Level 2 — Necessary context

Only what changes understanding.

`Changes will sync when you're back online.`

#### Level 3 — Recovery or next action

Usually represented by the controls themselves.

`Try again`

#### Level 4 — Detail

Hide behind:

* disclosure
* help
* details
* documentation
* tooltips
* secondary screens

Do not put Level 4 information into Level 1 UI.

## Voice and tone

### One voice

The product should sound like the same product everywhere.

Before adding or changing copy, inspect nearby strings and existing terminology.

Do not introduce local stylistic variation for novelty.

If the product calls something a `workspace`, do not alternate between:

* workspace
* space
* team
* project

unless these are different concepts.

Maintain a terminology list when the product is substantial:

| Preferred | Avoid       | Meaning                                  |
| --------- | ----------- | ---------------------------------------- |
| workspace | team, space | Shared top-level environment             |
| archive   | hide, store | Remove from active view without deleting |
| delete    | remove      | Permanently destroy                      |

Consistency is more important than avoiding repeated words.

### Flexible tone

Voice stays consistent. Tone changes with the moment.

#### Routine actions

Neutral and minimal.

`Saved`

`Connected`

`3 updates available`

#### Empty states and onboarding

Can be slightly warmer, but remain useful.

`No projects yet`

`Create a project to get started.`

#### Errors

Calm and direct.

`Couldn't save changes`

`Check your connection and try again.`

#### Destructive actions

Plain and serious.

`Delete workspace?`

`This permanently deletes the workspace and its projects.`

#### Security, privacy, or data loss

Explicit. No playfulness.

Never use humor to soften serious consequences.

## Quality bar

Before accepting UI copy, ask:

#### Necessity

* Does this text need to exist?
* Is this the right moment for it?

#### Clarity

* Will the intended user understand it immediately?
* Is anything vague?

#### Context

* Am I repeating information already visible?
* Can the surrounding interface carry more of the meaning?

#### Brevity

* Can any word be removed without losing meaning?

#### Specificity

* Does the action name what actually happens?
* Does the error describe the real problem rather than a generic failure?

#### Consistency

* Does this use existing product terminology?
* Is the same action called the same thing elsewhere?

#### Tone

* Is the tone appropriate to the stakes?
* Is personality getting in the way?

#### Recovery

* If something failed, can the user tell what to do next?

#### Platform

* Is there an established OS or application convention we should use?

#### Accessibility

* Does the control remain understandable without relying on visual context alone?
* Should the accessible name contain more context than the visible label?

#### Localization

* Will the string translate cleanly?

If any answer exposes unnecessary copy, remove or rewrite it.

## Writing workflow

When writing new interface copy:

### 1. Recon

Read nearby UI text first.

Identify:

* product terminology
* platform
* audience
* component
* user action that led here
* current state
* reversibility
* stakes
* surrounding visual context

Do not invent a new voice locally.

### 2. Identify the minimum message

Write down what the user genuinely needs to know.

Do not draft polished prose yet.

### 3. Try removing the copy

Ask whether UI structure, state, or controls already communicate it.

### 4. Write the shortest clear version

Start with the essential noun or verb.

Add context only when ambiguity remains.

### 5. Check the surrounding interface

Remove repetition.

Make sure the string works with:

* title
* buttons
* icon
* current selection
* parent menu
* screen location

### 6. Check terminology

Reuse existing terms exactly.

### 7. Check tone and stakes

Routine → quiet
Error → calm
Destructive → explicit
Security/data loss → serious

### 8. Read it aloud

If it sounds robotic, bureaucratic, overly cheerful, or like marketing copy, rewrite it.

### 9. Cut again

Remove every word that does no work.

## Reviewing existing copy

When auditing a product, prioritize issues in this order:

1. Misleading or incorrect copy
2. Missing consequences or recovery
3. Ambiguous actions
4. Inconsistent terminology
5. Unnecessary interruption
6. Redundant explanation
7. Wordiness
8. Tone inconsistency
9. Minor stylistic polish

Do not spend time polishing a sentence that should be deleted.

When possible, distinguish:

* **Remove** — text is unnecessary
* **Rewrite** — text is needed but weak
* **Redesign** — the interaction itself creates the writing problem

## Output behavior

When asked to write a single UI string, return the strongest recommendation first.

Do not produce ten synonymous options.

Provide alternatives only when they represent genuinely different product decisions, such as:

* more concise
* more explicit
* safer for an irreversible action

When reviewing existing copy, prefer:

| Current | Recommended | Reason |
| ------- | ----------- | ------ |

Keep reasons short.

When implementing UI, apply these principles automatically to any user-facing strings even when the user did not explicitly ask for UX writing.

Do not mention these rules to the end user.

Just write better copy.

## Reference

- Language, tone, and mechanics (AI voice, plain language, punctuation, pronouns, filler, localization, accessibility): [language.md](language.md)
- Component-specific guidance (buttons, menus, dialogs, errors, toasts, forms, settings, notifications, length heuristics): [components.md](components.md)
