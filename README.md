# IT23181892-ITPM-New_Assignment_01

This project runs a Playwright-based automation script that reads test cases from an Excel file, sends each input to the chat translator UI, and writes the actual output and status back into the workbook.

## Requirements

- Python 3.11 recommended
- `openpyxl`
- `playwright`

Install the dependencies from the project root:

```powershell
python -m pip install --upgrade pip
pip install openpyxl playwright
playwright install
```

## Run

Run the script from the `Test_Automation` folder so the default Excel path is resolved correctly:

```powershell
cd Test_Automation
python IT23181892.py --excel "IT23181892.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

## Useful flags

- `--headless` runs the browser without a visible window.
- `--output` writes results to a different Excel file.
- `--sheet` selects a specific worksheet if the workbook has more than one.
- `--wait-ms`, `--type-delay-ms`, and `--slow-mo-ms` let you slow down or speed up the automation.

