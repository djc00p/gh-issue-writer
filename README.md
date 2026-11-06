# ⚡ gh-issue-writer

[![ClawHub Skill](https://img.shields.io/badge/ClawHub-Skill-blue)](https://clawhub.ai/djc00p/gh-issue-writer) [![Agent Skill](https://img.shields.io/badge/Agent-Skill-blue)](#) [![GitHub Issues](https://img.shields.io/badge/GitHub-Issues-181717.svg)](https://github.com/features/issues) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**gh-issue-writer** drafts clear, actionable GitHub issues from a brief description, an error message, or a raw idea.

The difference between an issue that gets fixed and one that gets closed as "not enough info" is almost always structure. A stack trace pasted at the top of a blank body is a request for clarification. An issue with reproduction steps, expected vs. actual behavior, and environment details is a ticket someone can pick up today.

---

## 🎯 When to Use

* *"Write a GitHub issue"*
* *"Open an issue for..."*
* *"File a bug"*
* *"Create a feature request"*
* Any description of a problem that needs to be tracked

---

## 📝 Step 1 — Understand the Input

Ask (or infer from context):

1. **What type of issue?** — Bug · Feature Request · Enhancement · Task · Question
2. **What repo?** — detect from `git remote get-url origin` if you're in a git dir, otherwise ask
3. **What happened / what's wanted?** — the raw description, error, or idea
4. **Optional** — labels, assignee, milestone, environment details

> If the user gave you enough context, **proceed without asking** — draft it and show for confirmation.

---

## 📋 Step 2 — Draft the Issue

Use the appropriate template. Fill every field; omit sections only if genuinely not applicable.

### Bug Report

```markdown
## Description
<!-- Clear, one-paragraph summary of the problem. -->

## Steps to Reproduce
1.
2.
3.

## Expected Behavior
<!-- What should have happened? -->

## Actual Behavior
<!-- What actually happened? Include error messages verbatim. -->

## Environment
- OS:
- Browser / Runtime / Version:
- Relevant config or dependencies:

## Logs / Screenshots
<!-- Paste relevant logs, stack traces, or attach screenshots. -->

## Additional Context
<!-- Related issues, recent changes, workarounds tried. -->
```

### Feature Request

```markdown
## Problem
<!-- What pain point does this solve? Who has it? -->

## Proposed Solution
<!-- What should the feature do? -->

## Alternatives Considered
<!-- What other approaches did you think about? -->

## Use Cases
<!-- Who would use this, and how? -->

## Additional Context
```

---

## 🚀 Step 3 — Submit (Optional)

With the `gh` CLI authenticated, the issue can be filed directly:

```bash
gh issue create --title "..." --body "..." --label bug --label "needs triage"
```

Otherwise, the drafted markdown is ready to paste into the GitHub web UI.

---

## 💡 Why Structure Matters

| Weak issue | Strong issue |
|------------|-------------|
| "It's broken" | One-line problem summary + reproduction steps |
| "Doesn't work on mobile" | Expected vs. actual behavior + viewport + browser version |
| "Add dark mode" | Problem statement + proposed solution + alternatives + use cases |
| Pasted stack trace only | Reproduction steps + environment + the trace |

---

## 📚 References

* `references/templates.md` — full templates for every issue type
* `references/cli.md` — `gh` CLI flags, label conventions, and bulk operations

---

**Published by [@djc00p](https://github.com/djc00p)**
