# Dashboard Automation for the Center for Indonesian Policy Studies (CIPS)

> This project aimed to automate the addition of new publications and monthly data to CIPS's Google Sheets dashboard

## Details
- Monthly data is gathered from Excel files on Google Drive containing monthly Download/View data for Neliti, a research publication repository, and Google Analytics
- Publication titles were webscraped from CIPS' website and the Neliti website
- The Google Sheets, Google Drive, and Google Analytics APIs were setup through Google Cloud
- Code is set to run at the start of every month for data from the previous month

## Methodology
1. Webscrape all the publication titles from the CIPS website and Neliti
2. Pull the current dashboard from Google Sheets using the API
3. Compare the webscraped titles with the current titles on the dashboard
4. Add new rows for each of the missing titles, if any, and ask the user to input the appropriate publication type and topic
5. Add new monthly data to the dashboard dataframe, pulling any missing month files from Google Drive and any missing month data from Google Analytics
6. Re-upload the complete dataframes to the Google Sheets dashboard using the API
