---
name: ditectrev-books
description: Generate new Ditectrev Awesome book & course repos from the shared template—README-as-book chapters, reveal.js slides, CodeSandboxes, extra resources, GitHub naming, and release notes. Use when creating a new Ditectrev book, study guide, course, slides, or cloning the HTML / A11Y / AZ-900 pattern.
---

# Ditectrev Books & Course Slides

Follow this skill whenever the task is a new or updated **Ditectrev Awesome Book & Course**. Do not invent a generic textbook layout. The book **is** `README.md`. Slides live in `__presentation-slides/index.html`. Copy structure, wording, and file names from the three source repos below.

## Source repos (copy, don't reinvent)

| Flavor | Repo | Role |
| --- | --- | --- |
| Hands-on (code + CodeSandbox) | [Awesome-HTML-Book-Course-HyperText-Markup-Language-HTML](https://github.com/Ditectrev/Awesome-HTML-Book-Course-HyperText-Markup-Language-HTML) | Canonical interactive-web book |
| Hands-on (code + CodeSandbox, later automation) | [Awesome-A11Y-Book-Course-Web-Accessibility-A11Y](https://github.com/Ditectrev/Awesome-A11Y-Book-Course-Web-Accessibility-A11Y) | Canonical a11y book + sandbox scripts |
| Certification study guide (no sandboxes) | [Awesome-Microsoft-Azure-AZ-900-Microsoft-Azure-Fundamentals-Study-Guide-Book-Course](https://github.com/Ditectrev/Awesome-Microsoft-Azure-AZ-900-Microsoft-Azure-Fundamentals-Study-Guide-Book-Course) | Canonical exam study guide |
| Slides starter | [Ditectrev/__presentation-slides](https://github.com/Ditectrev/__presentation-slides) | reveal.js theme; clone, never rename |

Pick **one flavor** before writing anything:

- **Hands-on book & course** if the topic is a skill students practice in the browser (HTML, A11Y, CSS, JS APIs). Matches HTML + A11Y.
- **Study Guide Book & Course** if the topic is a vendor exam (AZ-900 and similar). Matches AZ-900.

## When to use

Use this skill when the user asks to:

- Create a new Ditectrev book, course, or study guide
- Scaffold a repo named `Awesome-…-Book-Course-…`
- Write or expand `README.md` chapters in the Ditectrev voice
- Generate `__presentation-slides` from book headings
- Add numbered CodeSandbox examples (`Tap2Play`)
- Add `__extra-resources` recording notes
- Match GitHub description, Support block, Discord, Patreon, or release notes to existing books

Do **not** use this skill for unrelated docs sites, per-chapter `docs/` trees, Marp/Google Slides, or a root `LICENSE` for sellable book content.

## Canonical repo layout

GitHub file lists sort `*` after `_`, so double-underscore folders stay at the top. Keep these exact names:

```text
Awesome-{Topic}-Book-Course-{Expanded-Name}/
├── .github/
│   └── FUNDING.yml                 # patreon: Ditectrev
├── .gitignore
├── README.md                       # THE BOOK (4.5k–6.5k+ lines)
├── images/
│   ├── promotional.png             # required; H1 hero
│   ├── discord.png                 # required; Discord CTA
│   ├── ebook.jpg                   # required marketing asset
│   ├── codesandbox.svg             # hands-on only
│   └── {topic_diagram}.png         # optional figures used in README + slides
├── __extra-resources/              # recording notes; always include community file
│   ├── our-community-social-media.md
│   ├── our-community-social-media.pdf
│   ├── {topic-note}.md             # optional; pair with .pdf when exported
│   └── {topic-note}.pdf
└── __presentation-slides/          # clone of Ditectrev/__presentation-slides
    ├── index.html                  # ONLY file to author for the deck
    ├── images/                     # copy figures + codesandbox.svg here too
    ├── LICENSE                     # MIT (reveal.js) — keep
    └── README.md                   # clone instructions — keep
```

Hands-on books that automate sandboxes (A11Y pattern) also add:

```text
├── .env.example                    # CSB_API_KEY=
├── package.json
├── package-lock.json
└── scripts/
    ├── codesandbox.cjs
    ├── codesandbox.config.json
    └── sandboxes-manifest.json
```

Study guides do **not** add CodeSandbox scripts, `codesandbox.svg`, or sandbox footnotes.

### Naming rules that actually appear in the repos

| Piece | Hands-on (HTML / A11Y) | Study guide (AZ-900) |
| --- | --- | --- |
| GitHub repo | `Awesome-HTML-Book-Course-HyperText-Markup-Language-HTML` | `Awesome-Microsoft-Azure-AZ-900-Microsoft-Azure-Fundamentals-Study-Guide-Book-Course` |
| Pattern | `Awesome-{Short}-Book-Course-{Expanded}` | `Awesome-{Vendor}-{ExamCode}-{ExamName}-Study-Guide-Book-Course` |
| H1 | `# 📚 Awesome HTML Book & Course: HyperText Markup Language (HTML)` | `# 📚 Awesome Microsoft Azure AZ-900 (Microsoft Azure Fundamentals) Study Guide Book & Course` |
| GitHub description | `⭐ Awesome HTML Book & Course with interactive CodeSandboxes. Learn HTML online with pleasure.` | `⛳️ PASS: Microsoft Azure AZ-900 (Microsoft Azure Fundamentals) by learning based on our Study Guide Book & Course.` |
| Default branch | `main` | `main` |
| Homepage | Udemy course URL or `https://shop.ditectrev.com/product/…` | shop product URL |
| Topics | `ditectrev`, `awesome-list` / `awesome`, topic keywords | `ditectrev`, `awesome-list`, `udemy-course`, exam slug (`az-900`, `az900`) |
| Root `LICENSE` | **None** (content is sold) | **None** |
| Extra-resources folder | `__extra-resources` | AZ-900 currently misspells `__extra-resourcers` — **use `__extra-resources` for new books** |

npm `package.json` `name` (A11Y): lowercase kebab of the repo, e.g. `awesome-a11y-book-course-web-accessibility-a11y`.

### License

- Do **not** add a repository-root `LICENSE`. None of the three book repos have one; the README is commercial (shop, Udemy, Etsy, eBay, Google Play, Patreon).
- Keep `__presentation-slides/LICENSE` (MIT, Hakim El Hattab / reveal.js).
- Do not claim the book is MIT/ISC just because `package.json` defaults to ISC.

### Shared constants (copy verbatim)

- Discord: `https://discord.gg/RFjtXKfJy3`
- Discord image alt/title: `Join our Discord`
- Patreon: `https://patreon.com/Ditectrev?utm_medium=unknown&utm_source=join_link&utm_campaign=creatorshare_creator&utm_content=copyLink`
- Shop: `https://shop.ditectrev.com/product/{product-slug}`
- Udemy instructor: `https://www.udemy.com/user/social-ditectrev/`
- GitHub org: `https://github.com/Ditectrev`
- CodeSandbox org: `https://codesandbox.io/u/Ditectrev`
- `.github/FUNDING.yml`: set `patreon: Ditectrev`; leave other platforms commented as in the GitHub template

Copy `images/discord.png`, `images/ebook.jpg`, `images/codesandbox.svg` (hands-on), and `__extra-resources/our-community-social-media.md` from an existing book. Create a new `images/promotional.png` for the topic.

### `.gitignore`

Copy the fuller ignore from AZ-900 / A11Y (macOS, Windows, Linux junk, `.idea/`, `.vscode/`). For sandbox-script books also ignore `node_modules/`, `.env`, `.env.local`. Do not ship HTML's two-line `.gitignore` as the new default.

### `.editorconfig` (optional)

If added, name it exactly `.editorconfig` (HTML's copy has a hidden prefix — do not clone that filename). HTML uses `charset = utf-8`, `end_of_line = lf`, `insert_final_newline = true`, `indent_style = tab`, `indent_size = 2`.

## README.md is the book

There are **no** `chapters/` files. Typical size: HTML 4676 lines, AZ-900 4850, A11Y 6525. Write the whole book into `README.md`.

### Fixed front-matter order (do not reorder, do not skip)

Use these exact heading strings (swap only `{Topic}` / `Study Guide Book & Course` vs `book & course`):

1. `# 📚 Awesome {Title}`
2. `![Promotional image](images/promotional.png)`
3. `## ❣️ Support`
4. `## ✨ This book & course is unlike any {Topic} book & course you will find online.`  
   Study guides: `## ✨ This Study Guide Book & Course is unlike any {Exam} Study Guide Book & Course you will find online`
5. `## ⌛️ Short and to the point; why should you take the book & course:`
6. `## ☝️ Book & Course Updates` (study guides: `Study Guide Book & Course Updates`)
7. `## 🙋‍♀️ & 🙋‍♂️ Contribution`
8. `## Who this book & course is for:`
9. `## Requirements`
10. `## Table of Contents`
11. Chapter `##` headings (the book body)
12. Closing `## Conclusion…` and/or `## Additional Resources…` / appendices

### Support block (all three books)

Keep the intro sentences identical. Fill product URLs. Channel order is fixed:

```markdown
## ❣️ Support

There are many ways to support us; in exchange, you'll get this material in a proper format:

- ❤️ [shop.ditectrev.com, in EPUB or PDF formats](https://shop.ditectrev.com/product/{slug}),
- ▶️ [Udemy, in an interactive video course format](https://www.udemy.com/course/{slug}/?referralCode={code}),
- 🆓 [Shorter, but free, part of our Udemy course is available on YouTube](https://www.youtube.com/playlist?list={id}),
- 📚 [Google Play Books, in PDF format](https://play.google.com/store/books/details?id={id}),
- 🛍️ [Etsy, in PDF format](https://ditectrev.etsy.com/listing/{id}),
- 🛒 [eBay, in PDF format]({ebay-url}),
- 🔄 [Patreon subscription allows you to get access to all of the materials in EPUB and PDF formats. You can also buy separate items on Patreon, but the subscription technically allows us to include all updates for EPUB and PDF formats. Hence, you get EPUB and PDF updates when you subscribe to Patreon](https://patreon.com/Ditectrev?utm_medium=unknown&utm_source=join_link&utm_campaign=creatorshare_creator&utm_content=copyLink).

💰 If you work for a company, you could probably easily claim this expense while learning this topic. For us, it's about being in the game or not.

⭐ Good ratings & reviews help us to survive. Please don't forget to leave a nice one when you purchase an item.
```

If a storefront URL is unknown, keep the channel and leave a TODO — do not drop channels.

### Unlike-any / community block

Copy this paragraph and swap only the topic sentence (`learn about HTML` / `learn about Web Accessibility` / `pass the Microsoft Azure AZ-900 … confidently`):

```markdown
✋ Join a live online community and a book & course taught by industry experts and learn about {Topic}. We aim to build an ecosystem of Information Technology (IT) certifications and online courses in cooperation with the technology industry. We believe it will give our students 100% confidence in the pacing market in an open-source environment. We are just at the beginning of our way, so it's even better for you to join now!

[![Join our Discord](images/discord.png 'Join our Discord')](https://discord.gg/RFjtXKfJy3)
```

### Why-take list (always this skeleton)

```markdown
1. Always happy to answer your questions 😊
2. Unhappy? Please raise a refund; we'll always accept it 💸
3. Learn about topics, such as 😱
   - {chapter / topic bullets}
   - **Much More!**
4. Real Life examples ✅
5. The book & course explains the topic fully in-depth 🔬
6. {N} **unique** interactive `Tap2Play` CodeSandboxes 🕹️
```

Rules:

- Item 6 exists **only** on hands-on books. `{N}` must equal the number of `[![Edit NNN-…](images/codesandbox.svg)]` links (HTML: 120; A11Y: 61).
- Hands-on item 3 is a **nested outline** of chapters (HTML). A11Y uses a shorter nested list. Study guides use a **flat alphabetical topic dump** (AZ-900) and omit item 6.
- Study guides say `Study Guide Book & Course` in items 5 and the heading.

### Updates, contribution, audience, requirements

**Updates** — GitHub release tags, newest last. Recurring cadence from all three books:

```markdown
**[v1.0.0](../../releases/tag/v1.0.0): {Month D, YYYY}.**

- Launch of the book.

**[v1.1.0](../../releases/tag/v1.1.0): {date}.**

- Post-recording improvements.

**[v1.1.0](../../releases/tag/v1.1.0): {later date}.**

- Launch of the course.
```

Patches after that use `v1.1.1` (A11Y: "Fix CodeSandbox first example link."). Duplicate `v1.1.0` for post-recording vs course launch is the existing convention — keep it.

**Contribution** (HTML wording; use `#table-of-contents`):

```markdown
We are so thankful for every contribution, which makes sure we can deliver top-notch content. Whenever you find a missing resource, broken link in a [Table of Contents](#table-of-contents), the wrong answer, please submit an [issue](../../issues). Even better would be a [Pull Request (PR)](../../pulls).
```

**Audience** — every bullet starts with `👨‍🎓`. Hands-on pattern (from HTML/A11Y): enthusiasts, people who have heard of the topic, professionals who want basics without burnout, sceptical developers, self-paced learners, students, specialists who want A to Z. Study-guide pattern (AZ-900): exam candidates plus a long role list (Cloud Engineers, DevOps, PMs, SREs, …).

**Requirements** — always these three, topic-swapped:

```markdown
- 🤩 Excitement to learn!
- 0️⃣ Prior knowledge is required;
- ✅ You can learn {Topic} solely based on our book & course.
```

Study guides: `You can pass the {Exam} Exam solely based on our Study Guide Book & Course.`

### Table of Contents

- Nested GitHub-flavored bullets with heading anchors.
- Every `##` / `###` / example heading that students should jump to must appear.
- Hands-on books list `Example: …` headings and `Summary: {Chapter}` headings.
- A11Y-style books nest H4 under H3 (WCAG criteria, techniques).
- After the TOC, start the first chapter with `##`, never another front-matter section.

## Book content generation

Write the TOC **first**, then generate body text that uses **the same heading strings** so anchors stay valid.

### Heading levels

| Level | Use |
| --- | --- |
| `##` | Chapter (`Introduction to HTML`, `Core Azure Services`) |
| `###` | Section (`What is HTML?`, `Azure Compute Services`) |
| `####` | Subsection / technique (`Brief History…`, `WCAG 1.1.1 Non-text Content`) |
| `##### Example: …` | Worked example (HTML). A11Y often embeds examples under `####` without a separate Example heading |

End major chapters with `### Summary: {Exact Chapter Title}` (HTML, A11Y). Study guides more often close with conclusion / exam / glossary instead of per-chapter summaries.

### Tone (from the real prose)

- Instructor **we**, student **you**. Direct, practical, no academic fluff.
- Teach in depth with **real-life examples** (explicit brand promise in the why-take list).
- Spell out a term once, then use the acronym (`HyperText Markup Language (HTML)`, `Web Content Accessibility Guidelines (WCAG)`).
- Link **canonical docs** (MDN, W3C/WAI, Microsoft Learn) — AZ-900 uses `- **Documentation Reference:**` plus a Learn URL on each concept.
- Emoji belong in the **front-matter**, not in chapter body.
- Prefer working code and concrete scenarios over theory-only paragraphs.
- Do not claim "100% accessible" / "guaranteed pass" in chapter body; A11Y explicitly treats accessibility as a continuum, AZ-900 still promises you can pass using this guide in Requirements.

### Hands-on chapter recipe (HTML / A11Y)

For each `###` / `####` section:

1. 1–3 short teaching paragraphs (what it is, why it matters, when to use it).
2. Optional figure — **centered markdown table**, italic caption, same alt text as the image:

```markdown
|![A timeline graphic showing key milestones in the history of HTML, from HTML 1.0 to HTML5.](images/html_timeline.png)|
|:--:|
| *A timeline graphic showing key milestones in the history of HTML, from HTML 1.0 to HTML5.* |
```

3. A complete, runnable example in a fenced block (`html`, `css`, `js`, `javascript`, `json`, `bash`). HTML/A11Y examples are self-contained documents or clearly labeled fragments.
4. CodeSandbox widget + footnote (see below) when the example is meant to be played.
5. Bullet walkthrough of what the code does (HTML after the sandbox; A11Y often explains before/after).
6. Call out CodeSandbox limitations in bold when the demo cannot run there (HTML Service Worker / offline examples).

**Bad vs good** appears in A11Y (`<!-- Avoid: … -->` / `<!-- Prefer: … -->`). Use that for any topic with a common anti-pattern.

**Summary paragraph** restates the chapter, then points to the next chapter by name ("starting with Understanding Users and Disabilities").

### Study-guide chapter recipe (AZ-900)

For each concept:

```markdown
#### Virtual Machines (VMs)

  Azure VMs are on-demand, scalable computing resources …

- **What is a vCPU?**
  …

  **Key Characteristics:**
  - **Performance:** …
  - **Isolation:** …

  **Practical Example:**

  ```plaintext
  VM Size Examples:
  ├── B2s (Budget)
  │   ├── 2 vCPUs
  │   └── …
  ```

- **Documentation Reference:**
  [Azure … Documentation](https://learn.microsoft.com/…)
```

Recurring labels: **What is it?**, **Practical Example:**, **Why are they important?**, **Key Points**, **Common Use Cases**, **Documentation Reference**. Use `plaintext` trees (`├──` / `└──`) instead of CodeSandboxes. Include an **Exam Preparation** chapter (overview, official/community resources, exam tips) plus **Conclusion** (Key Takeaways, Next Steps, Additional Resources) and **Appendices → Glossary**.

### Closing chapters

Hands-on books end like HTML:

- Recap / next-steps / community (optional)
- `## Common Challenges and Debugging Tips` with Challenge + Debugging Tips per subsection
- `## Conclusion: {Topic} Course`
- `## Additional Resources and Reading Materials` (tutorials, books, forums, tools, courses)

A11Y ends with operational chapters (Testing, Documentation) then `## Appendix A–D` (WCAG quick reference, glossary, tools, checklist templates). Each appendix has `### Summary: Appendix {X}: …`.

Study guides end with exam prep, conclusion, glossary — not CodeSandbox recap.

## CodeSandboxes (hands-on only)

Every playable example uses this **exact** triple, with a zero-padded sequential number shared by the Edit label, the footnote id, and (usually) the sandbox slug:

```markdown
[![Edit 001-Basic HTML Structure](images/codesandbox.svg)](https://codesandbox.io/p/sandbox/001-basic-html-structure-7gq85k)

[^1]CodeSandbox: Basic HTML Structure.

[^1]:[CodeSandbox: Basic HTML Structure](https://7gq85k.csb.app/), last access: January 1, 2025.
```

Rules derived from HTML + A11Y:

- Numbers are **001, 002, …** through the whole book (HTML to 120; A11Y to 061).
- Footnote index `[^N]` matches the decimal number (001 → `[^1]`).
- Editor URL: `https://codesandbox.io/p/sandbox/{slug}`.
- Preview URL: `https://{id}.csb.app/`.
- Title after `Edit NNN-` matches the heading / example name.
- Image is always `images/codesandbox.svg`.
- `last access:` is a real date.
- Update the why-take count when the number of sandboxes changes.
- Prefer one sandbox per distinct example. A11Y sometimes has separate HTML and CSS sandboxes under the same heading — only do that when book and sandbox would otherwise drift.

### Sandbox file policy (from A11Y `scripts/codesandbox.cjs`)

- README may show an HTML **body fragment**; the sandbox must be a **full document** (`<!DOCTYPE html>`, `lang`, `title` = heading).
- If the README adds CSS, the sandbox `index.html` includes the preceding HTML plus those CSS blocks.
- Runtime: static browser template; collection path like `/Awesome A11Y Book/examples`.
- To batch-create sandboxes, copy A11Y's `scripts/codesandbox.cjs` + `codesandbox.config.json` + `sandboxes-manifest.json`. Commands: `codesandbox:scan`, `codesandbox:create`, `codesandbox:insert`, `codesandbox:verify`. Needs `CSB_API_KEY` in `.env` (see `.env.example`).

Slides reuse the same two links (see Slides).

## `__extra-resources`

This folder is **Udemy recording leftovers and deep links**, not a second copy of the book. Students of the GitHub README may never open it; the course does.

Always include:

- `our-community-social-media.md` + `.pdf` — copy from HTML/A11Y (Facebook, GitHub, Instagram, LinkedIn, Reddit, X, YouTube, Discord, shop, eBay, Etsy, education.ditectrev.com, Udemy, Google Play Books, iOS app, CodeSandbox user, Patreon).

Then add **kebab-case** notes that match what was shown on camera:

| Kind | Examples from the repos |
| --- | --- |
| "During the recording I showed…" link lists | HTML `online-tutorials-guides.md`, `file-api.md`, `webrtc-api.md` |
| Portal / tool walkthroughs with screenshots | AZ-900 `tco-calculator.md` + `tco1.png`…`tco8.png` |
| Demo media used in examples | A11Y `sample-video.mp4`, `sample-video-en.vtt`, `t-rex-roar.mp3`, `chart-q1.png` |
| PDF export of the same note | pair `foo.md` + `foo.pdf` when the note is used in recording; some HTML notes are PDF-only (`canonical-links.pdf`, `screen-readers.pdf`) |

Do not move these materials into `README.md`. Do not invent a docs site for them.

## Slides generation

### Bootstrap (required)

From the book repo root, as documented in `__presentation-slides/README.md`:

```bash
git clone https://github.com/Ditectrev/__presentation-slides
```

**Do not rename the folder.** The double underscore keeps slides at the top of the GitHub file list. Follow [reveal.js](https://revealjs.com) for runtime behavior.

Author **only**:

- `__presentation-slides/index.html` — `<title>` + the markdown inside `<textarea data-template>`
- `__presentation-slides/images/` — copy every figure the deck references (`codesandbox.svg`, diagrams). Paths in the deck are `images/…` relative to the slides folder, not the book root.

Leave `dist/`, `plugin/`, `css/`, tests, and examples untouched.

### `index.html` shell (shared by all three)

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>{Exact README H1 without the 📚 emoji}</title>
  <link rel="stylesheet" href="dist/reset.css">
  <link rel="stylesheet" href="dist/reveal.css">
  <link rel="stylesheet" href="dist/theme/serif.css">
  <link rel="stylesheet" href="plugin/highlight/monokai.css">
  <style>
    .fragment.blur { filter: blur(1rem); }
    .fragment.blur.visible { filter: none; }
  </style>
</head>
<body>
  <div class="reveal">
    <div class="slides">
      <section data-markdown>
        <textarea data-template>
# Welcome <!-- .slide: data-transition="zoom" data-transition-speed="slow" -->

---

## {First Chapter Title} <!-- .slide: data-transition="zoom" data-transition-speed="slow" -->

---
        </textarea>
      </section>
    </div>
  </div>
  <script src="dist/reveal.js"></script>
  <script src="plugin/notes/notes.js"></script>
  <script src="plugin/markdown/markdown.js"></script>
  <script src="plugin/highlight/highlight.js"></script>
  <script>
    Reveal.initialize({
      hash: true,
      slideNumber: 'c/t',
      plugins: [RevealMarkdown, RevealHighlight, RevealNotes]
    });
  </script>
</body>
</html>
```

Required config: theme **serif**, highlight **monokai**, `hash: true`, `slideNumber: 'c/t'`, plugins Markdown + Highlight + Notes. Custom fragment class `.fragment.blur` as above.

Preview: `cd __presentation-slides && npm start` (gulp serve). Node `>=18`.

### Map README → slides (do this mechanically)

Walk the **Table of Contents** in order. Every TOC heading becomes a slide whose heading text is **character-identical** (so recording and GitHub stay in sync).

| README | Slide |
| --- | --- |
| (none) | `# Welcome` — always first |
| `## Chapter` | Title-only `## Chapter` slide, then children |
| `### Section` | Title-only `### Section`, then content slides |
| `#### Subsection` | Title-only, then bullets / code / image |
| `##### Example: …` | Code + sandbox links |
| `### Summary: …` | Title-only or short bullets (A11Y often title-only) |
| Figure table | Same table markdown on its own slide |
| Numbered concept (AZ-900) | `### Concept` + fragment bullets taken from the Practical Example list |
| `plaintext` tree | Fenced `plaintext` on a slide; a second slide may list the "why" bullets |
| Closing chapters | Keep Conclusion / Additional Resources (HTML, AZ-900). A11Y currently stops after Documentation and Maintenance and **omits Appendix A–D** from the deck — appendices may stay book-only |

**Never** paste full README paragraphs onto a slide.

### Slide body patterns (copy these classes)

Every slide heading ends with the same comment:

```markdown
### What is HTML? <!-- .slide: data-transition="zoom" data-transition-speed="slow" -->
```

Horizontal separator is a line containing only `---`.

**Fragment bullets** (181 uses in the HTML deck; this is the default list style):

```markdown
* The `<!DOCTYPE>` Declaration <!-- .element: class="fragment custom blur highlight-current-blue fade-up" -->
* The `<head>` Section <!-- .element: class="fragment custom blur highlight-current-blue fade-up" -->
```

**Stepped code highlight** (reveal highlight plugin; `|` separates clicks):

````markdown
```html[|1|2|11|2,11|3|6|3,6]
<!DOCTYPE html>
<html lang="en">
  ...
</html>
```
````

**Sandbox on a slide** (no footnotes; both editor + preview):

```markdown
[![Edit 001-Basic HTML Structure](images/codesandbox.svg)](https://codesandbox.io/p/sandbox/001-basic-html-structure-7gq85k)

[CodeSandbox: Basic HTML Structure](https://7gq85k.csb.app/).
```

**Images** — same centered table as the book, but the file lives in `__presentation-slides/images/`.

**Density**

- One idea per slide. Title-only openers are normal (all three decks).
- 4–8 fragment bullets max; split if more.
- HTML deck ≈ 278 `---` separators; A11Y ≈ 212; AZ-900 ≈ 137. A new book should be in that range, not a 20-slide summary.
- Do not add Welcome/Discord/promotional image slides unless the user asks — none of the three decks do.

## Repeatable workflow (new book)

Work in this order. Do not start slides before the TOC is stable.

1. **Choose flavor** — hands-on vs study guide.
2. **Name the repo** using the tables above. Default branch `main`. Description + topics + homepage as specified.
3. **Scaffold** the canonical layout. Copy FUNDING.yml, gitignore, Discord/ebook/codesandbox assets, and `our-community-social-media.md` from a source repo.
4. **Clone slides:** `git clone https://github.com/Ditectrev/__presentation-slides` (keep the name).
5. **Write README front-matter** (H1 through Requirements) with placeholders for storefront URLs.
6. **Write the Table of Contents** as the contract. Get chapter names approved if a human is in the loop.
7. **Generate chapters** with the matching recipe. Keep heading text = TOC text.
8. **Hands-on:** add numbered examples + CodeSandboxes; run A11Y-style scan/insert if scripts are present; set why-take count = sandbox count.
9. **Generate slides** by walking the TOC into `index.html` markdown. Copy images into `__presentation-slides/images/`. Set `<title>` to the book title.
10. **Extra resources** — community pair plus recording notes / media.
11. **Local check** — README TOC anchors; `npm start` in slides; spot-check sandbox editor + `.csb.app` URLs.
12. **Release** — tag `v1.0.0` "Launch of the book". After Udemy recording, `v1.1.0` "Post-recording improvements", then same tag note "Launch of the course".

When extending an existing book: update TOC + body + slides together; never leave a heading that exists in only one of the three.

## Checklists

### Repo / GitHub

- [ ] Name matches `Awesome-…-Book-Course-…` (add `Study-Guide` only for exams)
- [ ] Description uses ⭐ + CodeSandboxes (hands-on) or ⛳️ PASS (exam)
- [ ] Topics include `ditectrev` and the subject slugs
- [ ] Homepage is shop or Udemy
- [ ] `.github/FUNDING.yml` has `patreon: Ditectrev`
- [ ] No root `LICENSE`
- [ ] `__presentation-slides/` and `__extra-resources/` spellings (not AZ-900's `__extra-resourcers`)
- [ ] `images/promotional.png`, `images/discord.png`, `images/ebook.jpg` present
- [ ] Hands-on: `images/codesandbox.svg` in **both** `images/` and `__presentation-slides/images/`

### README front-matter

- [ ] H1 starts with `📚 Awesome`
- [ ] Support has all seven channels in the fixed order
- [ ] Discord CTA uses `images/discord.png` and `https://discord.gg/RFjtXKfJy3`
- [ ] Why-take items 1, 2, 4, 5 match the template; item 3 lists this book's topics; item 6 only if sandboxes exist and the count is exact
- [ ] Updates, contribution, audience (`👨‍🎓`), requirements (`🤩` / `0️⃣` / `✅`) present
- [ ] TOC anchors resolve (GitHub slug rules: punctuation stripped, spaces → `-`)

### Chapters

- [ ] Heading strings equal TOC strings
- [ ] Hands-on: code → sandbox → explanation; summaries named `Summary: {Chapter}`
- [ ] Study guide: Practical Example trees + Microsoft Learn (or vendor) documentation links
- [ ] Figures use the three-row caption table
- [ ] Official links are live; no leftover `TODO` in student-facing body unless the user asked for stubs

### CodeSandboxes (hands-on)

- [ ] Sequential `001…N` with matching `[^N]` footnotes and `last access` dates
- [ ] Editor URL `codesandbox.io/p/sandbox/…` and preview `https://{id}.csb.app/`
- [ ] Why-take count = number of Edit badges
- [ ] Sandbox HTML is a full document even if the README shows a fragment

### Slides

- [ ] `<title>` matches the book title
- [ ] serif + monokai + `hash` + `slideNumber: 'c/t'` + Markdown/Highlight/Notes
- [ ] First slide is `# Welcome`
- [ ] Every slide heading has `data-transition="zoom"` / `data-transition-speed="slow"`
- [ ] Lists use `fragment custom blur highlight-current-blue fade-up`
- [ ] TOC headings appear in order; no essay paragraphs
- [ ] Sandbox and image paths resolve under `__presentation-slides/images/`
- [ ] `npm start` shows the deck without markdown parse errors

### Extra resources / release

- [ ] `our-community-social-media.md` + `.pdf`
- [ ] Recording-only notes stay here, not in README
- [ ] `v1.0.0` / `v1.1.0` notes follow the launch → post-recording → course pattern

## Agent operating rules

- Clone or read a source repo of the **same flavor** before writing. Prefer HTML for general hands-on, A11Y for accessibility/WCAG, AZ-900 for exams.
- Preserve Ditectrev marketing copy in the front-matter; do not "improve" it into generic GitHub README style.
- If storefront/Udemy/YouTube IDs are unknown, keep the Support skeleton and mark missing URLs clearly rather than deleting channels.
- Do not restructure the book into multiple markdown files.
- Do not replace reveal.js with another slide stack.
- Do not add a root license or change `__presentation-slides` to a friendlier folder name.
- When the user asks for "just slides" or "just chapters", still keep headings aligned with the other artifact if it already exists.
