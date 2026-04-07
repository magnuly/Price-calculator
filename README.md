Product Pricing Calculator — Mac Setup Guide
===========================================

What is included
----------------
- index.html
- styles.css
- app.js
- open_calculator.py
- open_calculator.command
- saved order JSON backup files (if included in the package)

Recommended setup on a Mac
--------------------------
1. Extract the ZIP to any folder, for example your Downloads folder.
2. Open Terminal.
3. Go to the extracted folder, for example:
   cd ~/Downloads/product-pricing-calculator-mac
4. Make the launcher executable:
   chmod +x open_calculator.command
5. Start the calculator:
   ./open_calculator.command
6. Your default browser should open automatically.

If macOS blocks the launcher
----------------------------
If macOS warns that the file is from an unknown developer:
1. Right-click the file `open_calculator.command`
2. Choose `Open`
3. Confirm that you want to open it

If that still does not work
---------------------------
Run a local server manually:

1. Open Terminal in the extracted folder
2. Run:
   python3 -m http.server 8000
3. Open this in your browser:
   http://localhost:8000/index.html

Why localhost is recommended
----------------------------
If you open `index.html` directly as a file, some browsers may block the automatic exchange-rate lookup.
Using the launcher or localhost avoids that problem.

Notes
-----
- Saved orders are stored in the browser you use on that Mac.
- Clicking `Save order` also downloads a JSON backup file locally.
- If JSON backup files are included in the ZIP, they are available as files on the Mac, but they are not automatically imported into the browser's saved-order list.
- Internet access is needed for automatic historical exchange-rate lookup.
- Manual FX override works even without the automatic lookup.
