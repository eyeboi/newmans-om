# Newman's OM — website

The website for **Newman's OM**, a home bakery in Jacaranda Cay, FL making
small-batch sourdough and handmade pasta.

- **Live site:** https://newmansom.com
- **Code lives at:** https://github.com/eyeboi/newmans-om

---

## Who's who

| | |
|---|---|
| **Paul Newman** | The baker. Bakes everything at home. Newman's OM is Paul's bakery. |
| **Freddi Newman** | Paul's sibling. Handles **delivery** of orders, and co-runs this website. |
| **David Taylor Gonzalez** | Freddi's co-worker. Built the site and helps maintain it. |

Both Freddi and David are collaborators on the GitHub repo, so either can
make changes at any time.

## How the whole thing is wired up

- **Domain** (`newmansom.com`) was purchased on **GoDaddy**. The DNS there
  points at GitHub Pages. The `CNAME` file in this folder is what tells
  GitHub the site answers to that domain — **don't delete it.**
- **Hosting** is **GitHub Pages**, serving the `main` branch straight from
  the root of this repo. There is no build step and no server.
- **Publishing** is automatic: when a change is saved to `main`, GitHub
  Pages redeploys. It usually takes **1–2 minutes** to show up. If you don't
  see your change, hard-refresh (Cmd+Shift+R).
- **Orders come in by text** (or Zelle/Venmo contact) — the site takes no
  payment. Paul or Freddi confirms the details and total over text.
- **The online order form is currently turned off.** It still exists in
  `index.html`, just commented out, and can be switched back on by deleting
  two marker lines (search `OPEN-COMMENT`). When it's on, submissions are
  emailed via a free service called [Web3Forms](https://web3forms.com).
- **Payments** happen off-site: Zelle or Venmo, arranged over text.

## The files in this folder

| File | What it is |
|---|---|
| `index.html` | **The entire website.** All the text, prices, and styling are in this one file. |
| `assets/` | Images: hero photo, schnauzer logo, and the link-preview image. |
| `CNAME` | Tells GitHub Pages the site is `newmansom.com`. Leave it alone. |
| `README.md` | This file. |
| `AGENTS.md` | Instructions for AI assistants (Codex, Claude) working on this repo. |

---

## Making changes (no coding required)

The easiest way is to **ask your AI assistant in plain English.** Open this
project in the Codex app and just say what you want:

> "Change the price of the Rye loaf to $11."
>
> "Add a new signature flavor called Everything Bagel for $12, ingredients are
> filtered water, bread flour, whole wheat flour, everything bagel seasoning, salt."
>
> "Take Pumpernickel off the menu for now."
>
> "Change the order cutoff from 9 AM to 10 AM everywhere it appears."
>
> "The phone number changed to 954-555-0000, update it everywhere."

The assistant knows the house rules (they're in `AGENTS.md`) and will make
the edit **and publish it to the live site** for you.

### If you want to poke at it yourself

Open `index.html` and search for `[EDIT]`. Every section that you'd
reasonably want to change is labeled with a comment explaining what it
controls and what to watch out for. For example, searching `[EDIT] MENU
CLASSICS` lands you right on the classic loaves.

Anything wrapped in `<!-- ... -->` is a note to you and never shows up on
the actual website.

### Two things that bite people

1. **The phone number and Venmo handle appear in more than one place.** If
   you change one, change them all, or the site will contradict itself.
   Easiest fix: ask the assistant to "update it everywhere."
2. **The 50% off promo is in three places** — the scrolling banner, the big
   promo box, and a checkbox on the order form. If the offer ends, all three
   need to go.

## If something breaks

Nothing you do here can break the bakery, and every previous version of the
site is saved in GitHub's history. If a change goes wrong, ask the assistant
to **"undo the last change and republish"** and it'll roll back.
