# Google Scholar to EndNote Downloader 📚

This Python script downloads EndNote (`.enw`) files from Google Scholar using a BibTeX (`.bib`) file as input. It searches for each title, attempts to find the "Cite" information, parses it to locate the EndNote download link, and saves the `.enw` file.

## 🚨 IMPORTANT WARNINGS 🚨

* **HIGH RISK:** Google Scholar **actively blocks** automated scraping. Expect temporary **IP blocks (403/429 errors)** and **CAPTCHAs**.
* **NO AUTO-SOLVE:** This script **cannot** solve CAPTCHAs. It will fail on those entries.
* **RUN SLOW & USE VPN:** Long delays are built-in and **essential**. Use a **VPN** and rotate IPs if you encounter blocks.
* **NO GUARANTEE:** Success is **not guaranteed**. Many entries might fail.
* **FRAGILE:** Relies on Google's current HTML structure and `scholarly` – **can break anytime**.

## Setup & Run

1.  **Install Libraries:**
    ```bash
    pip install bibtexparser scholarly requests beautifulsoup4
    ```
2.  **Configure Script:**
    * Download the `main.py` file.
    * Open it and **set the `BIB_FILE_PATH` and `OUTPUT_DIRECTORY` variable** to point to your `.bib` file.
3.  **Run:**
    ```bash
    python main.py
    ```

## Output

* **`.enw` files:** Saved in the `endnote_files` directory (or your configured output folder).
* **`scholar_download.log`:** A detailed log file. **Check this file to see which references failed and need manual download.**

