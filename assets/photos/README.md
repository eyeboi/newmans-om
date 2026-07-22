# Photos

**These are AI-generated placeholder images**, made to give the site the right
look until real photos of Paul's actual bread are available. They are not
photographs of real Newman's OM products.

The big hero image at the top of the page lives one folder up as
`assets/hero_marble.jpg` (alternate: `assets/hero_blossom.jpg`), and is also
AI-generated. It replaced an earlier hero of unknown origin. Its composition
deliberately keeps the middle of the frame empty so the headline stays
readable — if you swap it, pick something with a calm center, and re-check the
mobile crop position set in `index.html` near the `max-width:640px` rule.

**Replacing one with a real photo** is the goal. To swap:

1. Drop the new photo into this folder.
2. In `index.html`, search for `[EDIT] PHOTO` and change the `src` to the new
   filename.
3. Update the `alt` text to describe what's actually in the new picture, and
   update `width`/`height` to the new image's real pixel dimensions.

You can also just ask the assistant: *"replace the classics photo with
`my-new-loaf.jpg`"* and it will handle all three steps.

| File | Where it appears | Shows |
|---|---|---|
| `classics_01.jpg` | Banner above Classic Flavors | Three scored boules on a cooling rack |
| `sig_seeded_01.jpg` | Banner above Signature Flavors | Seeded loaf, one slice cut |
| `pasta_01.jpg` | Banner above Handmade Pasta | Fettuccine nests on a floured board |
| `craft_proof_01.jpg` | Photo strip, left | Dough proofing in a banneton |
| `craft_crumb_01.jpg` | Photo strip, middle | Macro of the open crumb |
| `craft_tools_01.jpg` | Photo strip, right | Lame, couche, and starter jar |

**Unused alternates** — ready to drop into the Signature banner if you'd
rather feature a different loaf. Swap the `src` and `alt` in `index.html`:

| File | Shows |
|---|---|
| `sig_frenchonion_01.jpg` | Caramelized onion and gruyère crumb (the house special) |
| `sig_chocolate_01.jpg` | Dark cocoa crumb with melting chocolate chips |

There was previously a butterfly pea blossom photo here. It was removed
because the AI-invented blue didn't match the loaf Paul actually bakes.
**Don't regenerate that one** — the color is too specific to guess at, so it
should wait for a real photograph.

## Notes for whoever swaps these

- **Banners** are cropped to a wide strip, so put the subject near the middle.
  Roughly 3:2 and at least 1500px wide works well.
- **Strip photos** are cropped square.
- Save as JPEG around 85% quality. Keep files under ~400KB so the page stays
  fast; the current ones are 150–350KB.
- Each image has a `.json` sidecar recording the prompt that generated it.
  Delete the sidecar when you replace the image with a real photo.

Once the menu shows real bread, update the accuracy note in `AGENTS.md`.
