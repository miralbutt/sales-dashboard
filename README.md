
# Sales Dashboard (Power BI)

A clean dataset to build a regional sales dashboard in **Power BI** (or Excel / Tableau).

## Files
- `sales_data.csv` — daily sales by region and product

## Suggested KPIs
- Total Revenue, Units Sold, Average Selling Price
- Revenue by Region, Revenue by Product
- Month-over-Month growth, YoY (if you extend data)

## Power BI Steps
1. Open Power BI Desktop → Get Data → CSV → select `sales_data.csv`
2. Model: set `date` as Date type; create relationships if you add a Date table
3. Create the following DAX measures (examples):
   ```DAX
   Total Revenue = SUM(sales_data[revenue])
   Total Units = SUM(sales_data[units_sold])
   Avg Price = DIVIDE([Total Revenue], [Total Units])
   ```
4. Build visuals: Cards for KPIs, Bar chart by Region, Line chart by Date, Matrix by Product/Region
5. Publish to Power BI Service (optional)

## Next Ideas
- Add a Date dimension and time intelligence measures
- Forecasting with Python visuals inside Power BI
