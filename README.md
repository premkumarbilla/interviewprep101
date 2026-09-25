# Interview Prep 101

Free, no-sign-up checklists for software engineering interview prep. Progress is saved in each visitor's browser, and there's no backend.

Live site: https://premkumarbilla.github.io/interviewprep101/

| Path | What it is |
|---|---|
| `index.html` | Home page, with links to each track and your System Design progress |
| `system-design/index.html` | System Design Interview Reading Tracker (Alex Xu, Vol. 1 and 2, 457 references) |
| `coding/index.html` | Coding tracker (coming soon) |
| `og-image.png`, `system-design/og-image.png` | Preview images shown when a link is shared |
| `sitemap.xml` | Lists the pages for search engines. Submit it in Google Search Console. |

## Publishing

This repo is published with GitHub Pages (Settings → Pages → Deploy from a branch → `main` / `(root)`). Changes go live a minute or two after each commit.

## Updating the System Design lists

The reference data is the `DATA` object in the `<script>` block in `system-design/index.html`. The lists are also written into the HTML for search engines, so when you change a reference, update it in both places.

Progress is stored by position (`v1-ch4-3` means Volume 1, Chapter 4, reference 3). Add new references at the end of a chapter so saved progress stays correct.

If the site address changes, update the URLs in each page's `<head>` tags and in `sitemap.xml`.

## How progress is stored

Progress is saved in `localStorage` under the key `sdi-tracker`. It is never sent anywhere. It stays with one browser on one device, and visitors can move it with Export and Import on the tracker.

## Credit

The System Design reference lists come from the author's public repository, [alex-xu-system/bytebytego](https://github.com/alex-xu-system/bytebytego). This is an unofficial study aid and is not affiliated with Alex Xu, Sahn Lam or ByteByteGo.
