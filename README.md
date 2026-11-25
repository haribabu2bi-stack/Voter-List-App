# JMK Voter List – Party Editing

Files:
- `index.html` – website with Party-only editing in Grid and List views.
- `voter-data.js` – original 1,290 voter records.
- `JMK_Party_AppScript.gs` – Google Sheets backend for shared Party values.

## One-time Google Sheets setup
1. Create a new Google Sheet named `JMK Party Database`.
2. In that Sheet, open **Extensions → Apps Script**.
3. Replace the editor contents with the full contents of `JMK_Party_AppScript.gs`.
4. Save. From the function dropdown, select `setupPartySheet` and click Run. Approve the requested permissions. This creates a `PartyData` tab with S.No and Party columns for all 1,290 records.
5. Click **Deploy → New deployment**. Select type **Web app**.
6. Set **Execute as: Me** and **Who has access: Anyone** (or the broadest access allowed by your organization). Click Deploy and authorize.
7. Copy the Web app URL (ends in `/exec`).
8. Open `index.html` in this repository, click Edit (pencil), replace `PASTE_YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE` with the URL, and Commit changes.

## GitHub Pages
Keep `index.html`, `voter-data.js`, and `README.md` in the repository root. In **Settings → Pages**, select **Deploy from a branch**, branch `main`, folder `/(root)`, then Save.

## Using the app
- Edit only the Party field and click Save.
- Party values are stored in the Google Sheet by S.No; other voter fields are not changed.
- Refreshing the website reloads the shared Party values. Users need internet access.
- Anyone who can access the web app can update Party values. Share the website only with intended users; the underlying voter data is already public in the static site.
