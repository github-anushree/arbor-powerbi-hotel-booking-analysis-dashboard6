#  Hotel Booking Analysis Dashboard | Power BI Project  

##  Project Overview  
This Power BI project analyzes hotel booking data from City and Resort hotels to identify trends in bookings, cancellations, lead time, and customer behavior.  
The dashboard provides data-driven insights to help hotel management improve pricing strategies, reduce cancellations, and increase occupancy rates.  

---

## 🎯 Project Objectives  
- Understand booking patterns and customer behavior.  
- Identify major factors driving cancellations.  
- Analyze revenue performance by hotel type, country, and booking channel.  
- Compare City vs. Resort hotels based on key KPIs.  
- Provide actionable insights for business growth and better customer retention.  

---

## 🧹 Data Cleaning (KYD Process)
Performed thorough cleaning to ensure accuracy and reliability:
- Verified dataset size: **119,390 rows × 32 columns**.  
- Filled missing values:  
  - `children` → 0  
  - `country` → “Unknown”  
  - `agent` → “Direct Booking”  
  - `company` → “No Company” (removed later due to high nulls)  
- Fixed invalid ADRs (negative values and extreme outliers).  
- Removed duplicates and standardized text formats.  
- Created valid `arrival_date` and derived `booking_date = arrival_date - lead_time`.  
- Added calculated fields like `total_guests`, `total_nights`, and `is_family_booking`.

---

## 🔧 Data Transformation / Wrangling  
Data transformed in **Power Query** for better analysis:
- Created `BookingID` as unique key.  
- Derived fields:  
  - `total_guests = adults + children + babies`  
  - `total_stay = stays_in_weekend_nights + stays_in_week_nights`  
  - `revenue = adr × total_stay`  
- Grouped ADR and Lead Time into bins for trend analysis.  
- Created dimension tables for Hotel, Country, and Room Type.  
- Built star schema data model in Power BI for fast performance.  

---

## 🧠 Data Modeling  
- **Model Type:** Star Schema  
- **Fact Table:** Hotel_Bookings_Clean  
- **Dimension Tables:** DimHotel, DimRoom, DimCountry, Date Table  
- Relationships established via primary keys.  
- Used Date Table for time-intelligence calculations (Yearly, Monthly trends, etc.).

---

## 📈 Dashboard Design Strategy  
The Power BI dashboard was divided into **3 main pages** to address specific business areas:  

1. **Executive Overview** – High-level KPIs for management (Bookings, ADR, Revenue, Cancellations).  
2. **Channels, Pricing & Guests** – Insights on booking sources, guest types, ADR distribution, and lead time.  
3. **Operational Insights** – Cancellation patterns, occupancy trends, and drill-through analysis.

Each page includes interactive slicers, buttons, and a Q&A section for quick analysis.

---

## 📊 Key KPIs  
| KPI | Description |
|------|--------------|
| Total Bookings | Number of confirmed bookings |
| Total Revenue | Sum of ADR × total nights |
| ADR (Average Daily Rate) | Average revenue per room night |
| Cancellation Rate | % of bookings canceled |
| Repeat Guest Rate | % of repeat customers |
| Avg Lead Time | Days between booking and arrival |

---

## 💡 Business Insights  

### 🔹 **Executive Overview Dashboard**
- **City Hotels** generated **61% of bookings**, showing higher urban demand.  
- **Resort Hotels** had fewer bookings but a higher ADR.  
- Revenue peaked in **2016**, with a slight drop in **2017**.  
- **Top 3 revenue countries:** Portugal, UK, and France.  

### 🔹 **Channels, Pricing & Guests Dashboard**
- **Online Travel Agencies (OTA)** dominate bookings (~99%), but also drive the **highest cancellations**.  
- **ADR distribution** shows most bookings in the €50–€200 range (mid-range pricing segment).  
- **Repeat guests** contribute less than 4% of total revenue — low customer retention.  
- **Lead time analysis:** Most bookings are made within 0–100 days of arrival.

### 🔹 **Operational Insights Dashboard**
- **Occupancy trends** peak between **May–August** — strong summer demand.  
- **Cancellations** are higher in OTA and group segments with longer lead times.  
- **Direct bookings** and **corporate clients** show more stable and reliable performance.  

---

## 🧩 Recommendations  
1. **Implement Dynamic Pricing:** Adjust room rates based on demand and seasonality to optimize ADR.  
2. **Strengthen Loyalty Programs:** Encourage repeat bookings through discounts or rewards.  
3. **Introduce Non-refundable Plans:** Reduce OTA cancellations with stricter policies.  
4. **Focus on High-Revenue Markets:** Target Portugal, UK, and France for marketing campaigns.  
5. **Automate Cancellation Prediction:** Use Power BI + ML to forecast and minimize cancellations.  

---

## 🚀 Expected Business Impact  
- 10–15% reduction in cancellations.  
- 5–8% increase in occupancy rate.  
- Better pricing control and revenue forecasting.  
- Improved customer retention and satisfaction.

---

## 🛠️ Tools & Technologies  
- **Power BI** – Dashboard, KPIs, and visual analysis.  
- **Power Query** – Data cleaning and transformation.  
- **DAX** – Calculated columns and measures.  
- **Excel** – Initial data exploration and validation.  
- **Data Model:** Star Schema (Fact + Dimension tables).  

---

## 📷 Dashboard Preview  
*(Add screenshots of your 3 dashboard pages here — Executive Overview, Channels & Guests, Operational Insights)*  

---

## 👩‍💼 Author  
**Anushree Kashyap**  
Data Analyst | Power BI Developer  
[LinkedIn Profile](https://www.linkedin.com/in/anushreekashyap/) | [Medium Profile](https://medium.com/@anushreekashyap03)

---

### ⭐ *If you found this project insightful, please star this repository and share your feedback!*
