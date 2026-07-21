# Working agreement

The user is not comfortable with Git or GitHub terminology. Handle the Git workflow for them and explain outcomes in plain language.

## Publishing changes

- The official site is `https://newmansom.com/`.
- It is hosted by GitHub Pages from the repository's `main` branch at the repository root.
- When the user asks to change the website, treat publishing that completed change to the official site as part of the request unless they explicitly ask for a preview, draft, or local-only change.
- Before publishing, inspect the diff and run proportionate checks. Never include unrelated user changes in a commit.
- For a finished website edit, commit only the intended files and push directly to `origin/main` so GitHub Pages deploys it. Do not make the user manage branches, commits, pull requests, or deployment unless access controls require it.
- After pushing, monitor the GitHub Pages deployment until it succeeds. If practical, verify the public site. Report plainly whether the change is live; do not claim it is live merely because the push succeeded.
- If validation, push, or deployment fails, preserve the work, explain the problem simply, and continue troubleshooting when it is safe to do so.
- Never force-push, rewrite shared history, expose credentials, or bypass repository protections.
