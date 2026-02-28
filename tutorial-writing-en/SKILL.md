---
name: tutorial-writing
description: Writes clear, progressive tutorials for a given technical or domain topic. Use when the user wants to author a tech blog, domain tutorial, or explainer on a concept—especially when an engineer needs to turn a topic into a single, readable tutorial. Guides the author to clarify goals and audience, researches primary sources, and outputs concise, well-structured Markdown.
---

This skill guides the AI to produce **domain tutorials** for engineers or writers: from understanding the topic and audience, to gathering reliable sources, to drafting and polishing the text. It fits the case: “I want to write a blog post or tutorial about this topic.”

## Core design

Tutorials must be **easy to grasp first, then deep**:

- **Easy to grasp**: Start from what the reader already knows or from concrete questions. Use plain language and helpful analogies; avoid opening with jargon.
- **Then go deep**: Once intuition is in place, explain concepts, mechanics, and boundaries (e.g. how it works under the hood, when to use it, common pitfalls).
- **Pacing**: Prefer “working example or scenario first, then concepts”; one idea per paragraph, with clear breaks so the text doesn’t feel cramped.
- **Verifiable**: If code is involved, examples should be runnable on their own;

## Thinking

Before writing, clarify two things:

1. **What the author wants to say**  
   What is the real goal? To resolve confusion (“what’s the difference between coroutines and threads?”), to onboard (“Python async for devs from another language”), or to be practical (“how to write working asyncio code”)? The tutorial’s focus and level of detail should follow this.

2. **Reader experience**  
   Who is the audience (e.g. programmers with little Python experience)? Where will they get stuck (concepts, setup, or syntax)? What do they dislike (length, repetition, no examples, unexplained terms)? Use this to decide depth, number of examples, and whether to add comparisons (e.g. Python vs Java) or “code first, then concepts.”

**Principle**: Prefer explaining fewer points clearly and in order over covering everything in a vague or repetitive way.

## Guidelines

1. **Be concise; avoid repetition**  
   Explain each idea once, in one place. Do not restate the same point in a “summary” at the end of each section, or rephrase the same thing in multiple ways. Aim to **get it right in one go**.

2. **Markdown output: clear and minimal**  
   Use Markdown consistently: clear headings, lists, tables, and code blocks.  
   Avoid excessive horizontal rules (`---`), decorative symbols, or empty subheadings. Use language tags on code blocks and add short comments only where they help.

3. **Terminology and tone**  
   When introducing technical terms (e.g. `async`/`await`, event loop), use “one clear sentence first, expand only if needed.” If the reader says something is hard to follow, rewrite that part rather than adding another paragraph of explanation.

## Workflow

### 1. Understand the domain and guide the author

Before drafting the tutorial:

- **Understand the domain**: core concepts, common questions, and easy-to-mix-up points (e.g. coroutines vs threads, what the event loop is).
- **Use questions to guide** the person using this skill to state:
  - The exact topic or concept they want to cover;
  - The target reader (background, experience);
  - Specific questions they want answered or aspects they want to emphasize;
  - Preferences on length, style, and number of examples (e.g. “lots of runnable examples,” “code first, then concepts”).

Do not start writing a long draft without enough intent and audience information. A short outline or list of questions is fine first; expand after the author responds.

### 2. Gather sources

After the writing direction and focus are clear:

- **Search** for material on the topic. Prefer:
  - Official documentation, standards, and authoritative manuals;
  - Official READMEs and design docs of well-known projects;
  - Recognized tech blogs or books (sources can be cited briefly).
- **Do not treat as authoritative**:
  - Unattributed or unverifiable articles from content farms or low-quality aggregators;
  - Obvious copy-paste, outdated, or documentation-contradicting tutorials.

If a document is used, a brief note in or at the end of the tutorial is enough (e.g. “See the official Python asyncio docs”); no need for line-by-line citations.

### 3. Write the tutorial

With topic, audience, focus, and sources in place:

- Follow the **core design**: easy then deep, concrete then abstract, code then concepts when applicable, clear paragraphs.
- Align with **thinking**: keep the author’s goal and the reader’s sticking points in mind; adjust detail and length accordingly.
- Stick to the **guidelines**: no repetition, no verbosity, clean and minimal Markdown.

