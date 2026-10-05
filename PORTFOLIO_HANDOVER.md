# Portfolio handover — Mallika Mujgule

Final pass completed on 5 October 2026 (updated with the last round of changes).

---

## 1. Final design decisions (locked)

| Decision | Value |
|---|---|
| Colour palette | **Stargazer** (primary `#A2285B`, secondary `#F7D9C4`, accent `#2F5D46`, background `#FFF9F3`, text `#1E1618`) |
| Navigation | **Pill** |
| Card hover | **Pill** |
| Footer heading | **Say Hello** |
| Footer logo | **Lily** |
| About photo frame | **Fan** |
| Jar of Wins | **On** |
| Kind Words | **Cards** |
| Home line | **Line 1** ("Designing products across finance, B2B, IoT, health and AI.") |
| Garden | Unchanged |
| Hero name treatment and interaction | Unchanged |
| Design Options panel | **Kept in the code, hidden on the live site** |
| Review Options panel | **Kept in the code, hidden on the live site** |

### How the hidden panels work

- On the live site, both panels are hidden, and the locked decisions above always apply. Old choices saved in a visitor's browser are cleared, so everyone sees the final design.
- To bring the panels back for experimenting, open the site with `?dev` at the end of the address, for example `https://your-site/index.html?dev` or `index.html?dev` locally. Choices you make in dev mode are saved in your browser only.
- To make an experiment permanent, change the defaults in `index.html`:
  - **Design Options defaults:** search for `var KEYS = {` (navigation, card hover, footer heading).
  - **Review Options defaults:** search for `var D={intro:` (photo frame, kind words, home line, jar, footer lily).

---

## 2. Changes made in this final pass

1. **Production mode:** the Design Options button and panel and the Review Options panel are hidden. Both stay available with `?dev`.
2. **Locked decisions set as defaults:**
   - Pill navigation, Pill card hover and the "Say Hello" footer.
   - Fan photo frame, Cards for Kind Words, Line 1, Jar of Wins on and the Lily logo.
   - The Fan frame's back card was restored behind the About photo.
3. **About:** the intro and expanded copy were replaced with your exact text, word for word.
4. **Resume:** all 3 resume links now point to `https://drive.google.com/drive/folders/1zLJzfmP_t_Iuva1C2Ddp-IsrbT-Y4wiu?usp=sharing`. No references to the old link remain, and the new link was tested: it opens the public "Resume" Drive folder.
5. **Home hero:** the text around the name is harmonised into three sizes.
   - "Hey, I'm" sits above the name.
   - Under the name: Werkstudent at FYTA / Currently based in Berlin, designing products across finance, B2B, IoT, health and AI. / MA Innovation Design Management, Berlin · Available full-time from February 2027.
   - The name and the shape-dropping interaction are unchanged.
6. **Whimsy:**
   - Door eye kept.
   - Eye sketch and lily card removed.
   - Light sketches are now a looping carousel: a slow crossfade with small dots and no thumbnail grid. It pauses on hover, only runs while on screen, and stops for visitors who prefer reduced motion.
7. **Brown Pedha:** print only, with a subtle lift on hover. The bottle-label view is removed.
8. **Spaces (Laurels, Ghibli study):** unchanged.
9. **Readability:** line lengths are capped on a few long paragraphs. No other typography changed.

### Last round of changes

10. **Hero:** the previous layout is back. "Hey, I'm" is now upright and regular, in the same typeface as the name. Under the name sit the "Currently based in Berlin" line, "Designing products across finance, B2B, IoT, health and AI." and one status line: *Werkstudent UX Designer at FYTA, Berlin · MA Innovation Design Management, Berlin · Available full-time from February 2027*, all in one weight.
11. **Email:** changed to **mallikamujgule08@gmail.com** everywhere: Copy email buttons, the contact page and the FYTA "Request a walkthrough" link.
12. **Thermax work card:** aligned with the case study. It now reads "Turning a customer portal that grew feature by feature into one predictable place for asset support." with **30% fewer routine status calls and emails**.
13. **Playground page:** the unlinked page with placeholders is removed. Typing `#playground` now shows the 404 page.
14. **About intro:** replaced with your new text, word for word (with “Today” changed to “Currently” in the FYTA sentence).
15. **Generative carousel:** it loops on its own every 2.4 seconds, and now also **changes on click** or with Enter or the arrow keys, with a small "Click for the next one →" hint. It pauses while the mouse is over it. If your computer has *Reduce motion* turned on (macOS System Settings → Accessibility → Display), the automatic loop stays off by design, but clicking still works. That is the most likely reason it wasn't changing for you before.

