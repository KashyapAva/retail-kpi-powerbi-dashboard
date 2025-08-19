# Retail KPI Dashboard (Power BI)

A business-ready KPI dashboard for a retail scenario. Built a star-schema semantic model (daily + monthly grains), custom DAX measures, and executive/marketing/category views.

## 📊 Pages
1) **Executive KPI Overview** – Revenue, Orders, AOV, Gross Margin %, Conversion Rate, % to Target Revenue, trends.  
2) **Marketing & Growth** – Sessions, CAC, ROAS, Returns, Revenue MoM %, Rolling 3M Avg.  
3) **Category & Monthly Breakdown** – Matrix with conditional formatting, Top N, Category trend.

## 🧠 Measures (highlights)
Revenue · COGS · Gross Margin % · Orders Count · AOV · Returns Amount · **Net Revenue** · **Returns % of Orders** · Total Sessions · Total Marketing Spend · **Conversion Rate** · **CAC** · **ROAS** · **Revenue MoM %** · **Revenue/Net Revenue YoY %** · **Rolling 3M Avg** · Target Revenue · % to Target Revenue.

## 🔧 Model notes
- Calendar (daily) & CalendarMonth (monthly) with bridge `Calendar[Month] → CalendarMonth[Month]`.
- Relationships: Many-to-one, Single direction; `Orders` ↔ `Products`, `Customers`, `Calendar`.
- Safe DAX (`DIVIDE`) to handle missing months; optional filter to **show only months with orders**.

## 🖼️ Previews
![Executive](screenshots/page1-executive.png)
![Marketing](screenshots/page2-marketing.png)
![Category](screenshots/page3-category.png)

## 🧩 Files
- `Retail_KPI_Dashboard.pbix`
- `/screenshots/*`
- `/data/*` (sample data only)

> Built in Power BI Service (Fabric web). Dataset is synthetic/anonymized.
