# Workflow Descriptions

Accounting Anna is organized into modular workflows, each responsible for a distinct stage of financial data processing. Below are the main workflows and their roles:

## 1. PDF to XLSX Extraction
- **Purpose**: Extracts transaction data from bank statement PDFs and writes results to Excel files.
- **Trigger**: New PDF upload or manual start.
- **Output**: Cleaned Excel files in OneDrive.

## 2. Data Preparation
- **Purpose**: Cleans and standardizes raw account data, detects account types, and prepares files for aggregation.
- **Trigger**: After PDF extraction or manual start.
- **Output**: Standardized CSV/Excel files, logs, and overview sheets.

## 3. Build Master Stream
- **Purpose**: Aggregates all processed account files into a master transaction stream XLSX per year.
- **Trigger**: Monthly, after data preparation.
- **Output**: Master transaction stream file for analysis and reporting.

## 4. Personal Accounting
- **Purpose**: Runs personal accounting calculations and reporting on the master transaction stream.
- **Trigger**: Monthly, after master stream build.
- **Output**: Summary reports, categorized spending, and analytics.

---

Each workflow is configurable and can be enabled/disabled via the central config file. For architecture details, see `architecture.md`.