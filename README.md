# ALPFA at SHSU — Official Website

The official website for the **Association of Latino Professionals For America** chapter at Sam Houston State University.

---

## 📁 Project Structure

```
alpfa-shsu/
├── index.html      ← The entire website (single file)
└── README.md       ← This file
```

This is a single-file website — all HTML, CSS, and JavaScript are in `index.html`. No build tools or dependencies required.

---

## ✏️ How to Update Content

All editable data is at the **bottom of `index.html`** in the `<script>` block. Look for the section labeled:

```
/* ============================================================
   EDIT THIS DATA TO UPDATE THE WEBSITE
   ============================================================ */
```

You will find four arrays to update:

### 1. Officers — `OFFICERS`
```js
{ name: "Full Name", title: "Position Title", major: "Major", email: "xx000@shsu.edu", initials: "XX" }
```

### 2. Advisors — `ADVISORS`
```js
{ name: "Full Name", title: "Faculty Advisor", dept: "Department Name", bio: "Short bio.", email: "xx@shsu.edu", initials: "XX" }
```

### 3. Events — `EVENTS`
```js
{ month: "APR", day: "08", type: "Networking", name: "Event Title", time: "6:00 PM – 9:00 PM", location: "Room / Building", desc: "Short description." }
```

### 4. Members — `MEMBERS`
```js
{ name: "Full Name", major: "Accounting", year: "Junior", initials: "XX" }
```
> Valid year values: `Freshman`, `Sophomore`, `Junior`, `Senior`, `Graduate`

### 5. Social Media Links
Search for `social-links` in the HTML and replace the `href="#"` values with your actual URLs:
```html
<a href="https://instagram.com/alpfashsu" ...>IG</a>
<a href="https://linkedin.com/company/alpfashsu" ...>in</a>
```

### 6. Contact Email
Replace `alpfa.shsu@shsu.edu` with your chapter's actual email address.

---

## 🚀 Deploying to GitHub Pages (Free Hosting)

### Step 1 — Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in.
2. Click **+** → **New repository**.
3. Name it `alpfa-shsu` (or any name you prefer).
4. Set it to **Public**.
5. Click **Create repository**.

### Step 2 — Upload Your Files

**Option A: Using the GitHub website (easiest)**
1. In your new repo, click **Add file** → **Upload files**.
2. Drag and drop `index.html` and `README.md`.
3. Click **Commit changes**.

**Option B: Using Git on your computer**
```bash
git init
git add .
git commit -m "Initial commit — ALPFA SHSU website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/alpfa-shsu.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. Go to your repository on GitHub.
2. Click **Settings** (tab at the top).
3. Scroll down to **Pages** in the left sidebar.
4. Under **Source**, select **Deploy from a branch**.
5. Set Branch to `main`, folder to `/ (root)`.
6. Click **Save**.

### Step 4 — Visit Your Site

After ~1–2 minutes, your site will be live at:
```
https://YOUR_USERNAME.github.io/alpfa-shsu/
```

GitHub will show you the exact URL in the Pages settings.

---

## 🌐 Custom Domain (Optional)

If your organization has a domain (e.g., `alpfashsu.org`):

1. In GitHub Pages settings, enter your domain under **Custom domain**.
2. With your domain registrar, add a CNAME record pointing to `YOUR_USERNAME.github.io`.
3. Check **Enforce HTTPS**.

---

## 🔄 Making Updates Later

Whenever you update content:
1. Edit `index.html` locally.
2. Go to your GitHub repo → click `index.html` → click the pencil ✏️ icon to edit directly.
   - OR push changes using Git: `git add . && git commit -m "Update members" && git push`
3. GitHub Pages automatically redeploys within a minute or two.

---

## 📬 Questions?

Contact the ALPFA SHSU webmaster or email **alpfa.shsu@shsu.edu**.

---

*Built with ❤️ by ALPFA at Sam Houston State University*
