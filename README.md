- 👋 Hi, I’m Chih-Chung Wuo but you can call me Kirk.
- 💥 Graduated from the MIT Professional Education Applied Data Science Program:
        Proud of our team's achievement in securing first place at an MIT hackathon during the program.  
      - Credential: https://www.credential.net/aa5ebda3-e6d5-4f08-8921-c2cc6f234f2c#gs.33b2cu  
      - Details of the achievements: https://eportfolio.mygreatlearning.com/chih-chung-wuo  
      - Detailed of this program: https://www.mygreatlearning.com/mit-data-science-program?utm_source=eportfolio&gl_source=Linkedin&gl_campaign=Eportfolio
- 🌱 I am a Google certified Business Intelligence Analyst:  
      - Credential: https://www.credly.com/badges/acfdbe53-c1db-463a-a336-f05826e20120/linked_in_profile
      - Detailed List of achievements: https://www.coursera.org/account/accomplishments/professional-cert/RD07RG3O2LOB
- 🌱 I am a Google certified Data Analyst:  
      - Credential: https://www.credly.com/badges/10c5a68a-e43d-460c-8719-ded431127847  
      - Detailed List of achievements: https://www.coursera.org/account/accomplishments/professional-cert/FC3DPWYT8USE  
- 👨🏻 I have been working in freight logistic industry for 18+ years and still going strong!
- 💎 Diploma in Computer System from British Columbia Institute of Technology (BCIT).
- 💎 B.Sc. Chemistry from Simon Fraser University (SFU).

#### Here is a list of my analysis on Kaggle:
[Cyclistic Bike Usage Analysis: using R](https://www.kaggle.com/code/chihchungwuo/cyclistic-bike-usage-analysis)

-------------------------------------------------------------------------------

#### Here is a list of dashboards built using Tableau Public:

[ICBC Road Safety & Casualty Severity Intelligence](https://public.tableau.com/views/ICBCRoadSafetyCasualtySeverityIntelligence/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
<br>✅Full end-to-end BI pipeline: 835k+ records stored in a Dockerized PostgreSQL database, aggregated via complex SQL queries in DBeaver, and visualized in Tableau Public.
<br>✅Uncovered the "Surrey-Vancouver Paradox": proving suburban arterial grids in Surrey experience a 43.6% higher casualty rate than Vancouver despite lower total crash volume.
<br>✅Features synchronized cross-filtering, interactive year slicers, executive KPI cards, and road user mode risk analysis.

<details>
<summary><b>🔍 View SQL Data Mart Query & Docker Configuration</b></summary>
<br>

**Analytical Aggregation Query (PostgreSQL / DBeaver)**

```sql
-- ICBC Road Safety Data Services
-- Analytical Mart: Aggregating 835k+ raw records across temporal, spatial, and risk dimensions

SELECT 
    "Date Of Loss Year",
    "Municipality Name",
    "Crash Location",
    "Motorcycle Involved",
    "Heavy Truck Involved",
    COUNT(*) AS "Total Crashes",
    SUM(CASE WHEN "Casualty Severity" = 'Y' THEN 1 ELSE 0 END) AS "Total Victims"
FROM icbc_crashes_raw
GROUP BY 
    "Date Of Loss Year",
    "Municipality Name",
    "Crash Location",
    "Motorcycle Involved",
    "Heavy Truck Involved";
```

**Database Container Spec (`docker-compose.yml`)**

```yaml
version: '3.8'
services:
  icbc_postgres:
    image: postgres:15
    container_name: icbc_safety_db
    environment:
      POSTGRES_USER: ${POSTGRES_USER:-postgres}
      POSTGRES_DB: ${POSTGRES_DB:-icbc_analytics}
      POSTGRES_PASSWORD: ${POSTGRES_PASSWORD} # Injected locally via untracked .env file
    ports:
      - "5433:5432"
    volumes:
      - pgdata:/var/lib/postgresql/data

volumes:
  pgdata:


</details>

</details>

[Cyclistic Bike-Share Rental](https://public.tableau.com/views/CyclisticRideSharing_17296376772410/MainDash?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
<br>✅Multiple dashboards navigation

[Canadian Seafood Export](https://public.tableau.com/views/CanadianSeafoodExport/MostValuableSeafoodDashboard?:language=en-US&:display_count=n&:origin=viz_share_link)
<br>✅Multiple dashboards navigation.

[Global Retail Dashboard (using Kaggle dataset)](https://public.tableau.com/app/profile/kirk1022/viz/GlobalRetailSalesKaggleData/RetailDashboard)
<br>✅R was used to clean and sample original dataset which was too large for our task. Output CSV for Tableau Public to import.

[Google's Stock Chart for Investor](https://public.tableau.com/app/profile/kirk1022/viz/GooglesStockChartforInvestor/GoogleStocks)
<br>✅Google Sheet was used to get data from Google Finance.
<br>✅Tableau Public then sync with the Google Sheet to get data.

[Reasons Why Business Not Adopting Advanced Technology](https://public.tableau.com/views/ReasonsWhyBusinessNotAdoptingAdvancedTech/DashboardforReasonThatBusinessDoNotAdoptAdvancedTech?:language=en-US&:display_count=n&:origin=viz_share_link)
<br>✅Data was obtained from Canadian government's Open Data website. 

<!---
kirkovski/kirkovski is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
