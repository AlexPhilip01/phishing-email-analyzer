# phishing-email-analyzer
# Phishing Email Analyzer

## Overview

This project is a simple Python-based tool that analyzes email headers to identify potential phishing indicators. It parses `.eml` email files and extracts key metadata such as sender information, IP addresses from the Received headers, and suspicious keywords commonly used in phishing campaigns.

The project demonstrates basic email forensics techniques used in cybersecurity investigations.

---

## Features

* Parses email header information
* Extracts sender IP addresses from "Received" headers
* Detects suspicious phishing-related keywords
* Generates a simple investigation report
* Includes a sample phishing email file for testing

---

## Technologies Used

* Python 3
* Google Colab
* Regular Expressions
* Python Email Library

---

## Project Structure

```
phishing-email-analyzer
│
├── Phishing_Email_Analyzer.ipynb
├── sample.eml
├── README.md
```

---

## How the Analyzer Works

1. The user uploads an `.eml` email file.
2. The script parses the email headers.
3. IP addresses are extracted from the "Received" header.
4. The subject line is checked for phishing keywords.
5. The tool outputs a simple investigation report.

---

## Example Output

```
----- Email Analysis Report -----

Sender: support@fakebank.com
Subject: Urgent! Verify your bank account

Sender IP Addresses:
192.168.1.50

Phishing Indicators:
Suspicious keyword detected: urgent
Suspicious keyword detected: verify
Suspicious keyword detected: bank

Analysis Completed
```

---

## How to Run the Project

1. Open the notebook in Google Colab.
2. Upload an `.eml` file when prompted.
3. Run all cells to analyze the email.
4. Review the phishing analysis report.

---

## Learning Outcomes

This project demonstrates several core cybersecurity concepts:

* Email header analysis
* Identification of phishing indicators
* Basic threat investigation workflow
* Automation of security analysis using Python

---

## Future Improvements

* Extract URLs from the email body
* Integrate IP reputation checks
* Implement phishing risk scoring
* Detect suspicious sender domains

---

## Disclaimer

This project is intended for educational and research purposes only.

