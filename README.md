# Phishing Email Analyzer

A Python-based tool that analyzes `.eml` email files to detect 
phishing indicators, calculate a risk score, and generate reports.

Built and run in Google Colab — no local setup needed.

---

## Features

- **Header Analysis** — extracts From, To, Subject, Reply-To, Date
- **IP Extraction** — pulls IPs from Received headers with false positive filtering
- **Display Name Detection** — flags alarm words like "HACKED" or "SUSPENDED"
- **Reply-To Mismatch** — detects when reply domain differs from sender domain
- **Keyword Detection** — 4 categories: urgency, fear, credential harvesting, financial
- **Weighted Risk Scoring** — scores emails 0–100 with a clear verdict
- **Batch Mode** — analyze multiple .eml files at once with a summary table
- **PDF Export** — generates a styled, downloadable investigation report

---

## Risk Scoring

| Indicator                  | Points |
|----------------------------|--------|
| Alarm words in display name | +30   |
| Reply-To mismatch           | +25   |
| Private IP in routing       | +15   |
| Credential keywords         | +15   |
| Urgency / Fear / Financial  | +10   |

| Score     | Verdict                          |
|-----------|----------------------------------|
| 70 – 100  | 🔴 HIGH RISK — Likely phishing   |
| 40 – 69   | 🟡 MEDIUM RISK — Suspicious      |
| 15 – 39   | 🟠 LOW RISK — Some indicators    |
| 0  – 14   | 🟢 CLEAN                         |

---

## How to Run

1. Open the notebook in [Google Colab](https://colab.research.google.com)
2. Run cells 1–9 top to bottom to load all functions
3. Upload your `.eml` file(s) when prompted
4. View the full analysis report in the output
5. Run Cell 12 to export a PDF report

---

## Project Structure

| Cell | Purpose |
|------|---------|
| 1    | Install dependencies |
| 2    | Create sample .eml file |
| 3    | Header parser |
| 4    | IP extractor |
| 5    | Keyword detector |
| 6    | Risk scorer |
| 7    | Report printer |
| 8    | Single file analyzer |
| 9    | Upload your own .eml |
| 10   | Upload multiple .eml files |
| 11   | Batch analyzer + summary table |
| 12   | Export report to PDF |

---

## Example Output
