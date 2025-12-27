# Module and Folder Summaries

Accounting Anna is organized into several key folders and modules, each with a specific responsibility:

## Folder Structure
- **workflows/**: Contains the main workflow scripts for each processing stage (e.g., data preparation, master stream).
- **config/**: Centralized configuration files (YAML, Python) for account detection, workflow settings, and file paths.
- **utils/**: Utility modules for helpers, error handling, logging, and data transformation.
- **node_library/**: Reusable nodes for file I/O, OneDrive integration, notifications, and security.
- **pdf_extractors/**: Specialized modules for extracting data from different bank statement PDF formats.
- **output/**: Stores generated output files, logs, and processed data.
- **tests/**: Test scripts for validating workflows and integration.

## Key Modules
- **helpers.py**: Common helper functions for error handling, account detection, and logging.
- **helpers_data_preparation.py**: Data cleaning and preprocessing helpers for the data preparation workflow.
- **helpers_build_master_stream.py**: Functions for aggregating and standardizing transaction data.
- **onedrive_auth.py**: Handles authentication and token management for OneDrive API access.
- **logging_node.py**: Centralized logging utility for all workflows.

---

For workflow and architecture details, see `workflows.md` and `architecture.md`.