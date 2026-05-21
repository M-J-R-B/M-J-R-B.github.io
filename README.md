# M-J-R-B.github.io

Personal CV for Mary Jhoy Baselisco — a single-page static site hosted on GitHub Pages.

Live: https://m-j-r-b.github.io

## Editing content

Open `index.html` and find/replace the `{{PLACEHOLDER}}` tokens. They're listed in a comment at the top of the file:

- `{{NAME}}`, `{{TAGLINE}}`, `{{PHONE}}`, `{{ADDRESS}}`, `{{SUMMARY}}`
- `{{SKILLS_LANGUAGES}}`, `{{SKILLS_FRAMEWORKS}}`, `{{SKILLS_TOOLS}}`
- `{{JOB_1_TITLE}}` … `{{JOB_2_BULLETS}}` (duplicate the `<article class="entry">` block for more jobs)
- `{{EDU_1_DEGREE}}`, `{{EDU_1_SCHOOL}}`, `{{EDU_1_DATES}}`

To list remaining placeholders at any time:

```
grep -r "{{" .
```

Optional: drop an `assets/avatar.png` (square, ~256px) and add `<img src="assets/avatar.png" alt="" class="avatar">` inside the `.hero` section.

## Local preview

```
python -m http.server 8000
```

Then open http://localhost:8000.

## Deploy

1. Create a new **public** GitHub repo named exactly `M-J-R-B.github.io`.
2. From this folder:

   ```
   git init
   git add .
   git commit -m "Initial CV site"
   git branch -M main
   git remote add origin https://github.com/M-J-R-B/M-J-R-B.github.io.git
   git push -u origin main
   ```

3. On GitHub → **Settings → Pages → Source = Deploy from a branch → Branch = main / root**. Save.
4. After ~1 minute, visit https://m-j-r-b.github.io.

## Stack

Plain HTML, CSS, and a small JS theme toggle. No build step, no framework.
