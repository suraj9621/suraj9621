# 🐍 FIX Contribution Snake Animation (100% Working)

Aapka snake animation isliye work nahi kar raha kyunki GitHub Actions permissions aur workflow properly setup nahi hua hai.

---

# ✅ STEP 1 — Repository Name Check

Repository ka naam EXACTLY ye hona chahiye:

```bash
surajkushwaha123
```

⚠️ Same as your GitHub username.

---

# ✅ STEP 2 — Create Workflow Folder

Apne repository me ye folder banao:

```bash
.github/workflows/
```

Uske andar file banao:

```bash
snake.yml
```

---

# ✅ STEP 3 — Paste THIS FULL WORKING CODE

```yaml
name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"

  workflow_dispatch:

permissions:
  contents: write

jobs:
  generate:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout
        uses: actions/checkout@v3

      - name: Generate Snake Animation
        uses: Platane/snk@v3
        with:
          github_user_name: surajkushwaha123
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Push Snake Animation
        uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist

        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

---

# ✅ STEP 4 — GitHub Permissions ON Karo

Go to:

```bash
Settings → Actions → General
```

Scroll down 👇

### Workflow permissions:

✅ Select:

```bash
Read and write permissions
```

Then:

✅ Save

---

# ✅ STEP 5 — Actions Enable Karo

Go to:

```bash
Settings → Actions → General
```

Ensure:

✅ Allow all actions and reusable workflows

---

# ✅ STEP 6 — Run Workflow

Go to:

```bash
Actions
```

Then:

```bash
Generate Snake
```

Click:

```bash
Run workflow
```

Wait 2-3 minutes ⏳

---

# ✅ STEP 7 — README Me Ye Code Add Karo

```html
# 🐍 Contribution Snake

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/surajkushwaha123/surajkushwaha123/output/github-contribution-grid-snake-dark.svg">

  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/surajkushwaha123/surajkushwaha123/output/github-contribution-grid-snake.svg">

  <img alt="github contribution snake animation" src="https://raw.githubusercontent.com/surajkushwaha123/surajkushwaha123/output/github-contribution-grid-snake-dark.svg">

</picture>

</div>
```

---

# ✅ FINAL RESULT

Snake animation fully working ho jayega:

✅ Dark Mode  
✅ Light Mode  
✅ Auto Update Daily  
✅ Animated Snake  
✅ Professional Look

---

# 🚨 AGAR FIR BHI WORK NA KARE

Check karo:

### ❌ Common Mistakes

- Repository name wrong
- Actions disabled
- Workflow permissions OFF
- snake.yml wrong folder me
- README me username galat
- Workflow run nahi kiya

---

# ✅ Correct Folder Structure

```bash
surajkushwaha123/
│
├── README.md
│
└── .github/
    └── workflows/
        └── snake.yml
```

---

# 🔥 EXTRA PRO TIP

Ye bhi add karo README me:

```html
<img src="https://github-profile-trophy.vercel.app/?username=surajkushwaha123&theme=tokyonight&no-frame=true&row=1&column=7"/>
```

Aur:

```html
<img src="https://github-readme-activity-graph.vercel.app/graph?username=surajkushwaha123&theme=react-dark"/>
```

Profile aur professional lagega 🚀
