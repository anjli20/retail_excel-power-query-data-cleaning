# Excel Power Query – Sales Data Cleaning

A hands-on data cleaning and transformation project built entirely in **Excel Power Query Editor**, using a multi-table retail sales dataset (customers, products, stores, regions, returns and transactions for 1997–1998).

The goal: take raw, messy CSV files and turn them into a clean, analysis-ready data model with **no formulas and no VBA**, just Power Query's ETL (Extract → Transform → Load) pipeline, which refreshes automatically when new data lands in the source folder.

---

## Dataset

The dataset contains 7 CSV files, loaded together using **Get Data → From Folder**:

| Table | Description |
|---|---|
| `Customers` | Customer details: name, city, state, birth date, marital status, gender, children, education, membership card, occupation, homeowner status |
| `Products` | Product ID, brand, name, SKU, retail price, cost, weight, recyclable and low-fat flags |
| `Regions` | Sales districts and sales regions |
| `Stores` | Store ID, region, store type, name, street, city, state |
| `Returns` | Return date, product ID, store ID, quantity returned |
| `Transactions_1997` | Transaction date, stock date, product ID, customer ID, store ID, quantity |
| `Transactions_1998` | Same structure as 1997 |

---

## Key Concepts Covered

- **ETL pipeline**: Extract, Transform, Load, with auto-refresh on new data
- **Applied Steps**: every transformation is recorded and replayed on new data
- **Transform vs Add Column**: modify in place vs create a new derived column
- **Append vs Merge**: stack rows vertically vs join columns horizontally
- **Join types**: Left Outer, Right Outer, Inner, Full Outer, Left Anti, Right Anti
- **Locale-aware type conversion** for date formats that differ by region
- **Handling nulls with context** instead of blindly deleting or filling them
- **M language** (Mashup), the language behind Power Query
