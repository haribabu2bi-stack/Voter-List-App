# Voter Payment Status Web App

A voter-list management interface for viewing voter details and updating payment and vote-cast status.

## Features

- Search by S.No, name, mobile number, initial, or caste.
- Edit mobile number and caste.
- Update Payment Status (`Pending` / `Paid`).
- Update Vote Cast (`Not Done` / `Done`).
- Record the person who collected/recorded the payment in `PAID BY`.
- Export the full list or the currently filtered list as CSV or Excel-compatible `.xls`.

## Important: Hosting

This `index.html` is designed to run as the HTML front end of a **Google Apps Script web app**. It uses `google.script.run` to call server-side Apps Script functions such as `getVoters()` and `updatePayment()`.

It will **not work as a standalone GitHub Pages site** without replacing the Apps Script calls with a backend/API. GitHub can be used to store and version-control the source files, while Google Apps Script serves the working web app.

## Files

- `index.html` — front-end UI.
- `Code.gs` — server-side Google Apps Script code (keep this in the Apps Script project, or add it to the repository for source control).

## Setup in Google Apps Script

1. Open the Google Sheet containing the voter list.
2. Open **Extensions → Apps Script**.
3. Add or replace the HTML file named `Index` with the contents of `index.html`.
4. Add the matching server-side functions from `Code.gs` to the Apps Script project.
5. Confirm the sheet headers match these names (case-insensitive):
   - `S.No`
   - `MOBILE`
   - `పేరు`
   - `తండ్రి / భర్త`
   - `INTIAL`
   - `CASTE`
   - `PAYMENT STATUS`
   - `PAID BY`
6. The script adds a `VOTE CAST` column if it is missing.
7. Save, then choose **Deploy → Manage deployments → Edit → New version → Deploy**.
8. Restrict access to people who are authorized to view and edit voter data.

## Export notes

- CSV exports are UTF-8 with a BOM to help Excel display Telugu text correctly.
- The Excel option creates an Excel-compatible `.xls` file, not a native `.xlsx` workbook.
- Exporting the filtered list exports the records matching the current search field and search value.
- Save edits before exporting to ensure the latest changes are included.

## Privacy

The sheet may contain personal information. Do not publish the sheet or its data in a public GitHub repository. Keep the repository private if it contains internal source code or configuration, and restrict the web app to authorized users.
