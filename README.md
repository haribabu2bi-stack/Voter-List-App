# JMK Voter List

A static voter-list website built from `JMK_Voter_List(1).xlsx`.

## Files
- `index.html` — website interface (Grid View and List View).
- `voter-data.js` — voter records embedded as local JavaScript data.

## Features
- Search by S.No.
- Search by voter Name.
- Filter by Party, Gender, and Ward.
- Switch between Grid View and List View.
- Displays all source columns: S.No, Party, Name, Tandri Peru, Age, Gender, Door No, Voter ID, Ward.
- No server or database required; the website works as a static site.

## Run locally
Keep `index.html` and `voter-data.js` in the same folder, then open `index.html` in a browser.

## Publish with GitHub Pages
1. Create or open your GitHub repository.
2. Upload `index.html`, `voter-data.js`, and this `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main** and folder **/(root)**, then click **Save**.
6. Wait for GitHub Pages to publish and open the generated website link.

## Source data
- Worksheet: `Voter Details`
- Records: 1290
- Columns: 9

This is a static viewer. It does not edit or save changes back to the Excel file.
