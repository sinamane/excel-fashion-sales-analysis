# Dataset Documentation

## 📜Data Dictionary

| Column Name | Description | Example |
| --- | --- | --- |
| `Prouct_ID` | Unique identifier for each product | `M001` |
| `Product_Name` | The name of the product | `Manfinity Homme Loose Fit Men's Solid Color Button Up Shirt` |
| `Product_Type` | Categorizes products by their product types | `Shirt` |
| `Category` | Broader category that the product belongs | `Men's Clothes` |
| `Brand` | Simulated name for each category | `Loopline` |
| `Price` | Cost of product | `$11,99` |
| `Discount` | Discount percentage | `7%` |
| `Final_Price` | Cost after applying discount: `=Price × (1 - Discount%)` | `$11,150` |
| `Units_Sold` | Simulated with `=Price × (1 - Discount%)` | `420` |
| `Revenue` | `=Units Sold × Final Price` | `$4683,29` |
| `Region` | North, South, East, West | `North` |

## 🧠Data Assumptions

- Missing product `Price` values were imputed using average price per product
- Products without a precise `type` were labeled as `Other`

## ✅ Data Checks

- **Missing Values**
    - Checked all columns; missing values filled or flagged appropriately
- **Outliers**
    - Flagged transactions with `Price` for manual review

## 🔗Combine Process Summary

- **Files Combined**: 3 Excel files
- **Merge Method**: Vertically concatenated using consistent schema
- **Rows**: ~9369 combined rows

## ❓Key Questions / EDA Hypotheses

1. Which product categories drive the most revenue?
2. Which brands have the highest units sold vs. highest revenue?
3. Do larger discounts lead to more units sold?
4. Which regions perform best by total revenue and units sold?
5. Are certain product types consistently priced higher than others?
6. What’s the average discount per category or brand?
7. Are there outlier products that sell extremely well (or poorly)?
