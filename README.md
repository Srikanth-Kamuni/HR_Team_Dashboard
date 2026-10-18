# HR Team Performance Dashboard

Excel-based HR reporting project analyzing **171 employee records** across seven departments and joining years **2020–2025**.

## Business problem
HR teams need a consistent view of employee status, workforce movement and composition across departments, managers and joining cohorts. This dashboard organizes employee-level records into summarized views for exploratory workforce reporting.

## Project objectives
- Track on-board, attrition and transfer records.
- Compare joining-year, department, grade and employment-type distributions.
- Review manager-level employee counts.
- Identify data quality and privacy limitations.

## Workbook structure
| Worksheet | Purpose |
|---|---|
| Dashboard | Visual HR reporting interface |
| Calculations | Pivot-style summary tables |
| Data | 171 records, 16 fields |

## Key findings
| Metric | Value |
|---|---:|
| Employee records / distinct IDs | 171 |
| On-Board | 118 (69.01%) |
| Attrition | 47 (27.49%) |
| Transfer | 6 (3.51%) |
| Permanent | 148 |
| Contract | 23 |
| Male (Category field) | 107 |
| Female (Category field) | 64 |

**Interpretation:** These are status proportions in the dataset, **not annual employee attrition rates**. The source snapshot date is unspecified.

## Data dictionary
| Field | Description |
|---|---|
| Emp Status | Recorded status: On-Board, Attrition or Transfer; snapshot interpretation requires a reporting date. |
| Movement | Employee movement label (e.g., IJP, OnRoll); 146 blank values; source definitions not provided. |
| Emp Id | Employee identifier; 171 unique values. Remove from public sample data. |
| Name | Employee name; personal data, not suitable for public sharing. |
| Date of Joining | Recorded employment start date; Excel date field. |
| Data of Relieving | Column name as provided; likely departure date. Verify definition and inconsistent records. |
| Reporting Manager | Manager name; personal information requiring protection. |
| Emp Type | Employment type, Permanent or Contract. |
| Category | Contains Male/Female values; functions as a gender field in this dataset. |
| Date of Birth | Birth date; sensitive personal information; verify anomalous dates. |
| Marital status | Recorded marital status; personal information; not essential to public dashboard. |
| Grade | Employee grade: Trainees, Professional, Management or Contract. |
| Department | Organizational department, e.g., Operations, HR or Sales. |
| Total Experience | Numeric experience measure; units and calculation basis not stated. |
| Year | Joining-year grouping in workbook. |
| Stability | Categorical labels from 1+ years to 5+ years; calculation methodology not documented. |

## KPI definitions
- **Employee count:** Count of nonblank, distinct `Emp Id` values.
- **On-board count:** Count of `Emp Status = On-Board`.
- **Attrition records:** Count of `Emp Status = Attrition`.
- **Transfer records:** Count of `Emp Status = Transfer`.
- **Status share:** Status count / total records × 100.
- **Department distribution:** Employee record count grouped by `Department`, with status filters as appropriate.

## Data quality and limitations
- 171 unique employee IDs; 146 missing `Movement` values and 125 missing `Data of Relieving` values.
- `Category` stores Male/Female values and is therefore a gender-like variable despite its name.
- Some dates of birth appear inconsistent with joining dates and should be verified.
- `Stability` and `Total Experience` lack a documented calculation methodology.
- This is a snapshot-style analysis; no validated time-based attrition rate can be inferred.
- **Privacy:** Do not publish the original workbook without authorization. It contains employee names, IDs, dates of birth, reporting-manager names and other personal details. Replace with synthetic or properly anonymized data before public release.
- The workbook is `.xlsm`; review its macros before distributing it.

## Tools
Microsoft Excel, PivotTables / pivot-style calculations, dashboard visualizations, macro-enabled workbook.

## Repository contents
```text
HR-Team-Performance-Dashboard/
├── README.md
├── HR_Team_Project_Documentation.pdf
└── HR_Team_Dashboard.xlsm   # only if publication is authorized and data sanitized
```

## Portfolio description
Developed an Excel HR performance dashboard using 171 employee records to analyze workforce status, attrition records, transfers, department distribution and employee characteristics across joining cohorts.
