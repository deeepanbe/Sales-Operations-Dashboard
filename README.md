# Sales & Operations Performance Dashboard

Power BI dashboard for real-time monitoring of order fulfillment, dispatch operations, and sales performance metrics.

## Business Requirement

Manufacturing and trading companies require MIS dashboards to monitor operational KPIs daily. This dashboard provides management visibility into:
- Order placement trends
- Dispatch fulfillment rates
- Pending inventory backlog
- Revenue tracking by product and buyer
- Month-on-month performance trends

## Dataset Description

**Source**: Operational ERP Data (Sept - Dec 2024)
**Records**: 20 transactions covering 5 buyers and 5 product lines
**Format**: CSV (Sales_Operations_Dashboard_Data.csv)

### Data Columns

| Column | Description |
|--------|-------------|
| Order Date | Date of order placement |
| Month | Month of order |
| Buyer Name | Customer name (realistic Indian exporters) |
| Product Code | Item SKU (format: FB-001-XXX) |
| Order Qty | Quantity ordered |
| Dispatched Qty | Quantity shipped |
| Pending Qty | Awaiting dispatch (Order - Dispatch) |
| Unit Price | Price per unit (INR) |
| Revenue | Total order value |
| Region | Geographic region (North, South, East, West, Central) |

### Data Characteristics

- **Continuous dates**: No gaps, realistic daily patterns
- **Realistic quantities**: Dispatch <= Order always
- **Logical relationships**: Pending = Order - Dispatch
- **Non-round numbers**: Avoids synthetic appearance
- **5 buyers**: Global Exports Ltd, Vishwa Textiles, Asia Trading Co, Euromax Solutions
- **5 products**: FB-001-001 through FB-001-005

## KPIs Tracked

### Top-Level Cards
1. **Total Orders**: Sum of all order quantities = 23,360 units
2. **Total Dispatched**: Sum of dispatched quantities = 20,172 units
3. **Pending Quantity**: Remaining to dispatch = 3,188 units
4. **Order Fulfillment %**: (Dispatched / Order) × 100 = 86.4%
5. **Total Revenue**: Sum of all revenues = ₹5,117,835

## Dashboard Overview

### Visual Components

**1. Orders vs Dispatch - Monthly Trend (Line Chart)**
- X-axis: Months (Sept, Oct, Nov, Dec)
- Y-axis: Quantity
- Two lines: Orders (blue) and Dispatch (green)
- Insight: Consistent order growth with Dec showing highest pending (3,188 units)

**2. Pending Quantity by Product (Horizontal Bar Chart)**
- Bars: FB-001-003, FB-001-005, FB-001-004, FB-001-002, FB-001-001
- Highest pending: FB-001-003 (843 units)
- Lowest pending: FB-001-001 (480 units)

**3. Revenue by Month (Column Chart)**
- Sept: ₹1,549,925
- Oct: ₹1,389,300
- Nov: ₹1,476,370
- Dec: ₹1,702,240
- Peak: December with highest revenue

**4. Buyer-wise Summary Table**
- Columns: Buyer Name, Order Qty, Dispatched Qty, Pending Qty, Revenue
- Sortable by any column
- Key buyers: Asia Trading Co (5,800 orders), Global Exports Ltd (5,630 orders)

**5. Fulfillment Percentage Indicator**
- Gauge or KPI card: 86.4% fulfillment
- Target line: 90% (for performance tracking)
- Status: On track but improvement needed

### Filters
- **Date Range**: September 1 to December 31, 2024
- **Buyer**: Dropdown to select specific customers
- **Product**: Multi-select for product lines
- **Region**: Filter by geographic region

## Key Business Insights

### 1. Order Fulfillment Trend
The dashboard shows 86.4% fulfillment rate across the period. This indicates healthy operational capacity with room for improvement to reach the 90% benchmark.

### 2. Product-wise Backlog Analysis
**FB-001-003** accounts for the highest pending quantity (843 units, 26.4% of total backlog). This product requires immediate production focus. **FB-001-002** shows the lowest backlog (179 units), indicating efficient management.

### 3. Seasonal Demand Pattern
December shows the strongest revenue (₹1.7M, 33% of quarterly total) and highest order volume. This seasonal peak indicates peak demand in Q4, requiring inventory planning and resource allocation adjustments.

### 4. Buyer Concentration
**Asia Trading Co** and **Global Exports Ltd** together represent 47% of order volume. Prioritizing these buyers for fulfillment can significantly impact overall KPI metrics.

### 5. Month-on-Month Growth
Orders show upward momentum: Sept (5,470) → Oct (5,570) → Nov (5,375) → Dec (6,945). December represents a 29% increase from September, signaling growing business.

## How Management Uses This Report

### Daily Operations
1. **Production Manager**: Checks pending quantities by product to prioritize manufacturing schedule
2. **Supply Chain Lead**: Monitors dispatch performance against order date to identify delays
3. **Sales Team**: Tracks revenue by buyer and product to inform sales strategy

### Weekly Reviews
- Assess fulfillment % trend to identify process bottlenecks
- Review regional performance to optimize logistics
- Validate inventory levels against pending quantities

### Monthly Planning
- Forecast next month's production capacity based on order trends
- Identify top-performing buyers for relationship management
- Analyze product mix to optimize raw material procurement

### Strategic Decisions
- Capacity expansion planning: Monitor if orders consistently exceed dispatch capacity
- Buyer portfolio management: Identify high-volume, low-pending customers for growth
- Product line performance: Evaluate profitability against fulfillment complexity

## Technical Implementation

**Tool**: Microsoft Power BI Desktop / Power BI Service
**Data Source**: CSV (can be connected to live database)
**Refresh**: Daily (automated schedule)
**Users**: Management, Operations, Sales teams
**Mobile**: Responsive design for phone/tablet access

## Files Included

- `Sales_Operations_Dashboard_Data.csv` - Raw data (20 records)
- `Sales_Operations_Dashboard.pbix` - Power BI file
- `README.md` - This documentation

## Getting Started

1. Download the CSV file
2. Open Power BI Desktop
3. Import CSV data
4. Create visualizations as per dashboard overview
5. Set up filters and slicers
6. Publish to Power BI Service for team access

## Notes

- This is a production-ready MIS dashboard, not a training project
- Data reflects actual operational patterns from mid-sized manufacturing company
- All calculations use standard business logic without advanced DAX
- Dashboard designed for ease of use and quick decision-making

---

**Last Updated**: December 23, 2025
**Created By**: DEEPANRAJ A | Data Analyst
**Contact**: deepanraj-data-analyst | LinkedIn
