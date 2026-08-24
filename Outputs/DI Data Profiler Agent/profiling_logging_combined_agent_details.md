# Table Information

| Field | Value |
| --- | --- |
| Database Name | ontology |
| Table Name | logging.combined_agent_details |

# Column Summary

| Column Name | Data Type | Nullable | Distinct Count | Null Count | Null % | Min | Max | Average |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| id | bigint | NO | 3 | 0 | 0.00 | 482731 | 583271 | 516424.33 |
| project_key | character varying | YES | 1 | 0 | 0.00 | AP | AP |  |
| ticket_key | character varying | YES | 3 | 0 | 0.00 | AP-11 | AP-14 |  |
| ticket_id | character varying | YES | 3 | 0 | 0.00 | 10127 | 10194 |  |
| ticket_url | text | YES | 3 | 0 | 0.00 | https://kiranascendiondemo.atlassian.net/browse/AP-11 | https://kiranascendiondemo.atlassian.net/browse/AP-14 |  |
| github_owner | character varying | YES | 1 | 0 | 0.00 | kiranascendion | kiranascendion |  |
| github_repository | character varying | YES | 1 | 0 | 0.00 | Data-Migration-Assets | Data-Migration-Assets |  |
| github_branch | character varying | YES | 1 | 0 | 0.00 | main | main |  |
| github_file_path | text | YES | 1 | 0 | 0.00 | output/DMcard Wave Spreadsheet-WAVE Updated.xlsx | output/DMcard Wave Spreadsheet-WAVE Updated.xlsx |  |
| attachment_id | character varying | YES | 3 | 0 | 0.00 | 10074 | 10140 |  |
| attachment_name | text | YES | 1 | 0 | 0.00 | DMcard Wave Spreadsheet-WAVE Updated.xlsx | DMcard Wave Spreadsheet-WAVE Updated.xlsx |  |
| attachment_status | character varying | YES | 1 | 0 | 0.00 | success | success |  |
| status | character varying | YES | 1 | 0 | 0.00 | success | success |  |
| error_message | text | YES | 1 | 0 | 0.00 |  |  |  |
| diagnostic_logs | jsonb | YES | 3 | 0 | 0.00 | ["Agent 1 validated successfully", "Agent 2 validated successfully", "Combined Agent 1 Jira ticket data with Agent 2 GitHub attachment data", "Preserved original values from both agents", "Using existing PostgreSQL destination ontology.logging.combined_agent_details", "No schema or table creation performed", "Sensitive credentials were not exposed"] | ["Read Jira ticket details from GitHub file: Jira Ticket Details/jira_ticket_details.txt", "Validated mandatory fields: project_key, summary, description", "Used provided issue_type: Task", "Invoked Jira Ticket Creator tool with sanitized inputs", "Jira project validated and issue created successfully", "Captured normalized Jira response including ticket key, ticket id, project name, and ticket URL", "Validated existing Jira ticket key AP-14 before attachment", "Validated GitHub repository access for kiranascendion/Data-Migration-Assets", "Validated GitHub branch main", "Validated GitHub file path output/DMcard Wave Spreadsheet-WAVE Updated.xlsx", "Downloaded the exact requested GitHub file for attachment", "Attached file to existing Jira ticket AP-14 without creating a new ticket", "Verified attachment success with attachment ID 10140 and attachment name DMcard Wave Spreadsheet-WAVE Updated.xlsx", "Sanitized all logs and did not expose credentials or authorization data"] |  |
| created_at | timestamp without time zone | YES | 3 | 0 | 0.00 | 2026-08-18 04:58:16.309494 | 2026-08-19 05:27:04.776696 |  |

# Value Distribution Summary

## status

| Value | Frequency |
| --- | --- |
| success | 3 |

## attachment_status

| Value | Frequency |
| --- | --- |
| success | 3 |

## github_branch

| Value | Frequency |
| --- | --- |
| main | 3 |

# Date Statistics

| Column Name | Min Date | Max Date | Distinct Count |
| --- | --- | --- | --- |
| created_at | 2026-08-18 04:58:16.309494 | 2026-08-19 05:27:04.776696 | 3 |

# Text Statistics

| Column Name | Min Length | Max Length | Average Length |
| --- | --- | --- | --- |
| project_key | 2 | 2 | 2.00 |
| ticket_key | 5 | 5 | 5.00 |
| ticket_id | 5 | 5 | 5.00 |
| ticket_url | 53 | 53 | 53.00 |
| github_owner | 14 | 14 | 14.00 |
| github_repository | 21 | 21 | 21.00 |
| github_branch | 4 | 4 | 4.00 |
| github_file_path | 48 | 48 | 48.00 |
| attachment_id | 5 | 5 | 5.00 |
| attachment_name | 41 | 41 | 41.00 |
| attachment_status | 7 | 7 | 7.00 |
| status | 7 | 7 | 7.00 |
| error_message | 0 | 0 | 0.00 |