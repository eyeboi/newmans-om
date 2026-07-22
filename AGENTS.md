# Working agreement

## What this project is

The website for **Newman's OM**, a home bakery in Jacaranda Cay, FL selling
small-batch sourdough and handmade pasta. It is a new and growing business.

**People:**

- **Paul Newman** — the baker. Bakes everything at home. It's their bakery.
- **Freddi Newman** — Paul's sibling. **Delivers** completed orders, and is a
  collaborator on this repo.
- **David Taylor Gonzalez** — Freddi's co-worker. Built the site, also a
  collaborator.

**How orders actually work:** customer texts (or submits the web form) before
9 AM → Paul bakes overnight (24h ferment) → customer picks up in Jacaranda
Cay, **or Freddi delivers**. No payment is taken on the website; Paul or
Freddi texts back to confirm the order and total, and payment happens over
Zelle or Venmo.

**Infrastructure:**

- Domain `newmansom.com` registered on **GoDaddy**, DNS pointed at GitHub Pages.
- Hosted by **GitHub Pages** from `main` at the repo root. No build step.
- Repo: `https://github.com/eyeboi/newmans-om`.
- The `CNAME` file binds the custom domain. Never delete or rename it.
- **The online order form is disabled** (commented out in `index.html` as of
  2026-07-22, to be revisited). Re-enable by deleting the `OPEN-COMMENT` and
  `CLOSE-COMMENT` marker lines. Its CSS and JS were deliberately left intact;
  the JS is null-guarded and no-ops while the form is off. When live, it posts
  to **Web3Forms** and the `access_key` determines the destination inbox.
- The whole site is a single self-contained `index.html` plus `assets/`.

## Who you're talking to

**Neither collaborator is comfortable with Git, GitHub, or code.** Freddi
works through the Codex app and does not code at all. Handle the entire Git
workflow for them and explain outcomes in plain language. Never ask them to
resolve a merge conflict, pick a branch, or interpret a diff.

Because two people edit this repo independently, **always pull/fetch before
starting an edit** so you're not working from a stale copy.

## Publishing changes

- When the user asks to change the website, treat publishing that completed
  change to the live site as part of the request, unless they explicitly ask
  for a preview, draft, or local-only change.
- Before publishing, inspect the diff and run proportionate checks. Never
  include unrelated user changes in a commit.
- Commit only the intended files and push directly to `origin/main` so GitHub
  Pages deploys. Do not make the user manage branches, commits, pull requests,
  or deployments unless access controls require it.
- After pushing, monitor the deployment until it succeeds and verify the
  public site when practical. Report plainly whether the change is live; do
  not claim it is live merely because the push succeeded.
- If validation, push, or deployment fails, preserve the work, explain the
  problem simply, and keep troubleshooting when it is safe to do so.
- Never force-push, rewrite shared history, expose credentials, or bypass
  repository protections.

## Editing `index.html`

Editable regions are marked with `<!-- [EDIT] ... -->` comments. Keep those
markers accurate when you restructure anything, and add new ones for any new
section a non-coder would plausibly want to change.

**Content that is duplicated — change every copy or the site contradicts itself:**

- **Phone number `954-598-3667`** appears in the CONTACT chips and the FOOTER,
  and each occurrence has three parts: visible text, the `href="sms:+1..."`,
  and the `aria-label`.
- **Venmo `@naul_pewman`** appears in CONTACT and FOOTER.
- **The 50% off first-order promo** appears in the MARQUEE, the PROMO box, and
  as a checkbox in the ORDER FORM.
- **The 9 AM cutoff** appears in ORDER STEPS and in the order form intro.

## House style

- The voice is warm, plainspoken, and a little wry ("baked everyday, baked for
  you"; "quality control handled by the resident schnauzer"). Match it.
- Visual identity: pink/cream palette with Fraunces display type. Design tokens
  are CSS variables in `:root` — reuse them rather than hardcoding new colors.
- Prices display as whole dollars (`$8`, `$10 / lb`). `$MP` means market price.
- Keep the site a single dependency-free HTML file. Do not introduce a build
  step, framework, or npm without the user explicitly asking.
- Preserve accessibility: keep `alt` text, `aria-label`s, and label/input
  associations intact on anything you touch.
