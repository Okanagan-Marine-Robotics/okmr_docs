# Inbox

Drop raw documentation here and push. An AI sorts it into the vault and opens a pull request for someone to check.

**Accepted:** PDF, PNG, JPG, WEBP, HEIC (phone photos), .docx, .md, .txt, .csv

**From Google Docs:** *File → Download → PDF* (keeps images and tables) and drop the PDF here.

**How to drop files**
- In Obsidian: drag files into this folder, then *Obsidian Git: Commit and sync*.
- On GitHub: open `_inbox/` → *Add file → Upload files* → commit.

**Tips for good results**
- Add a short `.md` or `.txt` note with the files saying what they are, e.g. "BMS rev B bring-up, 2026-11-20, Amber".
- Photos: shoot straight on, in good light, one board/page per photo.
- Up to ~15 MB per drop.

**What happens next**
1. The *AI intake* workflow reads everything, adds to existing pages or creates new ones from the templates, and moves your originals into an `attachments/` folder next to the page they fed.
2. It opens a PR listing every change and anything it couldn't read or place.
3. Someone checks the numbers against the originals and merges.

Files it can't handle end up in `_inbox/unsorted/` and are listed in the PR.

Don't drop anything private. The free Gemini tier lets Google use the uploaded content, and this repo is public anyway.
