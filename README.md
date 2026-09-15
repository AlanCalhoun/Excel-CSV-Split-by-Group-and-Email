# Excel-CSV-Split-by-Group-and-Email

Split a CSV into separate files by values in a grouping column, then email each file to the matching recipient.

Built for a recurring behavioral health ops workflow: twice daily, a missing-notes report from the EHR must go to clinic supervisors. Each row includes a clinic location; each location has a different supervisor. This notebook splits the report by location, matches filenames to emails via a mapping workbook, and sends Outlook messages (with a subject keyword that triggers encryption).

## Features

- Group a CSV by a chosen column into per-group files
- Map output filenames to email addresses from an Excel list
- Outlook send path suited for encrypted clinical email policies
- Designed to finish in a few seconds for typical report sizes
- Optional `.bat` launcher for non-technical operators

## Files

| File | Purpose |
|------|---------|
| `Splt CSV by Group and Email.ipynb` | Main workflow |
| `email and file list.xlsx` | Sample filename â†’ email mapping (placeholder addresses) |

## Requirements

- Python 3.x with `pandas` / Jupyter
- Microsoft Outlook configured on the machine (for send)

## Usage

1. Update `email and file list.xlsx` with real filename patterns and recipient addresses.
2. Point the notebook at your source CSV.
3. Run the notebook, or launch via the companion `.bat` if you use one locally.

## Privacy

Do not commit real patient data or production email directories. The sample mapping file uses fictional addresses.

## License

MIT License — see [LICENSE](LICENSE).

