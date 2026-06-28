# PHILOSOPHY.md

# Project Philosophy

This document describes the engineering philosophy shared by projects created from the AGIT Project Template.

It complements the Collaboration Model in `ChatGPT.md`. The Collaboration Model describes how work is coordinated. This document describes the engineering values behind that work.

---

# Simplicity

Prefer simple solutions over complex ones.

Complexity should only be introduced when it provides a clear and lasting benefit.

Readable solutions are generally preferred over clever solutions.

A simple validated solution is usually better than a sophisticated unvalidated one.

---

# Maintainability

Software is expected to be maintained long after its initial implementation.

Engineering decisions should therefore prioritize long-term maintainability over short-term convenience.

Projects should evolve gradually rather than through unnecessary rewrites.

A change is not complete when it merely works once. It should also be understandable, reviewable and possible to continue later.

Code should be written for maintainers and future contributors, not only for the assistant that produced it. If the implementation would require private chat history to understand, it is not maintainable enough.

---

# Transparency

Software should behave predictably.

Important assumptions, configuration options, limitations and architectural decisions should be documented.

Automation should never hide important behavior from the user.

When a project uses AI assistance, the repository should make that collaboration understandable instead of relying on private conversation history.


---

# Integrity

Integrity is more important than appearing helpful.

A project artifact should never be described as completed unless it actually exists and contains the stated work. A limitation should be made visible instead of being hidden behind confident language.

This applies to code, documentation, generated archives, commits, validation results and AI-assisted repository updates. Trustworthy collaboration depends on accurate statements about what was actually done.

Standard template artifacts should also be preserved with care. When a project inherits a required template element, such as the AI Collaboration Note in the README files, it should keep the required disclosure visible and factually accurate. Project-specific wording may be adapted when literal template text would be misleading.

---

# Documentation

Documentation is part of the software.

It should evolve together with the implementation and be maintained with the same level of care as source code.

Every document should have a clearly defined purpose and audience.

Avoid duplicating the same rule across many documents. Prefer one authoritative location and clear references from other documents.

Documentation should describe the actual state of the project, not an aspirational state that has not been implemented or validated.

Code comments should be purposeful and close to the relevant implementation. They should explain intent, constraints and trade-offs where those are not obvious from names and structure alone.

---

# Pragmatism

Engineering decisions should be guided by practical value.

Automation is encouraged where it improves consistency, reliability or maintainability.

Manual steps are acceptable whenever they improve safety, transparency or the overall engineering process.

The best process is the simplest process that preserves correctness, traceability and confidence.

---

# Validated Learning

Projects should reduce uncertainty through validation.

A proof of concept is successful when it produces reliable knowledge. That knowledge may confirm the intended design, or it may show that a different approach is needed.

Validated negative results are useful project knowledge. They should be documented when they influence architecture or roadmap decisions.

The goal is not to pursue every technically interesting path. The goal is to answer the questions that matter for the current roadmap.

---

# Roadmap Discipline

The roadmap should guide implementation.

Projects should establish an explicit initial roadmap before implementation accelerates.

A good roadmap does not need to be perfect or exhaustive. It should provide enough structure to keep work focused, explain why each milestone exists and make it clear what should be validated before moving on.

Technical exploration should support the active milestone rather than replace it.

Before continuing with additional experiments, ask whether the current milestone objective has already been satisfied.

This prevents projects from drifting into open-ended engineering work after the important question has already been answered.

---

# Collaborative Efficiency

Efficient collaboration is a quality attribute.

Small, validated steps reduce uncertainty and keep momentum high. A good process should make it easy for the maintainer to know what to decide, what to run, what to review and when to commit.

Numbered next steps, explicit validation expectations and clear commit summaries and descriptions are not ceremony. They are lightweight tools for reducing ambiguity and preserving confidence.

---

# Quality

Software quality is not measured solely by functionality.

A successful project is also:

- understandable
- maintainable
- reproducible
- well documented
- transparent
- validated
- easy to resume after a pause

A repository that cannot be continued confidently is not finished, even if the code appears to work.

---

# Repository-First Work

The repository is the durable project memory.

Chats, notes and experiments are useful, but the repository should contain the information needed to understand and continue the project.

Important outcomes should be reflected in one or more durable artifacts:

- code
- documentation
- changelog entries
- project context
- ADRs, where useful
- commit history

---

# Continuous Evolution

Projects are expected to improve continuously.

Successful engineering practices should be retained.

Unnecessary complexity should be removed whenever practical.

The goal is steady evolution rather than constant reinvention.

The AGIT Project Template itself evolves through retrospectives based on real project experience.

---

# Versioning

Projects should follow Semantic Versioning.

Version numbers communicate the significance of completed project states rather than simply counting commits.

- Patch versions contain compatible fixes and minor improvements.
- Minor versions introduce new functionality while maintaining compatibility.
- Major versions indicate intentional breaking changes or significant architectural evolution.

Version tags identify meaningful completed repository states.

GitHub Releases communicate selected user-facing milestones.

Not every tag requires a GitHub Release.

Version tags and releases should be created intentionally rather than automatically.

---

# Final Principle

Well-designed software should communicate its quality through clarity, consistency and technical accuracy rather than persuasive language.
