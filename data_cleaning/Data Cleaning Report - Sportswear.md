# Data Cleaning Report - Sportswear

# Initial Summary

**File Name:** **us-shein-sports_and_outdoors-3853**

**Data Source:** Sourced from [Kaggle.com](https://www.kaggle.com/datasets/oleksiimartusiuk/e-commerce-data-shein?select=us-shein-womens_clothing-4620.csv) in csv file format.

**Grain:** Each row presents a men’s clothing item

**Size:** 3857 rows, 11 columns

[https://www.kaggle.com/datasets/oleksiimartusiuk/e-commerce-data-shein?select=us-shein-sports_and_outdoors-3853.csv](https://www.kaggle.com/datasets/oleksiimartusiuk/e-commerce-data-shein?select=us-shein-sports_and_outdoors-3853.csv)

---

# Data Cleaning Steps Taken

**Tools Used:** Microsoft Excel, Power Query

### Fixes & Transformations

| Issue | Action Taken | Example |
| --- | --- | --- |
| Negative percentages in the discount column | Applied the absolute value function in power query to convert to positive | -30% → 30% |
| Duplicate transactions  | Removed 20 duplicate rows |  |
|  |  |  |

### “Before vs After” Snapshot

| Metric | Before | After | **Change / Notes** |
| --- | --- | --- | --- |
| Row Count | 3857 | 3634 |  |
| Column Count | 11 | 11 | 8 columns removed
8 columns added |
| Missing Values (Total) | 20 | 0 | All columns had missing values |
| Duplicate Rows | 203 | 0 |  |
| Data Types Corrections | - | - |  |
| Date Formats (Variants) | - | - |  |
| Outliers or Obvious Errors | `Price` values were $0 | - | Filled rows with Mean Imputation |
| Manual Fixes | - | 3 label corrections | E.g., “goods-title-link” → “Product_Name” |
| Numeric Columns Stored as Text | 3634 | 0 | Fixed data types for `Price` |
|  |  |  |  |

---

# Final Data Summary

**Final Row Count:** 3857

**Final Column Count:** 3634

**Key Improvements:** 

- Converted prices from text to numeric
- Renamed Column Headers
- Added new columns with synthetic for analysis purposes:
    - Product_ID
    - Product_Type
    - Category
    - Brand
    - Final_Price
    - Units_Sold
    - Revenue
    - Region
- Addressed missing values in key columns

---

# Assumptions & justifications

- None
