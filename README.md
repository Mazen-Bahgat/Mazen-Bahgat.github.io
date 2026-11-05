# Mazen Bahgat Portfolio

Interactive portfolio site: 18 projects charted from embedded firmware to the cloud, with layer filters, search and expandable project details.

It is one static page (`index.html`) with no build step, so it runs directly on GitHub Pages.

## Files

| Path | What it is |
|---|---|
| `index.html` | The whole site: content, styles and scripts |
| `cv/Mazen_Bahgat_CV_DevOps.pdf` | DevOps CV, linked from the "Download DevOps CV" button |
| `cv/Mazen_Bahgat_CV_AI_Engineer.pdf` | AI Engineer CV |
| `cv/Mazen_Bahgat_Portfolio.pdf` | Printable portfolio, linked in the footer |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

## Publish on GitHub Pages

1. On GitHub, create a new **public** repository named exactly `Mazen-Bahgat.github.io`.
2. Choose **Add file → Upload files** and drag in everything from this folder, including the `cv` folder and `.nojekyll`. Commit.
3. Open **Settings → Pages**. Under *Build and deployment*, set *Source* to **Deploy from a branch**, branch **main**, folder **/ (root)**, then save.
4. After a minute or two the site is live at **https://mazen-bahgat.github.io**.

Then add that link to your LinkedIn profile, your GitHub profile README, and the "Portfolio" line in both CVs.

## Updating content

All project, experience and certification text is in the `P`, `EXP` and `CERTS` arrays near the top of the `<script>` in `index.html`.

- **Add a project:** add an object to `P` in date order (oldest first). Its `layers` list decides which rows of the chart it fills: `cloud`, `ai`, `app`, `control`, `embedded`. Set `featured:true` to tag it as featured.
- **Replace a CV:** upload the new PDF to `cv/` with the same file name.
- Each project has a shareable link, for example `https://mazen-bahgat.github.io/#herhealthgpt`.
