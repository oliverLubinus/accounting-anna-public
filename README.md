# Accounting Anna

Welcome to the public documentation for Accounting Anna, an automated financial data processing and aggregation agent.

## Project Overview
Accounting Anna streamlines the extraction, cleaning, and aggregation of financial statements from various sources, enabling users to generate unified transaction streams and personal accounting reports with minimal manual effort.

## Features
- Automated extraction of bank statement data from PDFs and CSVs
- Robust data cleaning and standardization for multiple account types
- Aggregation of processed data into a master transaction stream
- Integration with OneDrive for file management and uploads
- Detailed logging and notification system
- Configurable workflows for different financial institutions

## Project Structure
```
accounting-anna/
├── app/                  # (App logic, if present)
├── config/               # Bank and workflow config files (e.g. hanseatic_config.py)
├── node_library/         # Modular nodes (I/O, notify, util)
├── utils/                # Utility modules (PDF extractor, auth)
├── workflows/            # Main workflow and config
├── tests/                # Unit and integration tests
├── workflow_config.yaml  # Workflow step config
└── README.md             # This file
```

## Quickstart
1. **Install dependencies**
    - Requires **Python 3.9+**
    ```sh
    pip install -r requirements.txt
    ```
2. **Configure environment**
    - Copy `.env.example` to `.env` and fill in all required variables (see below).
    - Place your Gmail and OneDrive credentials as needed.
3. **Configure workflow and bank settings**
    - Edit `workflows/workflow_config.yaml` to enable/disable steps and set parameters.
    - Edit config files in `config/` to adjust parsing and extraction logic for each bank.
4. **Run the workflow**
    ```sh
    python workflows/pdf_to_excel_onedrive.py
    ```
5. **Run tests**
    ```sh
    pytest
    ```

## Technology Stack
- Python
- pandas
- OneDrive API integration
- Modular workflow architecture

## Vision & Roadmap
Accounting Anna aims to provide a seamless, automated solution for personal and business financial data management. Future plans include expanded account support, advanced analytics, and user-friendly reporting tools.


## Interested in more details?
- Contact: oliver.lubinus@gmail.com

---

For detailed workflow and architecture information, see the `docs/` folder.