---

### Update: mobile, values and highlights

16. **Mobile:** every responsive layout rule now has a second, plain screen-width version alongside the original. Phones and browsers that don't support the newer layout technique (older iPhones, some in-app browsers) now get the mobile layout too. Tested at phone width with and without that support: no sideways scrolling, and the side menu collapses as it should.
17. **Values:** "Curious before clever" is now **"Curious before assuming"**, with the line *"I ask questions early, so the work solves the right problem."*
18. **Home hero highlights:** *finance*, *B2B* and *health* now all use the same highlight colour.

---

### Update: designed for phones

19. **Phone layout (same link, adapts automatically):**
    - **Project cards:** one per row on phones and tablets. Before, they stayed in the desktop 7/5 split, which made them cramped and text-heavy. Each card now shows two tags, a shorter summary (three lines) and a smaller metric, and the hover-only "view" pill is hidden.
    - **Filters:** they scroll sideways in one row instead of wrapping.
    - **Type:** headings, intro lines, body text, quotes and big numbers all step down to phone-friendly sizes.
    - **Spacing:** tighter side margins and section spacing.
    - **Case studies:** the meta row, "In 30 seconds", and the cards and panels use smaller, calmer text.
    - **Checked** at 320, 360, 390, 768 and 1440 px. Desktop is unchanged: cards keep the 7/5 layout at full width.

---

## 3. QA results

| Check | Result |
|---|---|
| Console / JavaScript errors | None from the site's own code. In the test environment, one external resource (Google Fonts or Spotify) was blocked by the sandbox network; this will load normally online. |
| Internal links | All internal link targets resolve. No `href="#"` or empty links, and no placeholder text left. |
| External links | 28 unique. The resume link was tested live. Most source links were opened and checked during the project. LinkedIn, Instagram and Contra could not be fetched automatically (they block bots), so please click them once yourself. |
| Images | 91 images, all with an `alt` attribute (decorative ones are deliberately empty). 84 are lazy-loaded. |
| Contrast | No real failures. 3 automated flags are false positives: white text on coloured SVG shapes that the checker can't see. |
| Text size | No text smaller than 12px. |
| Responsive | Checked at 320, 360, 390, 768, 1024 and 1440 px. No sideways scrolling except the two intentionally scrolling strips. |
| Production UI | Design Options and Review Options not visible. Pill nav, Pill hover, "Say Hello", Lily logo and Stargazer palette all confirmed. |
| Carousel | Advances automatically; works on desktop and mobile. |

### Things I could not fully verify, or that you should know about

- **Video playback:** the four videos are in place, but my test browser can't play MP4s. Play each one once on the live site.
- **Real devices:** layouts were tested in a browser engine at phone and tablet sizes, not on physical phones. Please do a quick check on your own phone after going live.

---

## 4. Project technology

| Item | Detail |
|---|---|
| Framework | None. Plain HTML, CSS and JavaScript in one file (`index.html`). |
| Build tool | None needed. |
| Package manager | None. There is no `package.json` and nothing to install. |
| External dependencies | Google Fonts (Bricolage Grotesque, Newsreader, Figtree, Geist Mono) loaded from fonts.googleapis.com, and a Spotify embed for the footer song, loaded only when clicked. |
| Assets | `images/` (89 WebP images) and `videos/` (4 MP4s). About 11.8 MB in total. |
| Deployment requirement | Any static web host. No server, database or build step. |

There are two versions, and both show the same site:

- **`mallika-portfolio-site/`** (recommended for GitHub): `index.html` plus `images/` and `videos/` folders. It loads faster because images are cached and lazy-loaded.
- **`mallika-portfolio.html`**: one 15.6 MB file with everything embedded. Handy for sharing or a backup, but slower to load.

---

## 5. Environment variables / secrets

**None are required.** The site has no API keys, no backend and no secrets. Nothing sensitive needs to be kept out of the repository.

---

## 6. GitHub setup

