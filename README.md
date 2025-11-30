📊 OTT Dashboard – Power BI

This project contains a 3-page Power BI dashboard that analyzes content from Netflix, Amazon Prime, and Disney+ Hotstar using publicly available datasets.

📁 Folder Structure
📁 Datasets/           # CSV files used in the dashboard
📁 Pictures/           # Logos used inside the report
OTT_Dashboard.pbix     # Main Power BI file
OTT_Dashboard.pdf      # Exported PDF of the dashboard
📄 Dashboard Pages

Netflix Page
Total Shows, Movies, Series
Total Box Office
IMDb Score
Show Duration donut chart
Yearly Releases
Awards by Year
View Rating distribution
Genre + Searchable List of Shows
Red Netflix-style design

Amazon Prime Page
Total Shows, Movies, Series
Type filter (Movie / TV Show)
Description panel
Genre, Duration, Director filters
Rating distribution
Blue Prime-style design

Disney+ Hotstar Page
Total Shows, Movies, Series
Yearly Release Trend
Genre, Duration, Director filters
Rating distribution
Show description section
Blue Hotstar-style design

Main DAX Measures (Simplified)
Shows Prime = DISTINCTCOUNT(Amazontitles[show_id])

Movies Prime =
CALCULATE([Shows Prime], Amazontitles[type] = "Movie")
Series Prime =CALCULATE([Shows Prime], Amazontitles[type] = "TV Show")

Movies Prime % = DIVIDE([Movies Prime], [Shows Prime])
Series Prime % = DIVIDE([Series Prime], [Shows Prime])

▶ How to Use
Open OTT_Dashboard.pbix in Power BI Desktop.
Make sure the Datasets folder stays in the same location.
Use slicers and navigation buttons to explore each platform.
