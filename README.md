# Library Due Date Reminder Automation

A UiPath RPA automation that reads library book return dates from an Excel file and automatically sends email reminders to patrons before their due dates.

## What It Does
1. Reads library book data from an Excel file (patron name, book title, return date)
2. Checks each return date against the current date
3. Automatically sends email reminders to patrons with upcoming or overdue returns

## Tech Stack
| Component | Technology |
|-----------|-----------|
| RPA Platform | UiPath Studio 25.0.166 |
| Data Source | Microsoft Excel |
| Notifications | Email (SMTP via UiPath Mail Activities) |
| Language | Visual Basic (UiPath expressions) |

## Prerequisites
- UiPath Studio 25.0.166 or later
- UiPath Robot
- Access to an SMTP server for sending emails
- An Excel file with library book data

## Setup & Running

1. Open **UiPath Studio**
2. Open the project via `project.json`
3. Studio will auto-download required dependencies
4. Configure SMTP settings inside the workflow (mail server, credentials, sender address)
5. Update the Excel file path variable to point to your input file
6. Run `Main.xaml`

The automation will process each row and send email reminders where applicable.

## Excel Input Format
Your Excel file should include columns for:
- Patron name / email
- Book title
- Return / due date

## Project Structure
```
Library-Due-Date-Reminder-Automation/
├── Main.xaml       # Entry point workflow
├── project.json    # UiPath project configuration
└── .settings/      # Project settings
```

## Scheduling
This automation can be scheduled via **UiPath Orchestrator** to run automatically on a daily or weekly basis.
