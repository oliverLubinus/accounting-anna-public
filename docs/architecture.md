# System Architecture

Accounting Anna is built on a modular workflow architecture, enabling flexible and robust financial data processing. The system is organized into several key components:

## Main Components
- **Workflows**: Each workflow handles a specific stage of data processing (e.g., extraction, cleaning, aggregation).
- **Config**: Centralized configuration files control account detection, file paths, and workflow settings.
- **Utils**: Utility modules provide helpers for error handling, logging, and data transformation.
- **Node Library**: Contains reusable nodes for reading/writing files, integrating with OneDrive, and notifications.

## Data Flow
1. **Input**: Financial statements (PDFs, CSVs) are uploaded to OneDrive.
2. **Extraction**: PDF and CSV files are processed to extract raw transaction data.
3. **Cleaning**: Data is cleaned and standardized for each account type using config-driven logic.
4. **Aggregation**: Cleaned data is combined into a master transaction stream for analysis and reporting.
5. **Output**: Results are saved locally and uploaded to OneDrive; logs and overviews are generated.

## Integration Points
- **OneDrive API**: Used for file download/upload and workflow triggers.
- **Logging & Notification**: Centralized logging and optional email notifications for errors and workflow status.

## Extensibility
- New account types and workflows can be added by updating config files and extending workflow modules.

---

For workflow details, see `workflows.md`. For module summaries, see `modules.md`.