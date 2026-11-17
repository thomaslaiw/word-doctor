# Word Doctor

A whole-class, teacher-guided TELL (Technology-Enhanced Language Learning) activity for
Hong Kong primary English learners (P5–P6). Built as a single self-contained HTML file —
no dependencies, no build step, no internet connection required at runtime.

**[Play it →](https://thomaslaiw.github.io/word-doctor/)**

---

## The problem it addresses

Primary learners in Hong Kong tend to judge their own English by **grammar alone**. If the
sentence parses, they accept it — even when the sentence is impossible in the real world.
A student writes that a person is *boiling* with generosity, or that boiling water can be
*drunk immediately*, and no one notices, because the grammar is fine.

This is also the exact blind spot of many AI writing assistants: strong on surface form,
weak on whether a well-formed sentence actually makes sense.

The activity targets that habit directly, in a single lesson.

## The activity

**One sitting, 35 minutes, six rounds.** Teacher projects the app; the class works as a
team of "word doctors" diagnosing one sick sentence per round.

Per round:

1. The teacher reads the sentence aloud.
2. 45-second pair discussion — the class argues for a diagnosis.
3. The class commits publicly (show of hands, or mini-whiteboards).
4. The teacher locks in the answer.
5. **Only then** does the AI's comment appear — in English with Chinese support.

Scoring is flat: **+10 correct, −5 for a confident wrong answer**. No individual
leaderboard; the score belongs to the class.

### The six rounds

| # | Word | The problem | Design purpose |
|---|------|-------------|----------------|
| 1 | boiling | *Boiling* is for water, not for a person's kindness | Establishes the routine |
| 2 | careless | Wrong word family in an adverb slot | Clear, buildable error |
| 3 | boiling | Grammar is fine — but you cannot drink boiling water now | Correct form, false meaning |
| 4 | hot | The word means the opposite of the weather | Meaning over grammar |
| 5 | careful | The highlighted word is **correct**; the error is elsewhere | Breaks the "blame the highlighted word" heuristic |
| 6 | warmly | Adverb used where an adjective belongs | Independent consolidation |

Round 5 is the trap: by then the class has learned "the highlighted word is the problem,"
and this round punishes that assumption.

## Design decisions worth knowing

**The teacher never rules on the AI.** There is no "AI agrees" or "AI is wrong" badge, no
bonus for beating the AI, and no tally of rounds where the class out-scored it. The AI's
comment is presented as a comment — a second reader that has seen the same sentence but
does not know the class's answer. The teacher stays the pedagogical authority; the class
decides what to make of the AI. This also means the teacher never has to be certain about a
machine's output in front of thirty-five children.

**Everything is addressed to the student.** No explanation describes "the student" in the
third person, and none instructs a teacher. Feedback describes *the sentence*, never the
child — so a learner can be wrong without being named.

**Chinese appears only in the AI comment panel.** The sentence, question and options stay
English-only, so the language task is not scaffolded away. The Chinese sits beside the AI's
comment and its "why" explanation, where beginners need help parsing the reasoning.

**The AI comments are pre-written, not a live model call.** Each comment is staged in
advance so its accuracy is known to the teacher before the lesson. A live model could say
something unhelpful mid-lesson; a fixed set cannot.

## Pedagogical grounding

| Theory | Where it shows up |
|--------|-------------------|
| Swain (Output Hypothesis) | The class must commit to an answer aloud before anything is revealed |
| Long (Interaction) | Pair discussion forces negotiation of meaning |
| Schmidt (Noticing) | Rounds 1 and 4 look correct; round 5 defeats the class's own heuristic |
| Vygotsky / Wood, Bruner & Ross (ZPD, scaffolding) | Rounds escalate; the teacher models reasoning early and withdraws it |
| Black & Wiliam (formative assessment) | Immediate "why" after every round, never a mark without a reason |
| Mayer / Sweller (cognitive load) | One sentence, one question, four options, no animation, no auto-audio |
| Self-Determination Theory | Class score not individual ranking; cooperative goal, no public leaderboard |

## Assessment and evidence

Formative and in-lesson: pair-discussion observation, the on-screen record of what the
class chose each round, and an **exit slip** in the last three minutes asking:

1. Which word will you be careful with from now on?
2. What was the difference between correct grammar and a correct meaning?

Prompt 2 is the transfer check. "AI is bad" is not yet at standard; "it's good at grammar
and bad at meaning" is.

## Running it

Open `index.html` in any modern browser. That's the whole installation.

- **Full session** — 6 rounds, ~35 minutes. Use this for the lesson.
- **Short demo** — 3 rounds, ~5 minutes. Use this for a presentation.

No devices are needed for learners. One teacher laptop and a projector (or interactive
whiteboard) is the entire technical requirement, and no internet connection is needed
during the lesson.

Keyboard shortcuts: **A B C D** to choose, **Enter** to lock in, **Enter** again to advance.

## Data and ethics

The app collects no learner data. Nothing leaves the browser; there are no accounts, no
analytics, and no network calls. Class choices live on the teacher's screen for the
duration of the lesson only.

The content is deliberately non-sensitive — everyday vocabulary in everyday contexts — so
no learner is asked to engage with personal material in front of peers.

## Context

Built for **INT4099 Emerging Technologies for Language Learning and Assessment**,
2026-27 Semester 1, EdUHK.
