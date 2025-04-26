#Data  Cleaning Report - Men’s Clothing

# Initial Summary

**File Name:** us-shein-mens_clothes-1891

**Data Source:** Sourced from [Kaggle.com](https://www.kaggle.com/datasets/oleksiimartusiuk/e-commerce-data-shein?select=us-shein-womens_clothing-4620.csv) in csv file format.

**Grain:** Each row presents a men’s clothing item

**Size:** 1890 rows, 7 columns

[https://www.kaggle.com/datasets/oleksiimartusiuk/e-commerce-data-shein?select=us-shein-mens_clothes-1891.csv](https://www.kaggle.com/datasets/oleksiimartusiuk/e-commerce-data-shein?select=us-shein-mens_clothes-1891.csv)

---

# Data Cleaning Steps Taken

**Tools Used:** Microsoft Excel, Power Query

### Fixes & Transformations

| Issue | Action Taken | Example |
| --- | --- | --- |
| Negative percentages in the discount column | Applied the absolute value function in power query to convert to positive | -30% → 30% |
| Duplicate transactions  | Removed 584 duplicate rows |  |


### Missing Data Handling

| Column | % Missing | Action Taken | Justification |
| --- | --- | --- | --- |
| Product_Name | <1% | Removed the records | These records had missing data in more than one column |
| Discount | 1% | Populated it with 0% | Not every item is discounted under normal circumstances |


### “Before vs After” Snapshot

| Metric | Before | After | **Change / Notes** |
| --- | --- | --- | --- |
| Row Count | 1890 | 1305 |  |
| Column Count | 7 | 11 | 4 columns removed
8 columns added |
| Missing Values (Total) | 1 | 0 | Removed 1 rows with more than 2 columns with missing values |
| Duplicate Rows | 584 | 0 |  |
| Data Types Corrections | - | - |  |
| Date Formats (Variants) | - | - |  |
| Outliers or Obvious Errors | - | - |  |
| Manual Fixes | - | 3 label corrections | E.g., “goods-title-link” → “Product_Name” |
| Numeric Columns Stored as Text | 1305 | 0 | Fixed data types for `Price` |

---

# Final Data Summary

**Final Row Count:** 1890

**Final Column Count:** 1305

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
