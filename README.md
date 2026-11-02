# PlanSurf Property

A lightweight investment property manager for small to mid-size investors.

This project tracks property details, rental income, deductible expenses, depreciation, CGT, stamp duty, and land tax for Australian investment properties. It follows the PlanSurf Budget app's browser-first design and encrypted OneDrive sync model.

Features:
- FY-based property tracking and portfolio summaries
- Rental income and expense management
- ATO-oriented tax calculators and summaries
- Depreciation and capital works tracking
- Microsoft sign-in and encrypted OneDrive sync
- JSON backup import and export, plus dark mode

Usage:
- Serve the repo over HTTPS (or localhost) and open it in a browser
- Add your properties and transactions
- Open the OneDrive button, sign in, and enter an encryption passphrase to load or save your property file
- Once OneDrive has been unlocked, changes are encrypted in your browser and saved automatically

The encryption passphrase is kept in memory and is never sent to Microsoft. OneDrive stores only the encrypted file `PlanSurfProperty.enc.json` in the app folder; PlanSurf has no property-data backend. Losing the passphrase means the file cannot be recovered. The Microsoft Entra application must allow this site's URL as a single-page application redirect URI. Its public client ID is configured in `config.js`.

Existing property data in this browser's previous local-storage keys is loaded into memory on first launch and the unencrypted browser copy is removed. Save that data to OneDrive or export a JSON backup before closing the page.
