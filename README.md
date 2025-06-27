# Restore n8n Workflows

This repository provides instructions and workflows for restoring your n8n workflows from backup files stored in GitHub, Google Drive, or another storage solution.

Template Spreadsheets Prompts https://docs.google.com/spreadsheets/d/1-xP4ihuQPBkPAQP9oQcEjRU9OooX8kP4bXht1U2soXU

Template Spreadsheets Bot Telegram https://docs.google.com/spreadsheets/d/1OKECNjNZW3f8hEgf2Hf4bw7CwqB8I6dmy8zeqjEyFJI
## Prerequisites

- **n8n instance** (self-hosted or cloud)
- **Backup files** (JSON format) stored in your chosen backup location
- **Access credentials** for the backup storage (e.g., GitHub token, Google Drive API key)
- **n8n API key** for authentication


## Supported Backup Sources

- **GitHub**: Workflows stored as JSON files in a GitHub repository[^2][^4]
- **Google Drive**: Workflows stored as JSON files in a Google Drive folder[^3]
- **Local Storage**: Workflows stored as JSON files on your local machine


## Quick Start

### 1. Restoring from GitHub

1. **Clone or download this repository** (if you are using a template).
2. **Configure the workflow**:
    - Open the workflow in your n8n editor.
    - Update the `Globals` node with your GitHub repository details:
        - `repo.owner`: Your GitHub username
        - `repo.name`: Name of your backup repository
        - `repo.path`: Path to your workflows folder (e.g., `workflows/`)
3. **Set up credentials**:
    - Add your GitHub token as a credential.
    - Add your n8n API key as a credential.
4. **Test and run the workflow** to restore your workflows from GitHub[^2][^4].

### 2. Restoring from Google Drive

1. **Open the Google Drive restore workflow** in your n8n editor.
2. **Set up Google Drive API credentials**.
3. **Specify the Google Drive folder** where your backup files are stored.
4. **Test and run the workflow** to restore your workflows from Google Drive[^3].

### 3. Restoring from Local Storage

1. **Download your backup JSON files** to your local machine.
2. **Open your n8n instance**.
3. **Import each workflow manually** via the n8n UI or use the CLI tool for bulk import[^5].

## Workflow Features

- **Bulk restore**: Automatically import multiple workflows in a single run.
- **Duplicate handling**: Skips or updates existing workflows based on configuration.
- **Manual or scheduled**: Trigger the restore process manually or on a schedule.


## Additional Notes

- **Workflow history**: You can also use n8n's built-in workflow history to restore previous versions of a workflow, depending on your plan[^6].
- **Backup frequency**: Adjust backup and restore schedules as needed.
- **Credentials backup**: Consider backing up your n8n credentials for a full recovery[^5].


## Troubleshooting

- **Workflow not restoring**: Check your credentials and API permissions.
- **Duplicate workflows**: Configure the workflow to skip or update existing workflows.
- **Memory issues**: For large numbers of workflows, monitor memory usage during bulk restore[^4].


## Resources

- [n8n Workflow History Docs][^6]
- [GitHub Backup \& Restore Workflows][^2]
- [Google Drive Backup \& Restore Workflows][^3]
- [n8n Community: Restore Backups of Workflows][^5]

