# Language, tone, and mechanics

## Avoid AI voice

Do not default to the stylistic habits common in generated copy.

Avoid:

* `Oops!`
* `Uh oh!`
* `Awesome!`
* `Great job!`
* `You're all set!`
* `Let's get started!`
* `We've got you covered.`
* `Something went wrong.`
* `It looks like…`
* `It seems that…`
* `Please note that…`
* `Simply…`
* `Just…`
* `Easily…`
* `Successfully…`

These words are not forbidden, but they must earn their place.

Prefer:

`Account created`

over:

`Awesome! Your account has been successfully created!`

Prefer:

`Couldn't save`

over:

`Oops! It looks like something went wrong while saving.`

## Use plain language

Use the familiar word unless precision requires a specialized term.

Prefer:

* `Delete`
* `Move`
* `Rename`
* `Connect`
* `Sign in`
* `Turn on`
* `Try again`
* `Not connected`

Avoid:

* `Initiate`
* `Execute`
* `Terminate`
* `Authenticate` when `Sign in` is accurate
* `Utilize`
* `Proceed`
* `Connectivity unavailable`

Technical products may use technical language when their users expect it.

Do not simplify established domain terminology into something less precise.

`Rebase branch` may be exactly right in a developer tool.

## Front-load meaning

Users scan interfaces.

Put the differentiating information first.

Prefer:

`Couldn't connect to GitHub`

over:

`There was a problem connecting to GitHub`

Prefer:

`3 files couldn't be uploaded`

over:

`We were unable to upload 3 of your files`

Prefer:

`Requires macOS 27`

over:

`This feature is only available on devices running macOS 27 or later`

when space is constrained and the meaning remains clear.

## Platform language

Respect the operating system.

Use terminology users already know.

Examples may include:

* `Show in Finder`
* `Move to Trash`
* `System Settings`
* Windows File Explorer terminology
* platform-standard keyboard notation

Do not invent a cross-platform phrase when the application can use the native term.

If the product is cross-platform, strings may differ by platform.

Platform conventions are part of the vocabulary.

## Desktop-specific restraint

Desktop applications are information-dense and frequently used.

Optimize for repeated exposure.

Copy that feels pleasantly explanatory the first time may become noise on the hundredth use.

For frequently used UI:

* favor recognition over explanation
* keep labels stable
* avoid greetings
* avoid motivational language
* avoid redundant descriptions
* favor keyboard-friendly terminology
* preserve spatial and terminological consistency

A professional desktop application should become quieter as the user becomes more familiar with it.

## Power-user interfaces

Do not dumb down concepts the audience understands.

In a developer tool, these can be good copy:

* `Checkout branch`
* `Rebase`
* `Force push`
* `Open diff`
* `Stage changes`
* `Run task`

Clarity means using the user's language, not replacing precise terminology with generic language.

Explain consequences where necessary:

**Force push to `main`?**

`Remote commits not in your local branch may be lost.`

## Naming features

Good names:

* fit where they appear
* set accurate expectations
* survive use across the product
* work in natural sentences
* avoid implementation details
* remain understandable across languages when possible

Prefer established category terms when they exist.

Do not rename familiar concepts merely to make the product sound unique.

Avoid branded names for ordinary functionality unless the feature genuinely benefits from a distinct identity.

A feature name should help users predict what it does.

## Sentence case

Default to sentence case:

`Create new project`

not:

`Create New Project`

Follow platform conventions when they differ.

Keep capitalization consistent within equivalent components.

## Punctuation

UI labels usually do not need periods.

Buttons:

`Save changes`

not:

`Save changes.`

Short descriptions and full sentences generally do.

Avoid unnecessary exclamation marks.

Use an exclamation mark only when the emotional intensity is genuinely appropriate.

Most software needs very few.

## Pronouns

Use `you` only when it makes the sentence clearer or more natural.

Do not insert `your` everywhere.

Prefer:

`Notifications`

over:

`Your notifications`

Prefer:

`Delete account?`

over:

`Are you sure you want to delete your account?`

Avoid unnecessary `we`.

Prefer:

`Couldn't connect`

over:

`We're having trouble connecting`

unless the product deliberately uses first-person voice and it adds useful meaning.

## Filler words

Delete words that usually add no useful information:

* just
* simply
* easily
* quickly
* successfully
* currently
* actually
* please
* note that
* in order to

Before:

`Simply select a folder in order to continue.`

After:

`Select a folder`

Before:

`Your changes were successfully saved.`

After:

`Changes saved`

## Accessibility

Visual context can justify shorter visible copy, but accessibility must remain complete.

Do not make visible labels verbose solely because assistive technology needs more context.

Instead, when appropriate, provide a fuller accessible name or description.

A toolbar may visually show only an icon while exposing:

`Toggle sidebar`

to assistive technology.

Links should make sense outside surrounding prose when users may navigate links independently.

Do not rely on:

* color alone
* iconography alone
* placeholder text alone
* spatial wording such as `the button on the right`

Error states should be announced with enough context to identify what failed.

Keep language predictable and structurally consistent.

## Localization

Write copy that survives translation.

Avoid:

* idioms
* puns
* culturally dependent humor
* sentence fragments assembled around variables
* grammatical assumptions about names or gender
* wordplay required to understand an action

Do not concatenate sentences from fragments.

Use full localizable strings with proper pluralization.

Concise does not mean cryptic. Extremely compressed English may expand badly or become ambiguous in other languages.

## Do not narrate the interface

Avoid:

`Click the button below to continue.`

`Choose an option from the dropdown menu.`

`Use the search field above to search.`

`Press Save to save your changes.`

Controls already communicate interaction.

Describe the task or consequence, not the mechanics.

## Do not restate nearby text

Bad:

**Notifications**

`Manage your notification settings.`

Good:

**Notifications**

Then show the settings.

Bad:

**Delete project?**

`Are you sure you want to delete this project?`

Good:

**Delete project?**

`This can't be undone.`

Every layer should contribute new information.

## Avoid false specificity

Never invent:

* causes
* durations
* progress
* availability
* guarantees
* recovery outcomes

If the system does not know why synchronization failed, do not write:

`Your internet connection was interrupted.`

Write:

`Couldn't sync changes.`

Specificity is valuable only when it is true.

## State the consequence, not implementation

Prefer:

`Changes won't sync across devices`

over:

`Cloud synchronization has been disabled`

when the consequence is what matters.

Prefer:

`Keep the app open to finish uploading`

over:

`Background processing is unavailable`

unless the implementation detail itself is useful.

## Progressive disclosure

Show information at the moment it becomes useful.

Do not front-load:

* advanced behavior
* edge cases
* secondary consequences
* detailed documentation
* troubleshooting

Use:

* tooltips
* `Learn more`
* disclosure controls
* help panels
* secondary dialogs
* documentation

for information that most users do not need immediately.

The primary interface should contain the minimum information necessary to act confidently.

## Interaction beats explanation

When copy becomes complicated, question the design.

If a button requires a paragraph explaining what it does, reconsider the button.

If users repeatedly make the same error, reconsider the input.

If an action is reversible, reconsider the confirmation dialog.

If a status needs constant explanatory copy, reconsider how the status is represented.

Copy is part of interaction design, not a substitute for it.
