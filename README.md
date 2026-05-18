# Sats for Trash

> An honest, verifiable, replicable protocol for rewarding real-world positive action.

Natural spaces cleanup outings logged on Nostr, paid in sats. 

🔗 **Live page:** *www.satsfortrash.com*
📡 **Nostr hashtag:** `#sats4trash`

---

## What this is

A public log of natural spaces cleanup outings. For each outing:

1. Trash is collected and photographed
2. A note is posted on Nostr with the photo.
3. The outing is logged in a spreadsheet
4. If people think the action deserves value, they zap sats directly to the Nostr note.
5. All zaps received are logged transparently

No platform in the middle. No permission required. No extraction.

## How it works

The page reads two CSV feeds from a spreadsheet and renders them client-side:

- **Notes** — one row per outing
- **Zaps** — one row per zap event

Bags are converted to liters (1 bag = 10 L). Rankings combine total sats sent with a loyalty bonus that rewards repeat zapping.

## Stack

- Plain HTML, CSS, vanilla JavaScript — no framework, no build step
- Google Sheets as the database (public read-only CSV export)
- GitHub Pages for hosting
- Nostr for publishing outings, Lightning for receiving zaps

## Replicate it

The protocol is designed to be forked. To run your own version:

1. Fork this repository
2. Duplicate the Google Sheet template *(link coming soon)*
3. Update `SHEET_ID` in `index.html` to point to your own sheet
4. Replace `hero.png` with your own image
5. Adjust intro text and Lightning address to your context
6. Enable GitHub Pages on your fork
7. Post your first outing on Nostr with the `#sats4trash` hashtag

You don't need to be doing beach cleanups specifically. The protocol works for any honest, physical, repeatable action that can be documented and published on Nostr.

Trash is Cash is the first instance of the **Love-Only Verifiable Economy** — a pattern for connecting real-world positive action to direct economic reward, without intermediaries.

The three components:

- **Signal** — the action and its honest documentation
- **Medium** — Nostr + Lightning + a public ledger
- **Potential** — two environments improve simultaneously: the physical space and the protocol itself

Related: [Open Ring Project](https://www.openringproject.com) — the diagnostic framework this builds on.

## License

MIT — see [LICENSE](./LICENSE).

Use it, fork it, modify it, run your own version. Attribution appreciated but not required.
