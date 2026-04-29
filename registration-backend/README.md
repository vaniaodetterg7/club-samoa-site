# Club Samoa Registration Backend

This folder contains the Google Apps Script backend and Excel templates for the two registration databases:

- `club-samoa-registro-uniformes.xlsx`
- `club-samoa-registro-examenes.xlsx`

## Google Sheets Setup

1. Open [script.google.com](https://script.google.com/) and create a new Apps Script project.
2. Paste the contents of `apps-script/Code.gs` into the project.
3. Run `configureDataSheets` once to connect the forms to the existing Google Sheets:
   - Uniformes: `1ZiN8C63ssLsCMhiszuU1I_xXkuIgGzFswmLm0vdp8cU`
   - Exámenes: `1GTkg0CF-AJLX-It04hBneMWBOqN0tNGyZFoW029YtjY`
4. Run `setupClubSamoaRegistros` once if you need Apps Script to format/rebuild the `Registro`, `Resumen`, and `Catalogos` tabs in those Sheets.
5. Approve the Google permissions.
6. Check the execution log. It will show the URLs for the two connected Google Sheets.
7. Optional: run `configureNotificationEmail("tu-correo@example.com")` to choose where notifications go.
8. Deploy the project as a Web App.
9. Set **Execute as** to `Me`.
10. Set **Who has access** to `Anyone`.
11. Copy the Web App URL ending in `/exec`.
12. Paste that URL into `registration-config.js`.

After that, the website forms will save rows into the matching Google Sheet and send an email notification for each new registration.
