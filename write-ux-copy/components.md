# Component guidance

## Buttons

Buttons describe actions.

Use verbs.

Prefer:

* `Save`
* `Create project`
* `Move`
* `Export`
* `Connect`
* `Try again`
* `Delete`
* `Replace file`

Avoid generic labels when the action matters:

* `OK`
* `Yes`
* `No`
* `Submit`
* `Confirm`
* `Continue`

`Continue` and `Done` are appropriate when they genuinely describe navigation rather than a domain action.

For consequential actions, the button should name the consequence.

Dialog:

**Delete branch?**

Actions:

`Cancel`
`Delete`

Not:

`Cancel`
`OK`

Keep action vocabulary consistent across a flow. Do not alternate arbitrarily between `Next`, `Continue`, and `Proceed`.

## Menus and commands

Desktop menus should be especially concise.

Use established command language:

* `New window`
* `Open…`
* `Open recent`
* `Duplicate`
* `Rename`
* `Move to folder…`
* `Copy link`
* `Copy path`
* `Show sidebar`
* `Check for updates…`
* `Close window`

Do not turn commands into explanatory sentences.

Prefer system terminology and conventions over invented phrasing.

Use ellipses according to the target platform's convention when an action requires more input before it can execute.

## Toolbars

Toolbar labels should identify the command, not explain the icon.

Prefer:

`Share`

not:

`Share this document with other people`

Prefer:

`Filter`

not:

`Filter the items shown in this list`

If a familiar icon plus placement makes the action obvious, the visible label may be unnecessary. Still provide an appropriate accessible name.

Visible brevity and accessible clarity are separate concerns.

## Tooltips

Tooltips identify or clarify unfamiliar controls.

Usually:

1–4 words.

Good:

* `Toggle sidebar`
* `Copy link`
* `Mute notifications`
* `Open in browser`
* `Previous change`

Do not put documentation in tooltips.

Do not use a tooltip merely to repeat a visible label.

For unfamiliar behavior, a short secondary hint may be appropriate:

`Open preview`
`⌘↩`

## Dialogs and sheets

A dialog interrupts the workflow. Every word must justify the interruption.

First ask:

**Should this be a dialog at all?**

Use blocking UI when the user must make a decision now.

Do not interrupt users to report routine success.

### Dialog anatomy

Ideally:

**Title**

One clear question or statement.

**Description**

Only when the title and actions are insufficient.

**Actions**

Specific and scannable.

A user should often be able to understand the decision from:

**title + buttons**

without reading the body.

Example:

**Replace “notes.txt”?**

`A file with this name already exists.`

`Cancel` `Replace`

Do not write:

**Are you sure?**

The user should never need the body to discover what they are being asked to confirm.

## Destructive actions

For irreversible or difficult-to-reverse actions:

1. Name the action.
2. Name the object.
3. State the meaningful consequence.
4. Say whether it can be undone when that matters.

Good:

**Delete workspace?**

`This permanently deletes “Acme” and its projects.`

`Cancel` `Delete`

Do not exaggerate danger.

Do not add confirmation dialogs to harmless, easily reversible actions.

Prefer undo where appropriate.

## Errors

Errors should help the user recover.

When known, communicate:

1. What failed
2. Why
3. What can be done

But do not mechanically include all three if fewer are sufficient.

#### Known cause

**Couldn't upload file**

`File exceeds the 10 MB limit.`

`Choose file`

#### Recoverable network failure

**Couldn't sync changes**

`Check your connection and try again.`

`Try again`

#### Unknown cause

**Couldn't save changes**

`Try again.`

Do not invent a cause.

Never present speculation as explanation.

Avoid:

* `Error 403` without useful context
* `Invalid input`
* `Illegal character`
* `An unexpected error occurred`
* `Oops! Something went wrong`
* blaming the user

Technical diagnostics can be available under `Details` when useful.

Error codes are for support and debugging, not the primary message.

### Inline validation

Tell the user how to satisfy the requirement.

Prefer:

`Use at least 8 characters`

over:

`Password is invalid`

Prefer positive instruction:

`Use letters and numbers`

over:

`Don't use symbols`

when both communicate the same rule.

Place errors near the thing that needs correction.

## Success states

Do not celebrate routine actions.

Prefer:

`Saved`

`Link copied`

`Invitation sent`

`Export complete`

Not:

`Your export has been successfully completed!`

If the result is already visually obvious, consider showing nothing.

A document visibly appearing in the requested folder may not need a toast saying:

`Document created`

Feedback should reduce uncertainty, not create notification noise.

## Toasts

