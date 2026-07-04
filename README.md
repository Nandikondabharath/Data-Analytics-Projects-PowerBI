# Data Analytics Projects - Power BI

This repository contains a Power BI project and the source sales data used to build the report. Below is a concise summary of the analysis and guidance for stakeholders, followed by descriptions for the files included in this repo.

## Key findings and recommendations

- Classic Cars leads all categories — $3.92M, 39.07% of total sales, more than double the next line (Vintage Cars, 18.97%). Risk: over-reliance on one product line.

- USA is the top market — $3.63M, 36.16% of total sales, more than Spain + France + Australia combined. Note: Territory field shows EMEA at 49.63% only because USA/Canada aren't tagged — fix before publishing.

- Medium deals are most efficient — 49% of orders → 61% of revenue. Small deals: 45% of orders → only 26% of revenue. Recommendation: prioritize moving Small-deal customers toward Medium-sized deals.

- November is peak season — 21.12% of total sales, nearly 2x October (11.18%) and ~5x June (4.53%). Plan inventory and marketing around Q4.

- Top 5 customers account for 21.39% of revenue (out of 92 total customers), led by Euro Shopping Channel alone at 9.09%. Key-account risk — protect these relationships.

- 92.61% of orders shipped cleanly; Cancelled + Disputed = ~$266.7K at risk (2.66% combined).

- 2003 → 2004 grew ~34% ($3.52M → $4.72M). 2005 figure ($1.79M) is partial-year (Jan–May only) — do not interpret it as a decline.


## Files in this repository

- PowerBI_Project1.pbix — Power BI report

  Description: Interactive Power BI report that contains the dashboards, visuals, data model, and measures used to produce the analysis above. Report pages include product-line performance, market / territory analysis, deal-size efficiency, seasonality, top-customer / key-account views, and shipment status. Use the included report to explore the findings; verify and correct the Territory tagging (USA/Canada) in the source data before publishing.

- Sales.xlsx — Source sales dataset (order-level)

  Description: Excel workbook containing the underlying transactional data used by the Power BI report. Expected fields include OrderDate, ProductLine, Territory, Market, Customer, OrderValue, OrderStatus (Shipped/Canceled/Disputed), ShipDate, and related dimensions. Note: the Territory field currently does not tag USA/Canada consistently — clean/tag these records before final reporting.


## Notes for reviewers / publishers

- The Territory issue (USA/Canada not tagged) inflates EMEA share; correct the Territory field in the Sales.xlsx file or in the ETL step before publishing any public-facing dashboards.

- The 2005 aggregate in the data is partial (Jan–May) and should not be compared directly to full-year figures for 2003–2004.

---

