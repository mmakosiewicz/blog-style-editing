# blog-style-editing

Editorial craft rules for blog and article prose, as an agent skill: voice, sentence and paragraph discipline, heading conventions, intro and conclusion structure, definition/explanation/answer patterns, link formatting, and a table of **AI-tell patterns to cut**.

It adapts rather than imposes. Give it your house style and that wins; give it nothing and it uses sensible defaults and tells you what it assumed.

## Install

```bash
git clone https://github.com/mmakosiewicz/blog-style-editing ~/.claude/skills/blog-style-editing
```

Swap the path for whatever your agent reads skills from (`~/.pi/agent/skills/` for Letaido). No dependencies — it's instructions, not code. Most environments load skills at session start, so restart afterwards. Then ask: *"edit this draft"*, *"make this sound less like AI"*, *"apply our style"*, *"copy-edit this post"*.

## What it hands back

**Every finding carries the replacement text**, quoted as current versus proposed. "This paragraph is too long" is an observation; "split after '…ranking factor.' and start the next paragraph at 'But'" is a fix. Phrasings like "consider tightening this" or "could be more specific" are explicitly banned.

It also offers to apply the edits to the file so you can diff them.

Two things stay as flags rather than rewrites, because guessing does real damage:

- **A missing example or statistic.** It names the gap and asks. It never invents one.
- **A claim it can't verify.** Flagged for the author, not rephrased into something that merely sounds more confident.

## AI-tell patterns

A table of the constructions that read as machine-written even when the content is good, each with the fix:

| Pattern | Why it's out |
|---|---|
| "It's not X, it's Y" | The signature AI contrast pivot |
| "This isn't theoretical" | Announces credibility instead of showing it |
| "If you're new to X… If you're already doing X…" | Dual-audience hedge |
| Em-dash used for a contrast pivot | Substitutes punctuation for an argument |
| "In this article, we will…" | Formal throat-clearing |
| Tricolon everywhere ("clear, concise, and compelling") | Rhythm on autopilot |

…plus corporate speak, hype adjectives, and unearned urgency ("in today's fast-paced world").

## Brand-neutral by design

A conventions table names what genuinely varies between publications — heading case, person, spelling, contractions, Oxford comma, product-mention policy — with instructions never to silently apply one brand's conventions to another. Where a publication's own guide disagrees, the publication wins.

**On product mentions:** there is no quota. Zero product mentions in an article is a perfectly good outcome, competitors get named plainly where they're the right answer, and the only test is whether the reader needs the tool to do the thing the section is about.

`references/ahrefs-profile.md` is included as a worked example of a brand profile. Copy its shape for your own publication.

## Companion skills

- [**query-match-audit**](https://github.com/mmakosiewicz/query-match-audit) — does the page match the query you want to win, and is it worth retrieving?
- [**ai-extractability-audit**](https://github.com/mmakosiewicz/ai-extractability-audit) — can AI search engines chunk, understand and cite its facts?

They stack: be *relevant* enough to retrieve, *extractable* enough to quote, *well written* enough to deserve it.

## License

MIT — see [LICENSE](LICENSE).
