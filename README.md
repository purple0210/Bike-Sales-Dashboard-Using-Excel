# Bike Sales Dashboard Using Excel 🚲📊

An Excel-based analytics project that explores customer demographics and purchasing behavior for a bicycle retailer, and rolls the findings up into a single-page interactive dashboard.

## Overview

This workbook (`Excel_Project_DASHBOARD.xlsx`) takes a raw customer dataset and turns it into actionable insight through data cleaning, pivot tables, and dashboard visualizations — all built natively in Excel using formulas, PivotTables, and PivotCharts (no macros or external tools required).

## File

- **`Excel_Project_DASHBOARD.xlsx`** — the complete workbook

## Workbook Structure

The workbook is organized into four sheets that represent the analytics pipeline from raw data to finished dashboard:

| Sheet | Purpose |
|---|---|
| `bike_buyers` | Raw source data — one row per customer (1,026 records) |
| `Working Sheet` | Cleaned/transformed copy of the data with derived columns for analysis |
| `Pivot Table` | PivotTables and PivotCharts summarizing the data along key dimensions |
| `Dashboard` | Final presentation layer combining the key charts into one view |

### `bike_buyers` (raw data)

Each row represents a customer record with the following fields:

| Column | Description |
|---|---|
| ID | Unique customer identifier |
| Marital Status | Married (M) / Single (S) |
| Gender | M / F |
| Income | Annual income |
| Children | Number of children |
| Education | Highest education level attained |
| Occupation | Job category |
| Home Owner | Yes / No |
| Cars | Number of cars owned |
| Commute Distance | Distance band from home to work |
| Region | Europe / Pacific / North America |
| Age | Customer age |
| Purchased Bike | Yes / No — target field |

### `Working Sheet`

A cleaned copy of the raw data with values normalized for readability (e.g. `M`/`S` expanded to `Married`/`Single`, `M`/`F` expanded to `Male`/`Female`) plus one derived column:

- **Age Brackets** — customers grouped into `Adolescent`, `Middle Age`, and `Old` buckets

This sheet feeds all of the PivotTables and PivotCharts in the rest of the workbook.

### `Pivot Table`

Several PivotTables built from the `Working Sheet` data, breaking down purchase behavior by:

- **Gender** — average income of buyers vs. non-buyers
- **Commute Distance** — count of purchases by distance band
- **Age Bracket** — count of purchases by age group
- **Age (individual)** — count of purchases by exact age

These feed the three PivotCharts used on the dashboard.

### `Dashboard`

A single-page summary combining the key charts for at-a-glance insight:

- **Average Income Per Purchase** (bar chart) — average income split by gender and purchase outcome
- **Customer Commute** (line chart) — bike purchases across commute-distance bands
- **Customer Age Brackets** (line chart) — bike purchases across age groups

## Key Insights

- Buyers skew toward **shorter commute distances** (0–1 miles has the highest purchase count).
- The **Middle Age** bracket accounts for the largest share of both buyers and non-buyers.
- **Male buyers** have a noticeably higher average income than male non-buyers; the gap is smaller for female customers.

## How to Use

1. Download and open `Excel_Project_DASHBOARD.xlsx` in Excel (2007+) or a compatible spreadsheet application.
2. Start on the **Dashboard** sheet for the high-level summary.
3. Explore **Pivot Table** to drill into a specific breakdown, or use the field list / slicers (if present) to filter by other attributes.
4. Refer to **Working Sheet** / **bike_buyers** to inspect or extend the underlying data — the PivotTables can be refreshed (right-click → *Refresh*) after any changes.

## Tools Used

- Microsoft Excel — PivotTables, PivotCharts, formulas

## License

Feel free to use and adapt this project for learning or portfolio purposes.

