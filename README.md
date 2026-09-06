# Anthracite 1902

A single-file browser game about the anthracite coal strike of 1902. You play
John Mitchell, thirty-two years old, president of the United Mine Workers, from
the walkout in May to the commission's award the following March.

**Play it:** open `index.html` in any browser. No install, no server, no network.
Serve the repo with GitHub Pages and the URL is the whole thing.

## What it is

Four acts, thirty-one beats, one continuous state. Nothing resets between acts:
the demands you file in May decide what the commission is allowed to rule on in
March, and the order you give the pump men in June changes how cold the cities
get in October.

| Act | | What you decide |
|---|---|---|
| I | The Walkout | What the strike is *for* — the demand sheet — and whether the pump men stay |
| II | The Long Summer | Evictions, the relief ledger, Shenandoah, the informer, the funeral |
| III | The Cold | The soft-coal contracts, Hanna's money, and an afternoon with Baer and Roosevelt |
| IV | The Board | Five hearing days, Darrow's closing, and whether to sign the award |

Nineteen distinct endings. The game can end in any act — a broken line or an
empty relief fund finishes it where it stands.

## Reading the screen

- **Voices** — five blocs and how they currently feel about you.
- **Meters** — men out, weeks of food, public opinion, your name, mines intact.
  A red cell is a warning.
- **The strip** — the fields, the coal, and the cities, drawn from live state.
  It is the argument of the whole game in one bar: your power was never the
  picket line, it was the cold.

Dotted terms open a plain-language definition. They are written for a ninth-grade
reader, English learners included.

## At the end of each act

The Scranton Republican writes the act up — what you did, how it landed, and one
quote for you and one against — followed by a ledger of your decisions and the
meter movement each one caused. At the end of the game, **Export the whole
record** produces the run as plain text: every decision, every consequence, each
act's headline, and the award clause by clause. It copies or downloads, and the
text is selectable if a browser blocks both.

## History

The events, the people and the numbers are real: the miners' ton of 2,240 pounds
or more, the company store's credit book, the Coal and Iron Police, the
Shenandoah killing, the Guard, Roosevelt's October 3 conference, the terms
written on J. P. Morgan's yacht, and the award of March 21, 1903 — ten per cent,
a nine-hour day, a checkweighman, a board of conciliation, and no recognition.
Andrew Chippie and Father Curran testified. "The record" notes on the reaction
cards say what actually happened, including where the game lets you do something
Mitchell did not.

## Accessibility

Fully playable by keyboard — Tab to move, Enter or Space to choose, including the
demand sheet, the witness list and the glossary. Visible focus. Text contrast
meets WCAG AA. All motion stops under `prefers-reduced-motion`. Works from
320px up.

## Editing it

Everything is in `index.html`. Beats live in one `BEATS` array tagged `act:1`
through `act:4`; each carries its scene, dateline, text and options. Shared state
is one `S` object with a comment mapping which act touches which field. Beat text
can ask a flag a question with `{{FLAG?yes|no}}`.
