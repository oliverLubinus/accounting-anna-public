# Configuration Guide

Accounting Anna is highly configurable via YAML and Python config files. The main configuration file is `main_config.yaml`, which controls workflow settings, account detection, file paths, and more.

## Key Configuration Sections

### 1. Global Settings
- **onedrive_output_folder**: Path for temporary output files.
- **onedrive_processed**: Path for processed files.
- **local_output_folder**: Local directory for output and logs.
- **file_extensions**: List of file types to process (e.g., `.xlsx`, `.csv`).

### 2. Workflow Settings
- **workflows**: Enable/disable each workflow and set descriptions, owners, and schedules.
- **data_preparation**: Tab names, column mappings, date formats, and regex patterns for each account type.
- **master_stream_workflow**: Required columns, alternate column mappings, and date formats for aggregation.

### 3. Account Detection
- Account type is determined by matching filename prefixes or patterns defined in the config.
- Easily add new account types by updating the relevant prefix or pattern lists.

### 4. Logging and Notifications
- **LOG_FILE**: Path for the unified log file.
- Email and notification settings can be configured for workflow alerts.

## How to Update the Config
- Edit `config/main_config.yaml` to change workflow behavior, add new account types, or update file paths.
- Restart the relevant workflow for changes to take effect.

---

For more on folder/module structure, see `modules.md`. For workflow details, see `workflows.md`.