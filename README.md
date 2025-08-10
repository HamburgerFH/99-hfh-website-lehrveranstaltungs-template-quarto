## Quick start (after copying the template)

0. **Copy template**

Copy this full template directory, including the hidden `.gitignore` and `.github/workflows/publish.yml`.

1. **Init & first commit**

```bash
git init
git branch -M main
git add .
git commit -m "initial commit"
```

2. **Create GitHub repo and set remote**

Example of remote link, adjust accordingly.

```bash
git remote add origin git@github.com:HamburgerFH/NEW-REPO-NAME.git
git push -u origin main
```

3. **One-time: record publish target (`_publish.yml`)**

```bash
quarto publish gh-pages --no-browser
```

4. **Adjust the `publish.yml` workflow**

Needs optimizing, otherwise too many or too few R packages are installed. Remove them if necessary.

5. **Enable GitHub Pages (in repo Settings -> Pages)**

* Source: **gh-pages**
* Folder: **/**

6. **Actions permissions (repo Settings -> Actions -> General)**

* Workflow permissions: **Read and write**

That’s it. Next pushes to `main` will build & publish automatically.

---

### (Optional) One-liner to do 1–3 at once

```bash
git init && git branch -M main && git add . && git commit -m "Initial site from template" \
&& git remote add origin git@github.com:HamburgerFH/NEW-REPO-NAME.git \
&& git push -u origin main \
&& quarto publish gh-pages --no-browser
```

After that, flip the **Pages** setting (Step 4) once and you’re done.
