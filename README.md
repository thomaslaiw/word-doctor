# Word Doctor

A whole-class, teacher-guided TELL (Technology-Enhanced Language Learning) activity for
Hong Kong primary English learners (P5–P6). Built as a single self-contained HTML file.

**[Open it →](https://thomaslaiw.github.io/word-doctor/)**

---

## What it does

Two ways to play.

**Built-in set** — six ready-made rounds on vocabulary precision. No key, no network,
works offline.

**Scan a page** — photograph any English page, the words are read from it, and six fresh
rounds are written about the vocabulary in that text. This needs your own DeepSeek API key.

Both run the same game: the teacher projects the screen, the class works as a team of
"word doctors" finding what is wrong with one sick sentence per round.

## The problem it addresses

Primary learners in Hong Kong tend to judge their own English by **grammar alone**. If the
sentence parses, they accept it — even when the sentence is impossible in the real world.
A learner writes that a person is *boiling* with worry, or that boiling water can be
*drunk immediately*, and nobody notices, because the grammar is fine.

That is also the blind spot of many AI writing assistants: strong on surface form, weak on
whether a well-formed sentence actually makes sense.

## The activity

**One sitting, 35 minutes, six rounds.** Per round:

1. The teacher reads the sentence aloud.
2. 45-second pair discussion — the class argues for a diagnosis.
3. The class commits publicly (show of hands, or mini-whiteboards).
4. The teacher locks in the answer.
5. **Only then** does the AI's comment appear — in English with Chinese support.

Scoring is flat: **+10 correct, −5 for a confident wrong answer**. No individual
leaderboard; the score belongs to the class.

## Design decisions worth knowing

**The teacher never rules on the AI.** There is no "AI agrees" or "AI is wrong" badge, no
bonus for beating the AI, and no tally of rounds where the class out-scored it. The AI's
comment is presented as a comment — a second reader that has seen the same sentence but
does not know the class's answer. This also means the teacher never has to be certain about
a machine's output in front of thirty-five children.

**Everything is addressed to the student.** No explanation describes "the student" in the
third person, and none instructs a teacher. Feedback describes *the sentence*, never the
child — so a learner can be wrong without being named.

**Chinese appears only in the AI comment panel.** The sentence, question and options stay
English-only, so the language task is not scaffolded away. The Chinese sits beside the AI's
comment and its "why" explanation, where beginners need help parsing the reasoning. It is
written standard Chinese (書面語), not Cantonese.

**The built-in rounds are pre-written, not model-generated.** Their accuracy is known
before the lesson. A live model could say something unhelpful mid-lesson; the fixed set
cannot. Scanned rounds are generated on demand by choice, and the teacher sees the result
before the class does.

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

## Using the scanner

The scanner needs a DeepSeek API key, because the key belongs to whoever is using it —
there is no shared key in this repository, and no server run by the authors.

1. Get a key at [platform.deepseek.com/api_keys](https://platform.deepseek.com/api_keys).
2. Open the app and enter the class password, then paste your key once.
3. The key is remembered in your browser, like a saved password. **Forget key** wipes it.

How it works: the key is stored in your browser's `localStorage` and used to call DeepSeek
directly from the page. It is never sent anywhere else, and nothing is logged. The
photograph never leaves your device — only the recognised text is sent, and only when you
press **Build the rounds**.

Cost is small: a single six-round generation is a fraction of a cent on DeepSeek's pricing.

## Running it

Open `index.html` in any modern browser, or use the hosted link above. That is the whole
installation for the built-in rounds.

For the scanner, the browser needs internet access and a valid key. The free offline path is
the built-in six rounds.

No devices are needed for learners. One teacher laptop and a projector (or interactive
whiteboard) is the entire technical requirement.

Keyboard shortcuts: **A B C D** to choose, **Enter** to lock in, **Enter** again to advance.

## Data and ethics

The built-in rounds collect nothing: no accounts, no analytics, no network calls.

For scanned rounds, only the recognised text is sent to DeepSeek, using the user's own key.
Photographs stay on the device. No learner data is collected at any point. The content is
deliberately non-sensitive — everyday vocabulary in everyday contexts — so no learner is
asked to engage with personal material in front of peers.

## Context

Built for **INT4099 Emerging Technologies for Language Learning and Assessment**,
2026-27 Semester 1, EdUHK.
