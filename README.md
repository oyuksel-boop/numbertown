# Isabel Leyla's Number Town

A calm maths game for a pupil starting P5 in Scotland. You run four shops in a
little town; the maths *is* the work of the shop. There are no timers and nothing
flashes red. Learning a skill earns a star, and stars are worth real pocket money.

**Play:** https://oyuksel-boop.github.io/numbertown/

## Level

Everything is pitched at **the end of P4** — First Level of Curriculum for
Excellence. Numbers to 1000, tables to 10, unit fractions and tenths, money and
change within £10, o'clock / half past / quarter past and to.

That is deliberate. A child who has just started P5 has *finished* P4, and
consolidating that is worth more than being stretched by next June's work. Every
skill is also written at two harder levels — mid-P5 and end-of-P5 — sitting
unused in the file. A grown-up flips the dial in the settings panel when school
has moved on; nothing already earned is affected.

## The money

Two separate pots, and the difference between them is the whole point.

| | What it is | Can it go down? |
|---|---|---|
| 🏦 **The bank** — £8.00 | 80 skills × 10p, earned by *learning a skill*. | **Never.** |
| 👛 **The purse** — £2.00 | 10p put at risk each day, banked at the end of the session. | Yes — 1p per careless slip, max 5p a day. |

**£10.00 maximum, ever.** The purse can only be dented by a mistake on a skill she
has *already earned a star for*. A mistake on something new never costs anything —
a child who is afraid of losing money stops attempting hard questions, and
attempting hard questions is the entire job.

The purse only banks on a day she does at least 10 questions, so the incentive is
attached to turning up and doing the work rather than to being right.

## Earning a star

Four clean answers — first try, no hint — spread over **at least two different
days**. Four right answers in one burst is a good day; still having it two days
later is learning, and the money follows the second one.

Measured on a simulated child at ~85% accuracy: a star every **14 questions**,
roughly 24p a day, so the £10 lasts about a school term of regular practice.

She works on **three skills at a time** rather than sampling all eight in a shop,
which is what makes stars actually arrive. Once a skill is starred it comes back
now and then to stay sharp — and a fumble there puts it back in the practice set
without ever taking money back.

## When she gets it wrong

1. Nothing goes red. The shopkeeper says have another look, and a **hint** appears.
2. Second miss: the **worked solution**, step by step.
3. Then she types the answer in herself before moving on. Repair, not punishment.
4. Still stuck after a few goes? A quiet "leave this one for now" appears.

Every question is generated fresh, so the same skill is never the same sum twice.

## The shops

| Shop | Curriculum |
|---|---|
| 🥐 The Bakery | naming fractions · equivalence · fraction of an amount · comparing · adding · fractions ↔ decimals ↔ percentages |
| 🛒 The Market | adding money in pence · change · multiplying and sharing cost · best value · column addition · two-step problems · rounding |
| 🐾 The Cat Café | tables to 10 · division facts · × 10 · 2-digit × 1-digit · remainders · bigger multiplying · factors · multiples |
| 🚂 The Station | reading a clock · writing the time · durations · arrival times · timetables · units of time · counting to the hour · calendars |

32 skills so far, of 80 planned. Measurement, shape and angle, coordinates, data
handling, patterns, place value and decimals are the next seven shops.

## Guardrails

- **No timers anywhere.** Timed drilling is the best-documented trigger of maths
  anxiety at this age; roughly a third of children are affected.
- **A day stops at 20 questions** — about fifteen minutes. It prevents both
  grinding and money-farming.
- **Effort is praised, not just correctness.** Getting there after a hint still
  earns coins and still counts.
- 🪙 **Coins** are separate play money, earned on every question and never lost.
  They are the fun; the pennies are the milestone.

## For grown-ups

The ⚙️ button opens a panel with skill-by-skill progress, a list of what is looking
shaky, a payday total with a **Mark as paid** button, the level dial, and switches
to turn shops off so she stays on whatever school is doing this term.

It sits behind a **4-digit PIN**, asked for the first time the panel is opened.
Without it nobody can reset the bank, mark money as paid, or wipe her progress —
and the reset button deliberately keeps the PIN, so a reset cannot be used to
unlock the panel. It is a latch against a curious nine-year-old, not real security.
If the PIN is forgotten, clearing the site's data in Chrome removes it along with
everything else, so write the total down first.

Everything is stored in the browser on that one device. No account, no analytics,
no network calls after the page loads.

## Install on a phone

Open the link in Chrome → menu → **Add to Home screen**. It then runs full-screen
and works offline.

## Files

- `index.html` — the whole game: one file, no build step, no dependencies
- `manifest.webmanifest`, `sw.js`, `icon-*.png` — installability and offline support

To change the maths, edit the `SKILLS` array near the top of the `<script>` block.
Each skill is one generator taking a level, and returns a question, a hint and a
worked solution. Every generator is checked by an independent verifier — 144,000
generated questions, answers re-derived from the prompt text rather than trusted.
Bump `CACHE` in `sw.js` after any edit so phones fetch the new version.
