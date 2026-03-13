# 🚀 Deploy Your Portfolio to GitHub Pages + bikentimalsina.com

## Step 1 — Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in as `timalsinabiken02`
2. Click **"New"** (green button, top left)
3. Name the repository exactly: `timalsinabiken02.github.io`
   - ⚠️ The name must match your GitHub username exactly
4. Set it to **Public**
5. Click **"Create repository"**

---

## Step 2 — Upload Your Portfolio File

**Option A — Via the GitHub website (easiest):**
1. Open your new repo
2. Click **"Add file" → "Upload files"**
3. Drag and drop `index.html`
4. Scroll down, click **"Commit changes"**

**Option B — Via Git (if you have Git installed):**
```bash
git clone https://github.com/timalsinabiken02/timalsinabiken02.github.io
cd timalsinabiken02.github.io
# copy index.html into this folder
git add index.html
git commit -m "Add portfolio site"
git push origin main
```

---

## Step 3 — Enable GitHub Pages

1. In your repo, go to **Settings** → **Pages** (left sidebar)
2. Under "Source", select **"Deploy from a branch"**
3. Branch: **main** | Folder: **/ (root)**
4. Click **Save**

Your site will be live at:
👉 `https://timalsinabiken02.github.io` (within 1–2 minutes)

---

## Step 4 — Buy Your Custom Domain (bikentimalsina.com)

Recommended registrars (cheapest):
- **Namecheap** → namecheap.com (~$10–12/year)
- **Cloudflare Registrar** → cloudflare.com (~$9/year, at-cost)
- **Google Domains / Squarespace Domains** (~$12/year)

Search for `bikentimalsina.com` and purchase it.

---

## Step 5 — Connect bikentimalsina.com to GitHub Pages

### A) Add DNS Records at Your Registrar

Log in to your domain registrar and add these **A records** pointing to GitHub's servers:

| Type | Host | Value          |
|------|------|----------------|
| A    | @    | 185.199.108.153 |
| A    | @    | 185.199.109.153 |
| A    | @    | 185.199.110.153 |
| A    | @    | 185.199.111.153 |

Also add a **CNAME record**:

| Type  | Host | Value                            |
|-------|------|----------------------------------|
| CNAME | www  | timalsinabiken02.github.io       |

> DNS changes can take up to 24–48 hours to propagate (usually much faster).

### B) Set the Custom Domain in GitHub

1. Go to your repo → **Settings** → **Pages**
2. Under "Custom domain", type: `bikentimalsina.com`
3. Click **Save**
4. ✅ Check **"Enforce HTTPS"** (after DNS propagates)

GitHub will automatically create a `CNAME` file in your repo.

---

## Step 6 — Verify Everything Works

After DNS propagates:
- Visit `https://bikentimalsina.com` ✅
- Visit `https://www.bikentimalsina.com` ✅ (redirects to root)
- Check the padlock icon — HTTPS should be active ✅

---

## Updating Your Site Later

Whenever you want to update content:
1. Edit `index.html`
2. Upload the new version to GitHub (replace the old one)
3. Changes go live automatically within ~30 seconds

---

## 💡 Tips

- **Add a profile photo**: Save your photo as `profile.jpg` in the repo, then update the hero section to include an `<img>` tag.
- **Add your resume**: Upload your CV PDF as `resume.pdf` to the repo, then link the "View Projects" button to it.
- **Google Analytics**: Sign up at analytics.google.com (free) and paste the tracking snippet before `</head>` to see visitor stats.

---

*Total cost: ~$10–12/year for the domain. Hosting is completely free via GitHub Pages.*
