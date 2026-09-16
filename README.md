# Personal homepage — deployment

The address printed on the OCEANS 2026 poster is **`https://winnieissleepingzzz.github.io/`**.
Once the poster is printed that address cannot change, so the repository name below
is not optional.

## One-time setup

1. On GitHub, create a **public** repository named exactly `WinnieIsSleepingzzZ.github.io`
   (the repo name must match the account name — that is what makes it a user site
   served at the bare domain rather than a project subpath).
2. Push the contents of this folder to its default branch:

   ```
   cd E:\beach_litter\homepage
   git init
   git add .
   git commit -m "Personal homepage"
   git branch -M main
   git remote add origin https://github.com/WinnieIsSleepingzzZ/WinnieIsSleepingzzZ.github.io.git
   git push -u origin main
   ```

3. Repository → Settings → Pages → Source: **Deploy from a branch**, branch `main`,
   folder `/ (root)`. First build takes 1–2 minutes.
4. Open `https://winnieissleepingzzz.github.io/` and scan the poster QR with a phone to
   confirm end to end.

Afterwards, editing is just: change `index.html`, commit, push. The address never
moves, so the printed code keeps working.

## Files

| Path | What |
|---|---|
| `index.html` | The whole site. Self-contained — no build step, no dependencies. |
| `assets/PLAS-Net_OCEANS2026_paper.pdf` | Conference paper (3.2 MB) |
| `assets/PLAS-Net_OCEANS2026_poster.pdf` | Poster, 72 × 48 in (3.6 MB) |
| `portrait.jpg` | **Not present.** Add a square headshot, or the page hides the slot. |
| `cv.pdf` | **Not present.** Add it, or delete the CV link in `index.html`. |

## Still to fill in

Search `index.html` for `TODO` — there are three:

- **Google Scholar** — the profile URL
- **ORCID** — the iD
- **Sample dataset link** — see below

Also confirm: the page says *Department of Ocean Technology, Policy, and Environment*
and *Doctoral student*. Both were inferred from the paper's affiliation line and from
the JST SPRING fellowship; correct them if wrong.

## The dataset does not go in this repository

`opensource_package/PLAS-Net_sample_dataset.zip` is **283 MB**. GitHub rejects files
over 100 MB on a normal push, so it cannot live here.

Two options, in order of preference:

1. **Zenodo** — upload the zip, get a DOI. The dataset becomes independently citable,
   the record is permanent, and it is what a reviewer expects. Then point the
   "Sample dataset" button at the DOI.
2. **GitHub Release** — attach the zip as a release asset on this repo (2 GB limit
   for release assets, unlike repository files). Faster, but no DOI.

Either way the poster is unaffected: the QR points at this page, and this page points
at the dataset. That indirection is the reason the QR does not point at the dataset
directly.
