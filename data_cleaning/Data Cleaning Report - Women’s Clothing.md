# Data Cleaning Report - Women’s Clothing

# Initial Summary

**File Name:** us-shein-womens_clothing-4620

**Data Source:** Sourced from [Kaggle.com](https://www.kaggle.com/datasets/oleksiimartusiuk/e-commerce-data-shein?select=us-shein-womens_clothing-4620.csv) in csv file format.

**Grain:** Each row presents a women’s clothing item

**Size:** 4623 rows, 8 columns

[https://www.kaggle.com/datasets/oleksiimartusiuk/e-commerce-data-shein?select=us-shein-womens_clothing-4620.csv](https://www.kaggle.com/datasets/oleksiimartusiuk/e-commerce-data-shein?select=us-shein-womens_clothing-4620.csv)

---

# Data Cleaning Steps Taken

**Tools Used:** Microsoft Excel, Power Query

### Fixes & Transformations

| Issue | Action Taken | Example |
| --- | --- | --- |
| Negative percentages in the discount column | Applied the absolute value function in power query to convert to positive | -30% → 30% |
| Duplicate transactions  | Removed 394 duplicate rows |  |

### Missing Data Handling

| Column | % Missing | Action Taken | Justification |
| --- | --- | --- | --- |
| Product_Name | <1% | Removed the records | These records had missing data in more than one column |
| Discount | 67% | Populated it with 0% | Not every item is discounted under normal circumstances |


### “Before vs After” Snapshot

| Metric | Before | After | **Change / Notes** |
| --- | --- | --- | --- |
| Row Count | 4623  | 4227 |  |
| Column Count | 8 | 11 | Removed 5 columns
Added 8 columns |
| Missing Values (Total) | 2 | 0 | Removed 2 rows with more than 2 columns with missing values |
| Duplicate Rows | 394 | 0 |  |
| Data Types Corrections | - | - |  |
| Date Formats (Variants) | - | - |  |
| Outliers or Obvious Errors | 6 `Price` values were $0 | - | Filled rows with Mean Imputation |
| Manual Fixes | - | 3 label correction | E.g., “goods-title-link” → “Product_Name” |
| Numeric Columns Stored as Text | 4227 rows | 0 rows | Text in `Price` column
Converted all to numeric |


---

# Final Data Summary

**Final Row Count:** 4227

**Final Column Count:** 11

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
