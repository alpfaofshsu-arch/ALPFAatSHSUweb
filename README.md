# ALPFA at SHSU — Website Editing Guide

This guide explains how to update the ALPFA at SHSU website (`index.html`) using **GitHub.com** — no coding software required. All edits are made directly in the browser.

---

## Table of Contents

1. [Repository Setup](#repository-setup)
2. [How to Edit a File on GitHub](#how-to-edit-a-file-on-github)
3. [Updating Officers](#updating-officers)
4. [Updating the Faculty Advisor](#updating-the-faculty-advisor)
5. [Updating Events](#updating-events)
6. [Updating Contact / Email Links](#updating-contact--email-links)
7. [Updating Section Text](#updating-section-text)
8. [Updating External Links](#updating-external-links)
9. [Updating the Logo](#updating-the-logo)
10. [Adding or Removing Sections](#adding-or-removing-sections)
11. [Social Media Links](#social-media-links)
12. [Publishing with GitHub Pages](#publishing-with-github-pages)

---

## Repository Setup

If the website is not yet on GitHub:

1. Go to [github.com](https://github.com) and sign in.
2. Click the **+** icon in the top right → **New repository**.
3. Name it (e.g., `alpfa-shsu-website`), set it to **Public**, and click **Create repository**.
4. Click **Add file** → **Upload files** and drag in `index.html`.
5. Scroll down and click **Commit changes**.

---

## How to Edit a File on GitHub

This is the process for every edit described in this guide:

1. Open the repository on GitHub.
2. Click on **`index.html`** to open it.
3. Click the **pencil icon** (✏️) in the top-right corner of the file view to open the editor.
4. Use **Ctrl+F** (or **Cmd+F** on Mac) to search for the text you want to change.
5. Make your edits directly in the browser editor.
6. When finished, scroll to the bottom and click **Commit changes**.
7. Add a short description of what you changed (e.g., `"Updated officer names"`), then click **Commit changes** again to save.

> 💡 **Tip:** GitHub saves the full history of every commit. If you make a mistake, you can always view or restore a previous version from the **Commits** tab.

---

## Updating Officers

In the editor, search for `const OFFICERS` to jump to this block near the bottom of the file:

```javascript
const OFFICERS = [
  { name: "TBD",  title: "President",              major: "",  email: "lxg149@shsu.edu", initials: "?" },
  { name: "TBD",  title: "Secretary",              major: "",  email: "", initials: "?" },
  ...
];
```

**To update an officer**, replace the placeholder values with real information:

```javascript
{ name: "Jane Doe", title: "President", major: "Accounting", email: "jd001@shsu.edu", initials: "JD" },
```

| Field | Description |
|---|---|
| `name` | Full name of the officer |
| `title` | Their position — **do not change the title text itself** |
| `major` | Their declared major |
| `email` | Their SHSU email address |
| `initials` | Two-letter initials shown in their avatar circle |

**Current officer positions:**
- President
- Secretary
- Treasurer
- VP of Outreach/Socials
- VP of Fundraising
- VP of Recruitment

> **Note:** Do not add or remove entries from this list without also reading [Adding or Removing Sections](#adding-or-removing-sections).

---

## Updating the Faculty Advisor

Search for `const ADVISORS` to find this block:

```javascript
const ADVISORS = [
  {
    name: "TBD",
    title: "Faculty Advisor",
    dept: "Sam Houston State University",
    bio: "Our faculty advisor provides mentorship...",
    email: "",
    initials: "?"
  },
];
```

Replace each field with the advisor's real information:

| Field | Description |
|---|---|
| `name` | Full name (e.g., `"Dr. Jane Smith"`) |
| `title` | Their role (e.g., `"Faculty Advisor"`) |
| `dept` | Their department at SHSU |
| `bio` | A short 1–2 sentence biography |
| `email` | Their SHSU email address |
| `initials` | Two-letter initials for the avatar |

---

## Updating Events

Search for `const EVENTS` to find the events list. Each event looks like this:

```javascript
{
  month: "APR", day: "08",
  type: "Networking",
  name: "Spring Mixer & Industry Night",
  time: "6:00 PM – 9:00 PM",
  location: "Lowman Student Center Ballroom",
  desc: "Connect with local employers..."
},
```

**To add a new event**, copy one block and paste it before the closing `];`, then fill in the new details:

```javascript
{
  month: "OCT", day: "14",
  type: "Workshop",
  name: "My New Event",
  time: "5:00 PM – 7:00 PM",
  location: "BBA Building, Room 101",
  desc: "A short description of the event."
},
```

**To remove an event**, delete the entire `{ ... },` block for that event.

| Field | Description |
|---|---|
| `month` | Three-letter abbreviation (`"JAN"`, `"FEB"`, `"MAR"`, etc.) |
| `day` | Two-digit day (`"08"`, `"15"`, `"22"`) |
| `type` | Category label (e.g., `"Networking"`, `"Workshop"`, `"Social"`) |
| `name` | Event title |
| `time` | Time range |
| `location` | Venue name and room |
| `desc` | Short description shown on the event card |

---

## Updating Contact / Email Links

The president's email address appears in **4 places** in the file. GitHub's editor does not have a built-in find-and-replace, so update each one individually by searching for `lxg149@shsu.edu` and replacing it with the new address.

The 4 locations are:
1. The **Contact Us** button in the Join section
2. The **Email Us** link in the footer
3. The **email social icon** in the footer
4. The **President officer card** in the data array

---

## Updating Section Text

### Hero (Banner) Text

Search for `hero-title` to find:

```html
<h1 class="hero-title fade-up delay-1">
  Where <span>Professionals</span><br>Are Built.
</h1>
```

Edit the text between the tags. The word inside `<span>...</span>` is displayed in gold.

The subtitle just below it can be found by searching for `hero-desc`:

```html
<p class="hero-desc fade-up delay-2">
  ALPFA at SHSU is your community...
</p>
```

### About Section

Search for `id="about"` to jump to the About section. Edit the text inside the `<p style="color:var(--muted); ...">` paragraph tags.

### ALPFA Houston Section

Search for `id="alpfa-houston"` to find this section. The two descriptive paragraphs and the three feature cards (Networking, Scholarships, Social Opportunities) can all be updated by editing the text inside their tags.

### Join ALPFA — Membership Requirements

Search for `id="join"` to find the Join section. The four membership requirements are `<li>` items that follow this pattern:

```html
<li ...><span ...>✓</span><span><strong ...>Requirement Title:</strong> Requirement description.</span></li>
```

Edit the bold title and the description text as needed.

---

## Updating External Links

| Link | Search for this text | Current URL |
|---|---|---|
| ALPFA Houston | `houston.alpfa.org` | `https://houston.alpfa.org` |
| SHSU COBA | `business-administration` | `https://www.shsu.edu/academics/business-administration/` |
| Student Orgs (BearkatHQ) | `campuslabs.com` | `https://shsu.campuslabs.com/engage/organizations` |
| Instagram | `alpfa_at_shsu` | `https://www.instagram.com/alpfa_at_shsu` |

To change a link, search for the text in the **Search for** column and replace the URL in the `href="..."` attribute with the new one.

---

## Updating the Logo

The logo is embedded directly in the HTML as a **base64-encoded image** — a very long string starting with `data:image/jpeg;base64,...`. To replace it:

1. Convert your new logo to base64 using [base64.guru/converter/encode/image](https://base64.guru/converter/encode/image). Copy the full output string.
2. In the GitHub editor, search for `alt="ALPFA at SHSU"`.
3. The logo appears in **two places** (navbar and footer). For each one, replace the entire `data:image/jpeg;base64,XXXXX...` value inside `src="..."` with your new base64 string.
4. Commit the changes.

> ⚠️ The base64 string is very long. Be careful to replace only the value between the quotes and not accidentally delete surrounding code.

---

## Adding or Removing Sections

Each page section is a `<section>` tag with a unique `id`:

| Section ID | Content |
|---|---|
| `hero` | Top banner with title and tagline |
| `about` | Who We Are description and pillars |
| `officers` | Officer and advisor cards |
| `events` | Upcoming events cards |
| `alpfa-houston` | National chapter info |
| `join` | Membership requirements and payment |

If you add a new section, also add a navigation link in three places:

1. **Navbar** — search for `nav-links` and add:
   ```html
   <li><a href="#your-section-id">Label</a></li>
   ```
2. **Mobile menu** — search for `mobile-menu` and add:
   ```html
   <a href="#your-section-id" class="mobile-link">Label</a>
   ```
3. **Footer Quick Links** — search for `Quick Links` and add:
   ```html
   <li><a href="#your-section-id">Label</a></li>
   ```

To remove a section, delete the entire `<section id="..."> ... </section>` block and remove its corresponding links from the navbar, mobile menu, and footer.

---

## Social Media Links

Search for `social-links` to find the footer social icons block:

```html
<a href="https://www.instagram.com/alpfa_at_shsu" target="_blank" class="social-link" title="Instagram">IG</a>
<a href="#" class="social-link" title="LinkedIn">in</a>
<a href="mailto:lxg149@shsu.edu" class="social-link" title="Email">✉</a>
```

- **Instagram:** Replace the `href` URL with the updated Instagram profile URL.
- **LinkedIn:** Replace `href="#"` with the chapter's LinkedIn page URL.
- **Email:** Update using the steps in [Updating Contact / Email Links](#updating-contact--email-links).

To remove an icon entirely, delete the full `<a ...>...</a>` line for it.

---

## Publishing with GitHub Pages

GitHub Pages lets you host the website for free directly from the repository.

**To enable it:**

1. Go to the repository on GitHub.
2. Click **Settings** (top menu).
3. In the left sidebar, click **Pages**.
4. Under **Branch**, select `main` and leave the folder as `/ (root)`.
5. Click **Save**.

After a minute or two, your site will be live at:
```
https://your-username.github.io/your-repository-name/
```

**Every time you commit a change** to `index.html`, GitHub Pages will automatically redeploy the updated site within a few minutes — no extra steps needed.
