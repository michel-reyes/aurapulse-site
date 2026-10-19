# AuraPulse public pages (for the Oura app registration)

Source of truth for the public pages; publish a copy to the separate public repo `aurapulse-site`.
Three static pages: `index.html` (website), `privacy.html`, `terms.html`, plus `style.css`.
Developer name, contact email and date are filled in (Michel Reyes, mreyesh85@gmail.com, October 19, 2026); edit them before publishing if you want different ones.

## Publish free with GitHub Pages
1. On github.com, create a new **public** repository, e.g. `aurapulse-site` (keep the app's own code private and separate).
2. Click **Add file › Upload files** and drag in all files (including the `oauth` folder) from this folder. Commit.
3. Settings › **Pages** › Source: *Deploy from a branch*, Branch: `main` / `(root)`. Save.
4. After a minute your pages are live at:
   - Website: `https://<your-github-username>.github.io/aurapulse-site/`
   - Privacy Policy: `https://<your-github-username>.github.io/aurapulse-site/privacy.html`
   - Terms of Service: `https://<your-github-username>.github.io/aurapulse-site/terms.html`

## Oura registration fields (https://developer.ouraring.com/applications)
- Display name: AuraPulse
- Website / Privacy Policy / Terms of Service: the three URLs above
- Redirect URI: `com.michelreyes.aurapulse:/oauth/oura` (an app callback, not a web page — type it exactly).
  If the form only accepts https, use `https://<your-github-username>.github.io/aurapulse-site/oauth/oura.html` instead (this folder includes that page).
- Scopes: Daily, Heartrate, Workout, Tag, Ring Configuration (optional: SpO2). Leave Email, Personal, Session, Stress, Heart Health unchecked.
- After saving: send the **Client ID** only (never the Client Secret — the app doesn't use it).
