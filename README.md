# pre-grade

A first look at a student paper, before the teacher grades it. pre-grade reads the paper and shows the teacher where to look. The grade and the judgement stay with the teacher.

Built for teachers by Anne Becheru, first presented at the workshop "Using AI for the development of entrepreneurial education", 26 November 2026.

## What it checks

| It checks | What you get |
|---|---|
| The argument | The thesis, the reasons, the evidence and the hidden assumptions, in 6 lines |
| The marking criteria | The criteria Oxford, Cambridge, Harvard and Princeton publish for marking written work, or your own grading grid, each with a quote from the paper |
| Critical thinking | 5 levels on the AAC&U Critical Thinking VALUE rubric, each with a quote |
| The writing | Motive, thesis, analysis and counter-argument (Harvard and Princeton writing programs) |
| Originality | Extends, applies or only restates the usual answer |
| Every reference | Verified, wrong, not found, or cannot be checked online. Claims checked against the source's abstract |
| Signs of AI writing | Only specific signs above a stated threshold, each with a quote. No score, no percentage |
| Your next step | 3 to 5 questions to ask the student, and strengths to name in feedback |

It never gives a grade, a band or a verdict. It never sends the student's text to another website: only reference details (author, title, year) are looked up.

## What it is built on

Every source is the institution's own document, linked in [references/frameworks.md](references/frameworks.md):

- Oxford: History examination conventions (2026), English and Law marking criteria
- Cambridge: History, Classics and Psychological and Behavioural Sciences marking criteria
- Harvard: Report on Grading at Harvard College (2023), with the Writing Program's sample rubric; Gordon Harvey, "Elements of the Academic Essay" (Harvard College Writing Program)
- Princeton: Writing Program grading standards (2021), English and Economics standards, the Writing Program lexicon
- Cambridge Assessment: critical thinking definition and taxonomy (2008)
- AAC&U: Critical Thinking VALUE rubric

The criteria are paraphrased with links to the originals. pre-grade is not endorsed by any of these institutions.

## How it was tested

On 25 November 2026 we ran it on papers with known answers:

- Three Cambridge International A level Global Perspectives essays with examiner marks (30, 20 and 10 out of 35). pre-grade ranked them in the same order as the examiners without seeing the marks.
- Prize-winning first-year essays from Harvard's Exposé (2014) and Writing Program excerpts from Princeton (2019).
- Published essays written before ChatGPT existed, to look for false AI alarms. The first version raised some; we removed the AI score and set thresholds, and the second version raised none on these texts.
- A test paper with planted mistakes ([test/](test/)). pre-grade found the invented reference and the misused real study.

These are small tests, not a validation study. Treat every report as a first look.

## Install

**Claude Code**

```
git clone https://github.com/becheruanne-prog/pre-grade ~/.claude/skills/pre-grade
```

Then, in Claude Code: `/pre-grade papers/paper1.md`

**Claude app (claude.ai):** on this page click Code, then Download ZIP. In Claude, open Settings and upload it under Skills. Then attach a paper and ask: "Use pre-grade on this paper."

**Gemini, ChatGPT, Copilot:** open [SKILL.md](SKILL.md), copy all of it into your Gem or Project instructions, and add [references/frameworks.md](references/frameworks.md) as a file. In these apps the reference check uses web search and is less precise.

Try it first on [test/test-essay-social-media.md](test/test-essay-social-media.md) and compare with [test/ANSWER-KEY.md](test/ANSWER-KEY.md).

## Make it yours

Write your own rules in [references/teacher-additions.md](references/teacher-additions.md): your grading grid, the mistakes your students repeat, your course AI policy. One rule per line, in plain words. Your rule wins over the defaults, except the privacy rules and "never grade, never accuse".

## Make it better for everyone

Found something it should do better? Open the file on GitHub, click the pencil, and choose **Propose changes**. Or open an issue and describe what went wrong, with the paper's level and what you expected. Good changes go into the next version for every teacher who uses it.

## Privacy

Use copies of papers with names removed. Write Student 1, Student 2. Follow your institution's data protection rules before using any AI tool on student work.

## License

MIT. See [LICENSE](LICENSE).
