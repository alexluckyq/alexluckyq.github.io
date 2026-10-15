---
title: "The AI awareness gap: a practical lens for engineers"
date: 2026-10-15T09:00:00-04:00
description: "Beyond impressive demos: evaluate AI on real engineering work, with clear constraints and evidence you can review."
summary: "People experience very different versions of AI. For engineers, the useful question is what a tool can deliver on a real task—and how we verify it."
author: Alex Qin
---

A recent [BigGo Finance article on AI awareness](https://finance.biggo.com/news/6e74d8f8-0a20-47b5-9ffe-f8a45cd33264) describes a four-tier model attributed to Andrej Karpathy: people with little exposure to AI, occasional chatbot users, professionals using advanced agents, and insiders with access to research systems.

Its useful premise is that people can have very different impressions of AI because they encounter different tools, tasks, and levels of access. The article presents its population figures as rough estimates. They should not be read as a measured census, and this post does not independently verify its claims about internal lab capabilities or incidents.

For software engineers, that framing suggests a more practical discussion: **what can a tool accomplish in our codebase, under our constraints, with results we can actually check?**

## Start with a real task

An isolated demo is a limited basis for choosing a development workflow. A useful evaluation starts with a bounded piece of work: explain an unfamiliar module, propose a refactor, reproduce a bug, or implement a small feature.

For an Android project, a trial task might be updating a screen while preserving its loading, empty, and error states. Give the tool the relevant architecture, supported devices, and acceptance criteria. Then assess the resulting change as you would any contribution to the project.

That produces more useful evidence than either an impressive screenshot or a single failed answer.

## Make verification part of the work

A proposed evaluation loop is straightforward:

1. **Define the outcome.** Describe the behavior that should change and the behavior that must remain intact.
2. **Constrain the change.** Identify the relevant modules, interfaces, and platform requirements.
3. **Request evidence.** Ask for a build result, appropriate tests, and a concise explanation of important decisions.
4. **Review the result.** Read the diff and exercise the affected experience, including failure paths.
5. **Measure the whole effort.** Include review, corrections, and integration time when judging whether the tool helped.

Passing checks is useful evidence, but it is only part of the picture. A feature also needs to fit the product and remain understandable to the next engineer.

## Bring device behavior into the evaluation

Android and XR work provides a concrete way to think about those limits. A change can look convincing in source code while still needing careful evaluation on the target device.

For a phone-to-headset experience, an acceptance checklist could include interrupted connections, app lifecycle transitions, input differences, and recovery after an error. The point is to make those expectations explicit before implementation, so the review has something concrete to judge.

This is also where engineering experience remains valuable: deciding which constraints matter, identifying missing cases, and choosing what evidence is sufficient for release.

## Build a shared understanding through examples

Teams do not need identical opinions about AI to evaluate it productively. They need shared tasks and a consistent review process.

A small collection of representative changes, recorded with their constraints, results, and required corrections, would make a useful internal reference. It can expose both valuable capabilities and recurring weaknesses without turning either into a universal claim.

The article's awareness-gap framing is a starting point for that conversation. The next step is grounded engineering: choose meaningful work, inspect the outcome, and update the workflow based on what the evidence supports.

---

*Source: [BigGo Finance's article on the four-tier AI awareness funnel](https://finance.biggo.com/news/6e74d8f8-0a20-47b5-9ffe-f8a45cd33264), accessed October 15, 2026. The engineering evaluation approach above is commentary inspired by the article, not a report of a benchmark or a claim about an employer's internal practices.*
