# CRM Productivity Abnormality Checker

A Streamlit app for uploading the daily CRM Productivity Dump, identifying abnormalities, and downloading an Excel report.

## Checks included

1. Placeholder mobile: `0000000000`
2. Invalid mobile format
3. Fake/default GPS: `51.673858, 7.815982`
4. Duplicate GPS with another visit
5. Visit less than 3 minutes after the previous visit by the same employee
6. Date anomaly against the selected report date
7. Invalid/missing GPS

The output contains:

- `Total_Flags`
- `Flag_Summary`
- Summary sheet
- Abnormality Summary sheet
- Employee Summary sheet
- Flagged CRM Data sheet

## Run locally

```bash
pip install -r requirements.txt
streamlit run app.py
```

Then open the local Streamlit URL shown in the terminal.

## Deploy on Streamlit Community Cloud

1. Create a GitHub repository, for example `crm-abnormality-checker`.
2. Upload `app.py` and `requirements.txt`.
3. Go to Streamlit Community Cloud.
4. Connect your GitHub account.
5. Select the repository, branch and `app.py`.
6. Click Deploy.
7. Upload the daily CRM Excel file in the deployed app.
8. Click Download Abnormality Report.

No CRM file needs to be stored in the GitHub repository.


## Highlighting

In **Flagged CRM Data**, every record with `Total_Flags > 0` is highlighted in light orange, matching the style of the reference screenshot. The downloaded Excel report also highlights the complete abnormal row.
