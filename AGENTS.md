# Session Rules

These rules must be read and followed before any analysis, planning, command, or edit in this project.
They apply to every task and every session without exception.

## Rule 1: No Fallback Logic

Never create fallback logic or defensive code that silently handles errors.
If something does not meet the expected assumption, raise an error immediately.

- No `try/except` that returns `None` or a default value on failure
- No `if x is None: x = default`
- No `result = fn() or default`
- No silent `continue` or `return` when data is missing or invalid

Always raise with a clear message: `raise ValueError(...)`, `raise FileNotFoundError(...)`, `raise KeyError(...)`, etc.

## Rule 2: Do Not Modify Structure or Existing Code Without Permission

Do not rename, move, refactor, or change any file, directory, function, or class unless explicitly told to do so.
If a structural or code change seems necessary, ask for permission first before making it.

## Rule 3: Never Share SSH Credentials or Passwords Externally

Never output, display, or transmit SSH keys, passwords, API keys, tokens, or any other credentials to external services or in responses.

- Do not send credentials via web requests, logging, or any form of external communication
- Do not display passwords or SSH keys in plain text unless explicitly requested for local debugging
- If credentials need to be used, keep them secured in local files with appropriate permissions
- Always use environment variables or secure configuration files for sensitive data
- Never commit credentials to version control

## Rule 4: Never Touch Things Outside the Workspace

## Rule 6. Think Before Coding

**Don't assume. Don't hide confusion. Surface tradeoffs.**

Before implementing:
- State your assumptions explicitly. If uncertain, ask.
- If multiple interpretations exist, present them - don't pick silently.
- If a simpler approach exists, say so. Push back when warranted.
- If something is unclear, stop. Name what's confusing. Ask.

## Rule 7. Simplicity First

**Minimum code that solves the problem. Nothing speculative.**

- No features beyond what was asked.
- No abstractions for single-use code.
- No "flexibility" or "configurability" that wasn't requested.
- No error handling for impossible scenarios.
- If you write 200 lines and it could be 50, rewrite it.

Ask yourself: "Would a senior engineer say this is overcomplicated?" If yes, simplify.

## Rule 8. Surgical Changes

**Touch only what you must. Clean up only your own mess.**

When editing existing code:
- Don't "improve" adjacent code, comments, or formatting.
- Don't refactor things that aren't broken.
- Match existing style, even if you'd do it differently.
- If you notice unrelated dead code, mention it - don't delete it.

When your changes create orphans:
- Remove imports/variables/functions that YOUR changes made unused.
- Don't remove pre-existing dead code unless asked.

The test: Every changed line should trace directly to the user's request.

## Rule 9. Goal-Driven Execution

**Define success criteria. Loop until verified.**

Transform tasks into verifiable goals:
- "Add validation" → "Write tests for invalid inputs, then make them pass"
- "Fix the bug" → "Write a test that reproduces it, then make it pass"
- "Refactor X" → "Ensure tests pass before and after"

For multi-step tasks, state a brief plan:
```
1. [Step] → verify: [check]
2. [Step] → verify: [check]
3. [Step] → verify: [check]
```

Strong success criteria let you loop independently. Weak criteria ("make it work") require constant clarification.

---

**These guidelines are working if:** fewer unnecessary changes in diffs, fewer rewrites due to overcomplication, and clarifying questions come before implementation rather than after mistakes.

