Sales_Performance_Dashboard
Interactive Excel Sales Performance Dashboard build using 51k+ records, XLOOKUP, Pivot Tables and Slicers.

📌 Executive Summary
An end-to-end interactive Sales Performance Dashboard built using Microsoft Excel to analyze over 51,000+ transaction records across global regions. The project covers data cleaning, relational data modeling (XLOOKUP), pivot table aggregation, and dynamic UI/UX visual formatting.

📈 Key Metrics & Highlights
Total Revenue Verified: $12,642,501.91
Total Dataset Volume: 51,290+ rows
Data Period Covered: 2012 – 2015
Key Dimensions Analyzed: Category, Sub-Category/Department, Region, Year, Order Status (Returns), Regional Leadership (People)

🛠️ Step-by-Step Project Workflow
1. Data Cleaning & Relational Data Modeling
Applied XLOOKUP to integrate Returns and People datasets into the primary Orders table.
Extended order details with custom fields:
Returned Status: =IFERROR(XLOOKUP(B2, Returns!B:B, Returns!A:A), "No")
Regional Manager: =IFERROR(XLOOKUP(N2, People!B:B, People!A:A), "Unknown")
Year Field Extraction: =YEAR(Order_Date_Cell) for clean temporal grouping.

3. Pivot Table Architecture
Created 4 core Pivot Tables to feed visual elements, ensuring strict reconciliation against the grand sum of $12,642,501.91:
Total Revenue Scorecard: Overall summary aggregate.
Category Performance: Revenue breakdown across Furniture, Office Supplies, and Technology.
Sub-Category / Department Breakdown: Granular sub-category revenue performance.
Yearly Sales Trend: Historical revenue trajectory from 2012 to 2015.

4. Interactive Dashboard Design & Formatting
Visual Elements: Doughnut Chart (Category), Horizontal Bar Chart (Department), Line Chart with Markers (Yearly Trend), Dynamic KPI Card.
Interactivity: Integrated Region and Year Slicers connected via Report Connections to update all charts and metrics simultaneously.
UI Cleanliness: Hidden Field Buttons, custom color palettes, gridlines removed, and title banners added.
