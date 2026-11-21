# Contributing to okmr_docs

## Workflow
1. Pull before you start (Obsidian Git: *Pull* from the command palette, or turn on *Pull on startup*).
2. Make a branch for anything bigger than a typo.
3. Commit with a real message (`BMS: add CAN telemetry table`), push, open a PR.
4. Someone from the affected subteam reviews. Interface changes need a reviewer from **both** sides of the link.

### Obsidian Git settings (per person, not committed)
- Pull on startup: **on**
- Auto commit-and-sync interval: **0 (off)**. Auto-commits to a shared repo create noise and merge conflicts.
- Pull before push: **on**

## Don't want to write it up yourself?
Drop your Google Doc (exported as PDF), photos, or notes into `_inbox/` and push. The **AI intake** workflow sorts them into the right pages and opens a PR. See [_inbox/README.md](_inbox/README.md). Whoever reviews that PR checks the numbers against the originals before merging.

## Where things go
| You're writing… | Put it in | Template |
| --------------- | --------- | -------- |
| A board, subsystem or task | `Systems/<Name>/<Name>.md` | System |
| A link between two things (UART, CAN, Ethernet, connector pinout) | `Interfaces/` | Interface |
| Why we chose X over Y | `Decisions/NNNN Title.md` (next number) | Decision |
| Bring-up, bench, pool or sim results | `Systems/<Name>/` next to the system, or `Test Plans/` for whole-sub tests | Test Report |

Insert a template with the command palette → *Templates: Insert template*.

## Conventions
- **One fact, one place.** Link to the page that owns a fact instead of copying it. Pinouts live on the interface page, not on both boards' pages.
- **Name files after what they are**, not `index.md`, so search and tabs stay readable.
- **Fill in the properties** at the top of each page. `Tracker.base` builds its tables from them.
  - System `status`: `concept` → `design` → `fab` → `bring-up` → `integrated` → `retired`
  - Interface / decision `status`: `draft` / `proposed` → `accepted` → `superseded`
  - Test report `result`: `pass` / `fail` / `partial`
- **Links** are standard Markdown with relative paths (the vault is set up to do this), so they also work on GitHub.
- **Diagrams**: use Mermaid code blocks. They render in both Obsidian and GitHub and diff cleanly. Canvas files only render in Obsidian.
- **Warnings**: use callouts (`> [!warning]`). GitHub renders them too.

## Files and images
- Images go in an `attachments/` folder next to the page (automatic when you paste). Compress screenshots; keep files under ~1 MB.
- **Don't commit Altium or KiCad projects here.** They live in the OKMR Altium 365 workspace / their own repos. Link to them and attach a PDF schematic export for each released rev.
- Datasheets: link to the manufacturer URL, don't commit the PDF.
