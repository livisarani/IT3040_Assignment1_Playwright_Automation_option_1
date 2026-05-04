# IT3040 Assignment 1 - Playwright Automation

This repository contains the completed Playwright automation for IT3040 Assignment 1.
It reads test data from the Excel workbook, sends each input to the web app, captures the translated output, and writes the result back into the workbook.

## Repository Link

GitHub repository: https://github.com/livisarani/IT3040_Assignment1_Playwright_Automation_option_1.git

The same link is also stored in [Git_Repository_Link.txt](Git_Repository_Link.txt).

## Included Files

- [test_automation.py](test_automation.py): main Playwright automation script
- [Assignment 1 - Test cases.xlsx](Assignment%201%20-%20Test%20cases.xlsx): completed test case workbook
- [Commands.txt](Commands.txt): example command used to run the script

## Prerequisites

- Python 3.10 or later
- Internet access for the browser automation target
- The following Python packages:
	- `playwright`
	- `openpyxl`

## Install Dependencies

From the project root, run:

```powershell
python -m pip install --upgrade pip
pip install playwright openpyxl
python -m playwright install chromium
```

If you are using a virtual environment, activate it before installing the packages.

## Run the Tests

Use the workbook included in the repository and run the automation with:

```powershell
python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

## What The Script Does

- Opens the browser and loads the target chat translator page
- Reads the Singlish input from the Excel sheet
- Sends each row to the web app and captures the Sinhala output
- Writes the actual output and pass/fail status back into the workbook
- Saves the completed results to the Excel file

## Notes

- The completed Excel file is titled [Assignment 1 - Test cases.xlsx](Assignment%201%20-%20Test%20cases.xlsx).
- The repository should remain publicly accessible for marking.
- If you want to save results to a different file, use the `--output` argument.