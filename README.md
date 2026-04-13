# BIG DATA ANALYSIS

COMPANY: CODTECH IT SOLUTIONS

NAME: PRACHI SONONE

INTERN ID: CTIS2104

DOMAIN: DATA ANALYTICS

DURATION: 16 WEEKS

MENTOR: NEELA SANTHOSH KUMAR

A data analysis project on a used cars dataset using PySpark in Google Colab. The notebook goes through basic exploration, filtering, aggregation, feature engineering, and exporting the final dataset.

---

## Dataset

**File:** `cars_data_set.csv`  
**Size:** 10,000 rows, 10 columns

| Column | Description |
|---|---|
| Car_Id | Unique identifier for each car |
| Car_Name | Name/model of the car |
| Year | Manufacturing year |
| Selling_Price_Lakh | Price at which the car is being sold (in lakhs) |
| Present_Price_Lakh | Current ex-showroom price (in lakhs) |
| Kms_Driven | Total kilometers driven |
| Fuel_Type | Petrol / Diesel / CNG |
| Seller_Type | Dealer or Individual |
| Transmission | Manual or Automatic |
| Owner | Number of previous owners |

---

## What's Covered

The notebook runs through 20 analysis tasks:

1. Display top 3 rows
2. Check data types with `printSchema()`
3. List column names
4. Count rows and columns
5. Summary statistics with `describe()`
6. Unique values in the Transmission column
7. Count of unique Fuel_Type values
8. Select a single column
9. Select multiple columns
10. Create a `Usage_Level` column based on kilometers driven - Lightly used (≤10,000 km), Moderately used (≤50,000 km), Heavily used (>50,000 km)
11. Rename `Year` to `Manufacture_Year`
12. Filter cars with selling price > 5.50 lakh
13. Filter by price and show transmission type
14. Filter manual cars with selling price > 5.50 lakh
15. Filter automatic cars with selling price > 5.50 lakh
16. Average selling price grouped by transmission type
17. Petrol cars sold by dealers
18. Min and max present price grouped by fuel type
19. All cars sorted by selling price (descending)
20. Car count grouped by seller type

The updated dataset (with the new `Usage_Level` column) is saved as `cars_updated_dataset.csv` at the end.

---

## Key Findings

- Automatic cars average 4.78 lakh in selling price; manual cars average 1.98 lakh
- Dealers account for 6,362 listings vs 3,638 from individual sellers
- The highest-priced car is a 2010 Land Cruiser listed at 35 lakh
- Diesel cars have the widest price range, present price goes up to 93.78 lakh
- CNG cars sit in a narrow range: 5.09 to 7.74 lakh (present price)

---

## Tech Stack

- Python 3
- PySpark 4.0.2
- Google Colab
- pandas (used for `.toPandas()` conversions)

---

## How to Run

1. Open the notebook in Google Colab
2. Upload `cars_data_set.csv` to your Google Drive
3. Update the file path in the `spark.read.csv(...)` cell to match your Drive location
4. Run all cells in order

Install PySpark if it's not already available:
```bash
!pip install pyspark
```

---

