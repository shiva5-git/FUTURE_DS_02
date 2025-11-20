📣 Social Media Campaign Performance Tracker
Power BI Dashboard — Facebook & Instagram Ad Analytics

This project analyzes Facebook and Instagram ad campaign data to evaluate engagement, CTR, CPC, conversions, and ROI.
The dashboard helps understand campaign effectiveness, platform performance, and budget optimization.

It is designed for digital marketers, analysts, and businesses focusing on social media growth and paid advertising.

#Dashboard Preview
![WhatsApp Image 2025-11-20 at 19 48 37_c1e0d00d](https://github.com/user-attachments/assets/9c64fe98-7f45-40e4-b82f-e73b1119dff3)


📁 Project Structure
📦 Social-Media-Campaign-Tracker
 ┣ 📊 Dashboard_Screenshots/
 ┣ 📜 Campaign_Analytics.pbix
 ┣ 📂 Dataset/
 ┃ ┗ social_media_campaign.csv
 ┗ 📄 README.md

🎯 Project Objective

To evaluate the performance of various social media ad campaigns by analyzing:

Impressions & Reach

Clicks and CTR

Engagement Rates

Cost Efficiency (CPC)

Conversions

Return on Investment (ROI)

Platform comparisons (Facebook vs Instagram)

🛠️ Tools & Technologies Used
Tool	Purpose
Power BI Desktop	Visualization & dashboard building
Power Query Editor	Data cleaning & transformation
DAX	Calculations (CTR, CPC, ROI)
CSV Dataset	Raw campaign data
Excel	Preprocessing (optional)
📥 Dataset Summary

Sample dataset fields include:

Campaign ID

Platform (Facebook / Instagram)

Impressions

Clicks

Conversions

Likes, Comments, Shares

Amount Spent

Revenue

Each record represents a campaign’s performance on a specific platform.

🧹 Data Cleaning Process (Power Query)

Performed using Power Query Editor:

Removed null/empty records

Converted numeric fields (Clicks, Impressions, Cost, Revenue)

Created new fields:

Engagement Count

CTR

Engagement Rate

Removed rows where Impressions = 0 (invalid CTR)

🧠 Data Modeling

Single-table model with additional calculated columns:

Engagement = Likes + Comments + Shares

CTR% = (Clicks / Impressions) × 100

ROI% = (Revenue – AmountSpent) / AmountSpent × 100

No complex relationships needed for this dataset.

🔢 DAX Measures Used
Total Impressions = SUM(Campaign[Impressions])

Total Clicks = SUM(Campaign[Clicks])

CTR % = DIVIDE([Total Clicks], [Total Impressions], 0) * 100

Total Engagement =
SUM(Campaign[Likes]) + SUM(Campaign[Comments]) + SUM(Campaign[Shares])

Engagement Rate =
DIVIDE([Total Engagement], [Total Impressions], 0) * 100

CPC = DIVIDE(SUM(Campaign[AmountSpent]), [Total Clicks])

ROI % =
DIVIDE(SUM(Campaign[Revenue]) - SUM(Campaign[AmountSpent]),
       SUM(Campaign[AmountSpent])) * 100

📊 Dashboard Features
✔ KPI Cards

710K Impressions

95K Clicks

13.4% CTR

4,700 Conversions

✔ CTR Formula & Explanation

Displayed clearly to educate non-technical users.

✔ Engagement Split (Donut Chart)

Shows platform-level engagement:

55% Facebook

45% Instagram

✔ CPC vs CTR Scatter Plot

Helps compare campaign efficiency based on:

Cost per Click (CPC)

Click Through Rate (CTR)

✔ ROI by Campaign (Bar Chart)

Shows profitability of each campaign (A, B, C).
Helps decide which campaigns to scale or optimize.

📈 Insights & Findings

Facebook has slightly higher engagement than Instagram (55% vs 45%).

CTR of 13.4% is strong, showing effective ad creative.

Campaign A produces the highest ROI → should receive higher budget.

Campaign C has the lowest ROI → requires optimization or pause.

CPC vs CTR scatter plot highlights which campaigns are cost-effective.

Engagement levels show which platform works best for interactions.
