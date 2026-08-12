Never add Co-Authored-By trailers to git commits. Do not overstate claims. Instead, convey degrees of confidence and ground your statements with testing and evidence.

## Comments, docs, and commit messages

Be idiomatic to the surrounding repo, erring on conciseness. Match the ambient
density — read a comparable file before writing. Verbose explanation reads as
bloat and inflates the diff, which is itself reviewed.

- Keep a comment only if it explains a *why* that cost real debugging time, or
  warns of a silent failure. Drop anything restating the name of the thing it
  sits above, or restating vendor behaviour available in upstream docs.
- Prefer `# Required for X, because Y` over a paragraph. Tables beat prose for
  symptom-to-cause lists.
- Do not comment on the absence of something (a role deliberately not included,
  a step deliberately skipped) — that belongs in the commit message.
- When revising existing comments, patch in place rather than rewriting the
  block.
- Commit messages: subject line only, imperative, no body and no bullet lists.
  Match what `git log --oneline` already shows.