- **Repository name:** `mallika-portfolio`. If you want the free address `https://<your-username>.github.io/` without a sub-path, name it **`<your-username>.github.io`** instead.
- **Visibility: Public.** GitHub Pages is free for public repositories. The code holds nothing private.
- **What to commit:** everything inside `mallika-portfolio-site/`, namely `index.html`, `images/`, `videos/`, `.nojekyll` (an empty file that stops GitHub from processing the site), `.gitignore` (already included) and this `PORTFOLIO_HANDOVER.md`.
- **What to exclude:** system files like `.DS_Store`, and the big single-file `mallika-portfolio.html` (not needed online). A `.gitignore` is included in the commands below.

---

## 7. Deployment: which host?

| Host | Fit for this project | Notes |
|---|---|---|
| **GitHub Pages** | **Best fit** | Free, built into GitHub, made for static sites like this one, updates automatically on every push. |
| Netlify | Good | Easy drag-and-drop, but it's a separate account and a second place to manage. |
| Vercel | Fine, but overkill | Built around frameworks like Next.js, which this site doesn't use. |

**Recommendation: GitHub Pages.** The site is plain static HTML with no build step, and it lives in GitHub anyway. You get one place to edit and publish, and every push updates the live site.

---

## 8. Exact commands

You only need Git installed. On a Mac, open Terminal and type `git --version`; if it isn't installed, macOS will offer to install it.

**Step 1: Create the repository on github.com**

1. Sign in, click **+** (top right), then **New repository**.
2. Name: `mallika-portfolio`. Visibility: **Public**. Leave "Add a README" **unchecked**.
3. Click **Create repository**.

**Step 2: In Terminal, go to the downloaded site folder**

```bash
cd ~/Downloads/mallika-portfolio-site
```
*Moves Terminal into your portfolio folder. Change the path if you saved it somewhere else.*

**Step 3: Prepare and push**

```bash
git init
```
*Turns the folder into a Git project, run once.*

```bash
git add .
```
*Selects all the site's files to save.*

```bash
git commit -m "Launch portfolio"
```
*Saves a snapshot of the files with a short note.*

```bash
git branch -M main
```
*Names your main branch "main".*

```bash
git remote add origin https://github.com/<your-username>/mallika-portfolio.git
```
*Links your folder to the GitHub repository. Replace `<your-username>`.*

```bash
git push -u origin main
```
*Uploads everything to GitHub. If it asks for a password, use a GitHub **personal access token** (GitHub → Settings → Developer settings → Personal access tokens), not your normal password. Or install **GitHub Desktop** and push with a button.*

**Step 4: Turn on GitHub Pages**

1. In your repository: **Settings → Pages**.
2. Under **Build and deployment**: Source = **Deploy from a branch**, Branch = **main**, Folder = **/ (root)**, then **Save**.
3. Wait 1–2 minutes. Your site will be live at `https://<your-username>.github.io/mallika-portfolio/`.

---


### Updating the live site after a change (browser only, no Terminal)

You uploaded your site through the GitHub website, so this is the simplest way:

1. Open your repository on github.com.
2. Click **Add file → Upload files**.
3. Drag in the new **index.html**. If you changed any images or videos, drag in the `images` or `videos` folder too. Files with the same name are replaced automatically.
4. Click **Commit changes**.
5. Wait 1–2 minutes, then refresh your live site. On a phone, close the tab and reopen it so you don't see an old cached copy.

## 9. Future updates (Terminal option)

1. Edit `index.html` (or replace images in `images/`).
2. Test locally by double-clicking `index.html`. Add `?dev` to the address to see the Design and Review option panels while experimenting.
3. Save and publish:

```bash
git add .
git commit -m "Describe what you changed"
git push
```

4. GitHub Pages updates the live site automatically within a minute or two.

---

## 10. Final live-site checklist

- [ ] GitHub repository created
- [ ] Project pushed
- [ ] Build successful (Settings → Pages shows "Your site is live")
- [ ] Deployment connected
- [ ] Live URL working
- [ ] Resume link tested
- [ ] Navigation tested
- [ ] Mobile tested (on your own phone)
- [ ] Desktop tested
- [ ] No broken links (click LinkedIn, Instagram, Medium and Contra once)
- [ ] No visible Design Options UI
- [ ] No visible Review Options UI
- [ ] Copy email tested (should copy mallikamujgule08@gmail.com)
- [ ] Videos play
- [ ] Portfolio ready for job applications
