# System Design Interview Reading Tracker

A single-page checklist of every reference in *System Design Interview: An Insider's Guide*, Volumes 1 and 2. Readers tick off what they've read, and their progress is saved in their own browser. There are no accounts and no backend.

Everything is in `index.html`. It has no build step and needs no server code.

## Publish on GitHub Pages (free)

1. Create a new public repository on GitHub, for example `sdi-reading-tracker`.
2. Upload `index.html` and this `README.md` to the repository root. Use **Add file → Upload files**, then commit.
3. Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch* and **Branch** to `main`, with the folder set to `/ (root)`. Click **Save**.
4. After a minute or two, the site is live at `https://<your-username>.github.io/sdi-reading-tracker/`.

To use your own domain, add it under **Settings → Pages → Custom domain** and follow GitHub's DNS instructions.

## Publish on Netlify or Cloudflare Pages (free)

- **Netlify:** go to app.netlify.com/drop and drag the folder containing `index.html` onto the page.
- **Cloudflare Pages:** go to Workers & Pages → Create → Pages → *Upload assets*, then upload the folder.

## Updating the lists

The reference data is the `DATA` object near the top of the `<script>` block in `index.html`. Each reference is a `[title, url]` pair, and `url` is `null` for print-only citations.

Progress is stored by position (`v1-ch4-3` means Volume 1, Chapter 4, reference 3). If you insert or remove a reference in the middle of a chapter, the saved ticks for later items in that chapter shift. Add new items at the end of a chapter to avoid this.

## How progress is stored

- Progress is saved in the visitor's browser (`localStorage`, key `sdi-tracker`). It is never sent to a server.
- It stays on one device and browser. **Export progress** gives a code or `.json` file, and **Import progress** merges it on another device.
- Clearing site data or using a private window erases progress.

## Credit

The reference lists come from the author's public repository, [alex-xu-system/bytebytego](https://github.com/alex-xu-system/bytebytego). This is an unofficial study aid and is not affiliated with Alex Xu, Sahn Lam or ByteByteGo. Consider asking the author before promoting it widely.
