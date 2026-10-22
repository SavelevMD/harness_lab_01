# Project conventions for Copilot

## Purpose

Use this repository to practice agentic AI developer workflows:

- Plan before acting.
- Keep changes small and reviewable.
- Treat GitHub as the system of record.
- Record durable artifacts for traceability.

## Operating model

- Use Plan → Act → Evaluate for non-trivial tasks.
- Separate planning from execution.
- Prefer pull requests over direct pushes.
- Ask for human review before irreversible or high-risk changes.
- Use least-privilege workflow permissions.

## Code style
- Prefer explicit access modifiers (public, private, internal, protected) on all type members.
- Use async/await throughout — never block on .Result or .Wait(), and avoid .GetAwaiter().GetResult() outside of Main.
- One assertion per test.
- Prefer var only when the type is obvious from the right-hand side.
- Use file-scoped namespaces unless the file needs multiple namespaces.

## Pull request etiquette
- Title format: <area>: <imperative summary> (e.g., auth: rotate session token on login).
- PR body must include a "Why" section before any "What" section.
- Link an issue or skip linking entirely — don't fake-link.

## Tools to avoid
- Do not call external network APIs unless explicitly listed in `.github/mcp-allowlist.yml`.
- Do not introduce new NuGet packages without approval from a maintainer.

## Memory and context rules

- Treat this file as repo-level long-term memory.
- Do not assume stale context is still correct.
- Prefer current repository files, workflow logs, and PR comments over memory.
- Remove obsolete instructions instead of layering conflicting guidance.

## Output expectations

- Explain assumptions.
- Include verification steps.
- Link changes to issues or PR comments when possible.
- Never include secrets in code, logs, or artifacts.