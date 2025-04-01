# AutoDownload_Sheets_Csv

This Google Apps Script automates the process of exporting specific sheets (tabs) from a Google Spreadsheet to existing CSV files in Google Drive. It also integrates with the spreadsheet's UI, allowing users to trigger the export via a custom menu.

## ✨ Features

- Export specific sheets to CSV format
- Overwrite existing CSV files in Google Drive
- Handles comma escaping in text values
- Adds UTF-8 BOM to ensure compatibility with Excel and other tools
- Adds a custom menu for easy access in the spreadsheet UI

## 📂 Project Structure

- `exportSheetsToCSV()`: Main function that reads data from specified sheets and overwrites existing CSV files.
- `onOpen()`: Adds a custom menu item called **"Run AutoDownload"** to the spreadsheet UI for manual execution.

## ⚙️ How It Works

1. Define:
   - The **Google Sheet ID** (`sheetId`)
   - An array of **sheet names** to export (`sheetNames`)
   - An array of **corresponding CSV file IDs** in Google Drive (`csvFileIds`)
2. When run, the script:
   - Reads data from each sheet
   - Converts it to properly formatted CSV
   - Overwrites the content of the corresponding file in Google Drive

## 🚀 How to Use

1. Open your Google Spreadsheet.
2. Go to **Extensions > Apps Script** and paste this code.
3. Replace the following variables with your actual values:
   - `sheetId`: ID of your Google Sheet
   - `sheetNames`: Names of the sheets to export
   - `csvFileIds`: Corresponding Drive file IDs for output
4. Save and refresh the sheet.
5. A new menu **"Run AutoDownload"** will appear. Click it and run **"Export Sheets to CSV"**.

## 🧪 Example

```javascript
var sheetId = 'YOUR_SHEET_ID_HERE';
var sheetNames = ['Sheet1'];
var csvFileIds = ['EXISTING_CSV_FILE_ID'];
