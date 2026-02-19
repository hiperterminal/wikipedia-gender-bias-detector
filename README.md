# Wikipedia Gender Bias Detector

## 🔗 [**Try the tool live →**](https://nethahussain.github.io/wikipedia-gender-bias-detector/)

> No login. No API key. No AI. Works in any browser, instantly.

---

A fully client-side tool that analyses Wikipedia biographies of women for systematic gender bias. Paste any article title or URL and the tool returns a detailed report of flagged passages, organised by bias category, with explanations and example rewrites for each.

---


## What it detects

The tool checks against **49 bias patterns** across 6 categories:

| Category | Examples |
|---|---|
| **Relational Definition** | "wife of", "daughter of", "the woman behind" |
| **Appearance Focus** | beauty/attractiveness language, body descriptions |
| **Diminutive Language** | "just a girl", "managed to", "despite being a woman" |
| **Unnecessary Gendering** | "female scientist", "woman engineer", "for a woman" |
| **Achievement Minimisation** | passive voice, "helped to develop", "stumbled upon" |
| **Patronising Tone** | "feisty", "plucky", "remarkably she", "opinionated" |

It also checks for structural issues: whether the opening paragraphs lead with personal/family details over professional identity, and whether passive voice is used at a rate that systematically removes the subject's agency.

---

## How it works

- Enter a Wikipedia article title or URL in the search box
- The tool fetches the article from Wikipedia's public API
- It runs the text through 49 pattern-matching rules
- Flagged passages are displayed with: matched phrase, explanation of the bias, suggested approach, and an example rewrite
- Each flag links directly to the relevant **section** of the Wikipedia editor so you can fix it immediately

**Scope:** Women's biographies only. Articles about men or non-biographical pages are rejected with a clear message.

---

## Features

- 🔍 Live Wikipedia search autocomplete as you type
- 📌 "Fix on Wikipedia" button links to the exact section containing the problem
- ✏️ Example rewrites (before/after) for most patterns — randomly varied each run
- 🖨️ Print / save as PDF
- ⚡ Fully offline-capable after first load — no data is sent anywhere except to Wikipedia's own API

---

## Technical notes

- Pure HTML + JavaScript (React 18 via CDN)
- No build step, no npm, no bundler
- No AI, no external API, no authentication
- Zero data transmission beyond fetching the Wikipedia article
- Pattern matching is rule-based and deterministic: same article → same results
- Results require human review — not every flagged passage will be biased in context

---

## Scope and limitations

This tool uses **pattern matching**, not AI or semantic understanding. It will:
- Occasionally flag passages that are not actually biased in context
- Miss bias that is expressed in unusual or indirect language
- Not detect bias that requires cultural or historical knowledge to recognise

It is designed as an **aid to human editors**, not a replacement for editorial judgement.

---

## Background

Developed as part of Wikipedia gender equity work. Intended for use by Wikipedia editors, researchers, and anyone interested in improving how women are represented in encyclopaedic biography.

---

## Translating this tool

A full translation guide is available for anyone wishing to adapt the tool to another language. It covers all 49 patterns with explanations and before/after examples, notes on adapting the regular expressions, and instructions for switching the Wikipedia API to a different language edition.

📄 [Download the translation guide (Word document)](https://github.com/nethahussain/wikipedia-gender-bias-detector/blob/main/translation-guide.docx)

---

## Licence

This project is released into the public domain under the [CC0 1.0 Universal (CC0 1.0) Public Domain Dedication](https://creativecommons.org/publicdomain/zero/1.0/).

You can copy, modify, distribute and perform the work, even for commercial purposes, all without asking permission.
