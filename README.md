# Isabel Leyla's Number Town

A calm maths game for a P5 pupil in Scotland. You run four shops in a little town;
the maths *is* the work of the shop. There are no timers and nothing flashes red.
Answering well earns stars, and the stars are worth real pocket money.

**Play:** https://USERNAME.github.io/REPO/ *(replace once Pages is live)*

## The money

Two separate pots, and the difference between them is the whole point.

| | What it is | Can it go down? |
|---|---|---|
| 🏦 **The bank** — £8.00 | 80 stars × 10p. A star is earned by *learning a skill*, not by getting one question right. | **Never.** |
| 👛 **The purse** — £2.00 | 10p is put at risk each day and banked at the end of the session. | Yes — 1p per careless slip, max 5p a day. |

**£10.00 maximum, ever.** The purse can only be dented by a mistake on a skill she has
*already earned a star for*. A mistake on something new never costs anything — that is
deliberate, because a child who is afraid of losing money stops attempting hard questions,
and attempting hard questions is the entire job.

The purse only banks on a day she does at least 10 questions. The incentive is attached to
turning up and doing the work, which is the version of paying-for-schoolwork that the
evidence actually supports.

## Earning a star

Three clean answers — first try, no hint — spread over **at least two different days**.
Spaced practice is how memory works, and it also means a star cannot be farmed in one
lucky sitting.

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
| 🛒 The Market | adding money · change · multiplying and sharing cost · best value · column addition · two-step problems · rounding |
| 🐾 The Cat Café | tables to 12 · division facts · × 10/100/1000 · 2-digit × 1-digit · remainders · 2-digit × 2-digit · factors · multiples |
| 🚂 The Station | reading a clock · 12h ↔ 24h · durations · arrival times · timetables · units of time · crossing midnight · calendars |

That is 32 of the planned 80 skills, covering the core of CfE Second Level. Measurement,
shape and angle, coordinates, data handling and simple algebra are the next four shops.

## Guardrails

- **No timers anywhere.** Timed drilling is the best-documented trigger of maths anxiety
  at this age; roughly a third of children are affected.
- **A day stops at 20 questions** — about fifteen minutes. It prevents both grinding and
  money-farming.
- **Adaptive**: the least-practised skill comes up most, with one question in four
  revisiting something already mastered so it stays sharp.
- **Effort is praised, not just correctness.** Getting there after a hint still earns coins
  and still counts.
- 🪙 **Coins** are separate play money, earned on every question and never lost. They are
  the fun; the pennies are the milestone.

## For grown-ups

The ⚙️ button opens a panel with skill-by-skill progress, a list of what is looking shaky,
a payday total with a **Mark as paid** button, and switches to turn shops off so she stays
on whatever school is doing this term.

It sits behind a **4-digit PIN**, asked for the first time the panel is opened. Without it
nobody can reset the bank, mark money as paid, or wipe her progress — and the reset button
deliberately keeps the PIN, so a reset cannot be used to unlock the panel. It is a latch
against a curious nine-year-old, not real security: anyone with a browser console could get
past it. If the PIN is forgotten, clearing the site's data in Chrome removes it, along with
everything else — so write the total down first.

Everything is stored in the browser on that one device. No account, no analytics, no
network calls after the page loads.

## Install on a phone

Open the link in Chrome → menu → **Add to Home screen**. It then runs full-screen and works
offline.

## Files

- `index.html` — the whole game: one file, no build step, no dependencies
- `manifest.webmanifest`, `sw.js`, `icon-*.png` — installability and offline support

To change the maths, edit the `SKILLS` array near the top of the `<script>` block in
`index.html`. Each skill is a generator that returns a question, a hint, and a worked
solution. Bump `CACHE` in `sw.js` after any edit so phones fetch the new version.