Toasts are transient. Users may see them for only a moment.

Usually use one short clause.

Good:

* `Link copied`
* `Changes saved`
* `Project archived`
* `Couldn't connect`
* `Download complete`
* `Moved to Trash`

Avoid body copy unless the user genuinely needs it.

Do not put important instructions only in a disappearing toast.

Avoid toasts for events the interface already makes unmistakably clear.

## Progress and loading

Describe the work.

Prefer:

* `Connecting…`
* `Downloading…`
* `Indexing files…`
* `Installing update…`
* `Waiting for approval…`

Avoid:

`Please wait while we connect to the server…`

Do not say `Please wait`.

If a reliable duration or remaining amount is available and useful, show it.

`Uploading 3 of 8`

is better than:

`Uploading…`

Do not invent progress estimates.

## Empty states

Not every empty state needs prose.

#### Self-explanatory

**No notifications**

Nothing else required.

#### First use

**No projects yet**

`Create a project to get started.`

`New project`

#### Search

**No results for “calendar”**

`Clear search`

#### Filter

**No projects match these filters**

`Clear filters`

An empty state should usually orient the user and, when appropriate, provide the next action.

But do not use every empty state as onboarding.

Do not put persistent information in an empty state; it disappears when content appears.

## Search

Keep search prompts terse and scoped.

Good:

* `Search`
* `Search files`
* `Search commands`
* `Search settings`

Avoid:

`Type here to search your files`

Do not explain how a search field works.

No-results copy should reflect the query or filtering context when useful.

`No results for “Atlas”`

is more informative than:

`Nothing found`

## Forms

Labels identify the information being requested.

Use:

`Email address`

not:

`Please enter your email address`

Helper text should explain something the label cannot.

Useful:

**Repository URL**

`HTTPS and SSH URLs are supported.`

Not useful:

**Repository URL**

`Enter the repository URL.`

Do not use placeholder text as the only label.

Placeholders are best for examples or formatting:

`name@example.com`

`https://github.com/org/repo`

Instructions belong near the decision they affect.

## Settings

Setting labels describe the enabled state.

Good:

`Open at login`

`Show line numbers`

`Send read receipts`

`Automatically check for updates`

Avoid negative toggle labels that create double negatives:

`Don't hide line numbers`

Settings descriptions answer a question the label cannot.

**Open at login**

`Launch the app when you sign in.`

If the behavior is obvious from the setting name, omit the description.

Do not give every setting helper text merely for consistency.

## Permissions

Ask for permission when the user understands why it is needed.

Explain the value before the system permission prompt when the reason is not obvious.

Prefer contextual requests:

**Allow notifications**

`Get notified when someone mentions you.`

Not:

`This app requires notification permissions to provide notifications.`

Say what the user gets, not which API the application wants.

Do not pressure or guilt users into granting permission.

If a feature can work partially without permission, say so when relevant.

## Onboarding

Onboarding should help users do something, not tell them everything about the product.

Prefer action over explanation.

Avoid:

`Welcome to Atlas, the powerful new way to organize and manage all of your projects in one convenient place.`

Prefer:

**Create your first project**

or simply put the user in the product and let them begin.

Do not explain standard UI conventions.

Teach unfamiliar concepts at the moment they become relevant.

Prefer contextual education over tours.

## Notifications

Notifications must earn interruption.

Lead with the useful information.

Good:

**Build failed**

`main failed after 4m 12s.`

Good:

**Jean mentioned you**

`“Can you review the new flow?”`

Avoid:

**New notification**

`You have received a new notification.`

Do not repeat the app name when the operating system already shows it.

Do not use notification copy as marketing copy unless that is explicitly the product's purpose and the user opted into it.

## Links

Describe the destination or action.

Prefer:

* `View documentation`
* `Manage subscription`
* `Privacy policy`
* `Learn about permissions`

Avoid:

* `Click here`
* `Read more` when multiple destinations could exist
* raw URLs in interface prose

Do not encode pointer assumptions unnecessarily.

Use `select` rather than `click` when the interface may support multiple input methods and the distinction does not matter.

## Length guidance

These are heuristics, not quotas.

#### Buttons

Usually 1–3 words.

#### Menu items

Usually 1–4 words.

#### Tooltips

Usually 1–5 words.

#### Toasts

Usually 2–7 words.

#### Dialog titles

Usually 2–6 words.

#### Setting names

Usually 1–5 words.

#### Supporting descriptions

Usually one short sentence.

#### Errors

Usually one short sentence plus an action, when needed.

Never add words to satisfy a target.

Never remove words if doing so introduces ambiguity.
