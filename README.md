
# 📄 README: Advanced Company Profiling and Data Validation

## Project Overview

This project aims to build a **data engineering solution** that profiles, cleans, deduplicates, validates, and enriches company records for UK companies, leveraging the **Companies House REST API** for validation and enrichment.

All steps are implemented using **Python** in a **Jupyter Notebook**, combining exploratory data analysis, cleansing techniques, API integration, and reporting through visualization.

---

## Key Steps in the Notebook

1. ✅ **Data Ingestion**
   - Reads the provided `Company.csv` file into a pandas DataFrame.
   - Initial inspection of row and column counts.

2. ✅ **Data Profiling**
   - Missing value analysis.
   - Duplicate records detection.
   - Use of `ydata-profiling` for automatic profiling reports.

3. ✅ **Data Cleansing**
   - Dropping rows with missing critical fields (e.g., company name).
   - Trimming whitespace and normalizing text case.
   - Normalizing column names for consistency.
   - Validating company number formats with regex.
   - Merging address columns to derive FullAddress Column.
   - Converting data columns to same format.
   - Fill missing fields with placeholder values.
   - Dropping unwanted columns with maximum null values.

4. ✅ **Deduplication**
   - Identifies and flags duplicate records by **company name** and **company number**.
   - Creates indicator columns for duplicates.

5. ✅ **Matching and Enrichment (API Integration)**
   - Connects to **Companies House REST API** to validate and enrich company records.
   - Matches company names to retrieve metadata such as company number, status, address, and incorporation date.
   - Merges enriched data back into the cleaned DataFrame.
   - Validating matches and investigate discrepancies.

6. ✅ **Reporting and Visualization**
   - Uses **Matplotlib** and **Seaborn** for:
     - Pie charts showing duplicate vs. unique records.
     - Bar charts comparing duplicates by name vs. number.
     - Visual summaries of data distributions.

---

## Technologies Used

- Python (Jupyter Notebook)
- pandas, numpy
- requests (API calls)
- ydata-profiling (EDA)
- Matplotlib, Seaborn, Plotly (visualization)

---

## How to Run

1. Install required packages (included at the start of the notebook):

   ```bash
   pip install pandas numpy ydata-profiling requests plotly seaborn
   ```

2. Open the notebook (`Cluedin_Assignment.ipynb`) in Jupyter Lab or Google Colab.

3. Ensure the `Company.csv` file is in the same directory or update the file path.

4. Run cells sequentially.

---

## Outputs & Deliverables

- Cleaned and validated company dataset.
- Enriched company information via Companies House API.
- Summary visualizations highlighting duplicates and data quality.
- Final merged dataset ready for downstream processing or reporting.

---

## Author’s Notes

This notebook showcases practical **data engineering skills** including:
- Data profiling & cleaning
- API integration
- Deduplication logic
- Data validation workflows
- Clear documentation & reproducibility

✅ Ready to integrate into larger ETL pipelines or data governance solutions.

---



