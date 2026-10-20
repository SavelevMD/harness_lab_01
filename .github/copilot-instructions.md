# Project conventions for Copilot

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