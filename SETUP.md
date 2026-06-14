# Setup — make this Profile README live

Your README only shows on your GitHub profile if it lives in a **special repo whose
name is exactly your username**. For you that means a repo called **`Harini7798`**
owned by the account **`Harini7798`** → `github.com/Harini7798/Harini7798`.

> ⚠️ The username must match **exactly** (case doesn't matter for the URL, but the
> repo name must equal the account name). If your real handle isn't `Harini7798`,
> rename the repo to match and update the two `Harini7798/Harini7798` URLs in `README.md`.

---

## 1. Create the special repo

1. Go to https://github.com/new
2. **Repository name:** `Harini7798`  ← must equal your username
3. Set it to **Public**
4. ✅ Check **"Add a README file"** (you'll overwrite it)
5. Click **Create repository**

GitHub will show a little hint: *"You found a secret! Harini7798/Harini7798 is a special
repository…"* — that confirms it's the right one.

## 2. Push these files

From inside this folder (`GitHub Portfolio`):

```bash
git init
git add .
git commit -m "retro profile readme + snake"
git branch -M main
git remote add origin https://github.com/Harini7798/Harini7798.git
git push -u origin main --force   # --force only because step 1 made an initial commit
```

## 3. Turn on Actions write permission (one time)

The snake Action needs permission to push the generated SVG.

1. Repo → **Settings** → **Actions** → **General**
2. Scroll to **Workflow permissions**
3. Select **"Read and write permissions"** → **Save**

## 4. Run the snake once

1. Repo → **Actions** tab
2. Pick **"Generate Contribution Snake"** → **Run workflow** → **Run workflow**
3. Wait ~30s. It creates an `output` branch containing the snake SVGs.
4. Refresh your profile — the snake now animates. It re-runs daily on its own.

> The snake images are 404 / blank until this first run finishes. That's normal.

---

## Customizing

| What | Where |
|------|-------|
| Typing header text / color / speed | `README.md` → the `readme-typing-svg` URL |
| Your own pixel banner | drop `assets/banner.png`, then swap the banner `<img>` in `README.md` (commented instructions are right there) |
| About Me bullets | `README.md` → the `## 🚀 About Me` section |
| Add stats / streak / trophy cards later | just ask — they're one-line embeds |

### Typing header quick reference
The header is an image from `readme-typing-svg.demolab.com`. Edit these query params:
- `lines=` — semicolon-separated lines it types (URL-encode spaces as `+`, `,` as `%2C`)
- `color=` — hex without `#` (currently `22D3EE`, cyan)
- `size=` — font size · `duration=` — type speed · `pause=` — pause between lines
