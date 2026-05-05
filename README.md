# 📝 Singlish to Sinhala Transliteration Testing

> **IT3040 – IT Project Management (ITPM) | Assignment 1 | SLIIT**

---

## 📌 Project Overview

This project evaluates the **accuracy and reliability** of a chat-based Singlish-to-Sinhala transliteration tool.

🔗 **Tool Under Test:** [https://www.pixelssuite.com/chat-translator](https://www.pixelssuite.com/chat-translator)

The project includes **50 automated negative test cases** designed to identify incorrect or unexpected transliteration outputs, executed using a Python + Playwright automation framework.

### Project Details

- The test data is stored in an Excel workbook.
- The automation script reads each Singlish input from the worksheet.
- The browser is opened automatically and the input is sent to the transliteration tool.
- The generated Sinhala output is captured and compared with the expected result when available.
- The workbook is updated with the actual output and test status after execution.
- This helps evaluate how the tool behaves under negative and unexpected input conditions.

---

## 🎯 Objectives

- ✅ Validate transliteration accuracy of the target tool
- ✅ Identify failure scenarios through **negative testing**
- ✅ Automate test execution using **Playwright**
- ✅ Record and analyze outputs efficiently via **Excel**

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python 3.11 / 3.12 | Core scripting language |
| Playwright | Browser automation framework |
| OpenPyXL | Excel file handling |
| Google Chrome / Chromium | Browser for test execution |

---

## ⚙️ Installation Guide

### Step 1 — Clone or Download the Project

```bash
git clone <your-repo-link>
cd test_automation
```

### Step 2 — Install Required Libraries

```bash
pip install playwright openpyxl
```

### Step 3 — Install Playwright Browsers

```bash
playwright install
```

### Step 4 — Open the Project Folder

Make sure you run the script from the `test_automation` folder so the Excel file path can be resolved correctly.

---

## ▶️ Running the Automation Script

Execute the following command to run all test cases and update the Excel file automatically:

```bash
python test_automation.py \
	--excel "Assignment 1 - Test cases.xlsx" \
	--url "https://www.pixelssuite.com/chat-translator" \
	--wait-ms 5000 \
	--type-delay-ms 80 \
	--slow-mo-ms 200 \
	--save-every 1 \
	--keep-open
```

### Command Options

- `--excel` sets the Excel workbook that contains the test cases.
- `--url` sets the target transliteration tool URL.
- `--wait-ms` controls how long the script waits for results.
- `--type-delay-ms` adds delay between keystrokes while typing input.
- `--slow-mo-ms` slows down browser actions for easier observation.
- `--save-every` saves the workbook after a chosen number of processed rows.
- `--keep-open` keeps the browser open after the test run.

---

## 📂 Project Structure

```text
test_automation/
│
├── test_automation.py               # Main automation script
├── Assignment 1 - Test cases.xlsx   # Test cases & recorded results
└── README.md                        # Project documentation
```

---

## 📊 Output

After execution, the Excel file is automatically updated with:

| Column | Description |
|---|---|
| **Actual Output** | Transliteration result captured from the tool |
| **Status** | `Pass` or `Fail` based on expected vs actual output |

The script can also keep the latest collected output in the workbook if an output file is configured.

---

## 👨‍💻 Author

| Field | Details |
|---|---|
| **Name** | Sathsara Illankoon |
| **Student ID** | IT23554818 |
| **Module** | IT3040 – IT Project Management |
| **Institution** | SLIIT |

---

## ⚠️ Important Notes

- Ensure the Excel file name **matches exactly** as specified in the command
- Maintain a **stable internet connection** throughout test execution
- **Do not close** the browser window while tests are running
- If the website layout changes, the automation selectors may need to be updated in the script.

---

## ✅ Final Submission Checklist

- [x] Excel file completed with all 50 test cases
- [x] Automation script executed successfully
- [x] GitHub repository updated
- [x] README.md added
- [x] ZIP file submitted to CourseWeb