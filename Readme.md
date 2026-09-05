# Maven Sales Analysis
## Introduction

This project analyzes sales performance for Maven Toys, a toy and 
games retailer, to uncover revenue trends, top and bottom performing 
products, category performance, and daily/monthly sales patterns.

The full dashboard is available in [Maven_Toys_Dashboard.xlsx](./Maven_pj.xlsx).

### Problems I solved
- I tracked the business KPI (Key Performance Indicators) 
- Product analysis to uncover best and worst performing products.
- The busines growth rate 
- Sales and Revenue Trend


### Dataset

The dataset covers  sales for Maven Toys, including:
- **Sales:** individual transaction records (product, store, date, units)
- **Products:** name, category, cost, and price
- **Stores:** location and store details
- **Categories:** Toys, Art & Crafts, Electronics, Games, Sports & Outdoors

Note that the dataset starts from January 2022 and ends in September 2023.

### Excel Skills Used

- **Charts** (line, bar, donut):
I used these to display my analysis while highlighting the KPIs. Line 
charts are for trends, bar charts are for categories and their 
respective figures, while the donut chart is for product category 
percentage breakdown.

- **PivotTable**:
The major backbone of my analysis, showcasing advanced skills beyond 
basic formulas.

- **Slicers** (Year filter):
The year slicer is connected to every chart, allowing smooth 
interaction across all visuals based on the selected year.

- **Power Query**:
My backbone for data cleaning . using Trim to clean columns and 
converting each column to its necessary format.

- **Data Modeling**:
With data modeling in Excel, I was able to create relationships among 
the tables for seamless analysis across them. I also created a proper 
date table for accurate time intelligence analysis.

- **DAX Functions and Measures**:
I made full use of the DAX function pane, creating a monthly growth 
rate measure, along with other measures for the KPIs.

Monthly growth rate:
```
=DIVIDE(
[TOTAL REVENUE]-[Revenue_PM],
[Revenue_PM]
)
```

## Data Cleaning Process

For my data cleaning, I used Power Query. I used Trim in the 
Transformation pane to remove unnecessary spaces in the 
`store_location` and `store_city` columns in `store_dim`.

After trimming the columns, I proceeded to capitalize the first letter 
of each word to avoid ambiguity, which could later lead to duplication 
in my analysis due to case sensitivity.

I also ensured that each column maintained its correct format for 
example, changing the date column in `sales_dim` from text to date 
format, and changing `product_price` and `product_cost` from number 
to currency format.

## Analysis 
- ### The Business KPI:

        - Total Revenue: $14,444,572
        - Total Quantity: 1,090,565
        - Total Orders: 829,262
        - Total Profit: $4,014,029 
This is the total key performance of Maven-Toys for the 1 year and 9 months.Its not really a bad performance but can improve its profit efficiency by minimizing product_cost since there is a huge difference in revenue($14M) and profit ($4M).

- ### Best ans Worst performing products:

Best performer: Lego Bricks ($1.33M), followed by Colorbuds ($1.13M)  both far ahead of the rest.

Worst performer: Uno Card Game ($21,653), alongside other traditional board/card games (Classic Dominoes, Chutes & Ladders) at the bottom.

Analysis: Top sellers are higher-ticket toys and electronics, while the weakest performers are consistently classic board/card games pointing to a category-level trend rather than a single weak product. Marketing and inventory spend may be better focused on proven winners like Lego Bricks and Colorbuds.

- ### Monthly Business Growth Rate:

**Monthly Growth: 2022 vs 2023**

Both years follow the same seasonal shape: a post-holiday dip (Jan–Feb), a spring rebound (March), a mid-year lull, and a dip before recovery. 2022 closes strong with a **33% December surge** ,clear holiday-driven demand. 2023 (through September) mirrors this pattern early on, but its **August dip (-20%) fails to rebound as strongly as 2022's did**  September 2023 recovers to just 0%, versus +20% in the same stretch a year earlier.

**Insight:** The business has a reliable, repeatable seasonal cycle tied to holiday gifting, not random fluctuation. But 2023's weaker August–September recovery is a deviation from that pattern  worth investigating (inventory, marketing spend, or shifting demand) rather than assuming it's normal seasonality.

**Recommendation:** Double down on Q4 marketing and stock readiness, since December is consistently the biggest driver of growth. At the same time, review what changed operationally around August–September 2023, since a weaker rebound there could signal an early warning sign heading into the next holiday season.

- ### Sales and Trend Analysis
Sales & Revenue Analysis: 2022 vs 2023

2022 generated $7.48M in revenue across 549,492 units and 420,845 orders (full year). 2023, despite covering only 9 months, already reached $6.96M in revenue with 541,073 units and 408,417 orders , nearly matching 2022's full-year totals in three-quarters of the time.

Insight: 2023's pace significantly outperforms 2022 on a like-for-like basis if the trend holds, full-year 2023 revenue could surpass 2022 once Q4 (typically the strongest quarter) is included. Order volume and units sold are tracking closely with 2022 as well, suggesting the growth is broad-based rather than driven by a few high-price items.

Recommendation: Maintain current inventory and marketing momentum into Q4, since 2023 is already outpacing 2022's pace , a strong holiday season could push full-year performance well ahead of the prior year rather than just matching it.

## Conclusion

This project strengthened my ability to build an interactive Excel 
dashboard and validate insights against raw transactional data. The 
findings can help Maven Toys plan inventory and marketing efforts 
around its clear seasonal demand pattern. Also strenghtened my advance excel skill such as data modelling,power query, dax, pivot tables and measures.