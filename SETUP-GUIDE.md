# CLC Ethiopia website: GitHub Pages setup and admin guide

## Files in this package
- `index.html` – the website (news gallery now loads from `data/news.json`)
- `data/news.json` – all news items (your 6 existing ones are included)
- `admin/index.html` + `admin/config.yml` – the admin panel at `/admin`
- Your existing photos (`images/...`, `St. Ignatius.jpg`, `Family.jpg`, etc.) must be uploaded too, in the same places as before.

## One-time setup (about 15 minutes)
1. Sign in at github.com as **Zekarias1616** and create a **public** repository named `clc-ethiopia` (if you pick another name, edit `repo:` and `site_url:` in `admin/config.yml`).
2. Upload everything: `index.html`, the `data` and `admin` folders, and all your photos and other site files, keeping the same folder structure. Commit to the `main` branch.
3. Go to **Settings > Pages**. Under "Build and deployment", choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save.
4. After 1 to 2 minutes the site is live at `https://zekarias1616.github.io/clc-ethiopia/` and the admin at `.../admin/`.
5. (Optional) Add your own domain under Settings > Pages > Custom domain.

## Giving the admin access
1. The admin creates a free GitHub account.
2. In your repository go to **Settings > Collaborators > Add people** and add their username (they accept the email invitation).
3. The admin creates a token: GitHub > Settings > Developer settings > Personal access tokens > **Fine-grained tokens** > Generate new token. Limit it to the `clc-ethiopia` repository, with **Contents: Read and write**. Copy it and keep it private, like a password.
4. The admin opens `/admin/`, chooses **Sign in with token**, and pastes it. The browser remembers it afterward.

## Everyday use
1. Open `/admin/`, choose **News & Events Gallery**, and click **Add News item** (new items go to the top).
2. Fill in the title, date, category, labels, photo and text, then **Save/Publish**.
3. The site updates in 1 to 2 minutes. Older items are kept; the front shows the newest 6 with a "View older news" button.
4. To edit or delete an item, open it in the same list.

## Tips
- Resize photos to about 1200px wide before uploading so the site stays fast.
- The **date** only controls the order (newest first). The dates on your 6 existing items are placeholders, so correct them in the admin.
- If a photo is missing, the card shows a stock picture instead, so check new items on the live site.
- Do not open `index.html` by double-clicking to test. Browsers block loading `news.json` that way, so test on the live site.
