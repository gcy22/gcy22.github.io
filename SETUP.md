# Your al-folio Homepage — Setup & Deployment

This is a personal homepage built from [alshedivat/al-folio](https://github.com/alshedivat/al-folio).
It is already customized for **Chenyu Guo (Harbin Institute of Technology, Shenzhen)** with a
clean starting point. This file tells you what is already done and what you still need to fill in.

---

## 1. What's already done ✅

- **`_config.yml`** — name (`Chenyu Guo`), a one-line bio, language set to English, light theme.
- **`_pages/about.md`** — affiliation set to HIT Shenzhen; bio/address are placeholders for you to edit.
- **`_data/socials.yml`** — your **ORCID** (`0009-0002-5906-4431`) is wired in.
- **`_data/cv.yml`** — a clean CV template pre-filled with your name/affiliation.
- **`_bibliography/papers.bib`** — one example publication entry (template).
- **`_projects/`** — one example project (template).
- **`_news/`** — one welcome announcement.
- All al-folio demo blog posts, Einstein's publications, and large demo media were removed.
- A git repository was initialized with an initial commit.

---

## 2. What you must fill in ✏️

Search for the placeholders below and replace them:

| What                         | Where                                                                          | Placeholder to replace                                                                         |
| ---------------------------- | ------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------- |
| GitHub username              | `_config.yml` (`url`), `_data/socials.yml` (`github_username`), `_data/cv.yml` | ✅ set to `gcy22`                                                                              |
| Email                        | `_data/socials.yml` (`email`), `_data/cv.yml` (`email`)                        | ✅ set to `dutgcy@gmail.com`                                                                   |
| Profile photo                | `_pages/about.md` (`profile.image`)                                            | ✅ left blank — add `assets/img/prof_pic.jpg` then uncomment `image:`                          |
| Bio / address                | `_pages/about.md`                                                              | ✅ updated — Ph.D. CS @ HITSZ; M.S. Mech. Eng. @ DUT (Jun 2026); **refine research interests** |
| Google Scholar ID (optional) | `_data/socials.yml`                                                            | uncomment `scholar_userid:` and fill it                                                        |
| LinkedIn / X (optional)      | `_data/socials.yml`                                                            | uncomment the lines you want                                                                   |
| CV PDF                       | `assets/pdf/Chenyu_Guo_CV.pdf`                                                 | drop your CV here (then edit `cv.yml`)                                                         |
| Publications                 | `_bibliography/papers.bib`                                                     | duplicate the example entry for each paper                                                     |
| Projects                     | `_projects/*.md`                                                               | add/copy project files                                                                         |

> If you want a **user/site** at `https://<username>.github.io`, keep `baseurl: ""` in `_config.yml`.
> If you deploy as a **project** repo (any other name), set `baseurl: "/<repo-name>"`.

---

## 3. Deploy to GitHub Pages 🚀

The repo includes a GitHub Actions workflow (`.github/workflows/deploy.yml`) that builds the
site with Jekyll in the cloud — **you do NOT need Ruby installed locally.**

1. **Create a repository on GitHub** (https://github.com/new):
   - For a personal site: name it `<your-username>.github.io`
   - For a project site: name it anything you like
2. **Push this code** (from the `my-homepage` folder):
   ```bash
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git branch -M main
   git push -u origin main
   ```
3. **Enable Pages**: go to the repo → _Settings → Pages → Build and deployment_,
   set **Source = "Deploy from a branch"**, branch = `gh-pages`, folder = `/ (root)`.
   (The Actions workflow creates the `gh-pages` branch automatically on first push.)
4. **Wait** for the "Deploy site" Actions run to finish (Actions tab), then visit your URL.

> Tip: every time you `git push` to `main`, the site rebuilds and redeploys automatically.

---

## 4. Local preview (optional) 💻

To preview locally you need Ruby + Jekyll (the cloud build above is usually enough).
The easiest path is GitHub **Codespaces** (the repo ships a `.devcontainer`), or follow the
official al-folio install guide: https://github.com/alshedivat/al-folio#install

---

## 5. Useful links

- al-folio docs: https://github.com/alshedivat/al-folio
- Publications format: https://github.com/alshedivat/al-folio#publications
- Adding blog posts: create a file in `_posts/` named `YYYY-MM-DD-title.md`
