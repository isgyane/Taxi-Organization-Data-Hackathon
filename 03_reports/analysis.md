# Data Analysis Report

**Main Aim:** To identify factors that can increase the revenue of the taxi organization by analyzing trip data and customer behavior.

## 1. Overview
In this analysis, the provided dataset was examined to uncover key insights that could help drive revenue growth for the taxi organization. Key variables like `Total Amount`, `Fare Amount`, `Trip Distance`, and `Tip Amount` were thoroughly explored. The dataset was clean and well-structured, which facilitated smooth exploratory data analysis (EDA) and data visualization efforts.

### Key Takeaways:
- **Revenue** is mostly linearly correlated with trip distance. 
- **Distance** emerged as the most important driver for increasing fare amounts.
- **Traffic conditions** play a significant role in revenue generation, with moderate traffic contributing the most revenue.
- Revenue is slightly higher on specific weekdays, but a linear correlation between the day of the week and revenue was minimal.
- **Drop-off Time Analysis:** 19 out of 1000 trips had a drop-off date extending into the next day, indicating that nighttime travel demand is low.

---

## 2. Data Transformations
- **PowerBI Data Modeling:** Calculated columns (e.g., total revenue, duration) were created using Power Query (instead of DAX ) - this helped to optimize performance and minimize the model's size
- **Calendar Table:** Generated using Power Query’s M-Language

---

## 3. Issues with the Dataset
- **Customer ID Limitation:** Each trip is linked to only one `Customer ID`, but the number of passengers per trip ranges from 1 to 4. This limits our ability to track multiple passengers on the same trip, which could potentially lead to revenue miscalculation if multiple people split the fare.

---

## 4. Revenue Drivers
### Top Revenue Insights:
1. **Trip Purpose:** Errands generated the most revenue, followed closely by business trips. However, the differences among the five groups were minimal.
2. **Day of the Week:** Revenue peaked on **Tuesdays, Wednesdays, and Fridays**. While weekends were slightly less profitable, the weekday variations weren’t strong enough to make definitive conclusions based solely on the day of the week.
3. **Traffic Conditions:** Trips during moderate traffic generated the most revenue. Surprisingly, light traffic saw lower revenue, likely due to shorter trips.
4. **Trip Distance:** Distance was the **strongest revenue driver**. This indicates that long-distance trips should be prioritized, especially during times of moderate traffic.

---

## 5. Correlation Analysis
- **Distance and Fare Amount:** Strong correlation (0.9), indicating that longer trips significantly increase fare revenue.
- **Duration and Distance:** Weak correlation, suggesting that distance is not necessarily linked to trip duration. This could be influenced by varying traffic conditions.
- **Traffic Conditions:** Moderate traffic generated the most revenue, while light traffic contributed the least.

### Important Notes:
- **Low correlation between `nearly all variables` and `Total Fare`:** This near-zero correlation may suggest that external factors like promotions, events, or holidays could play a larger role in influencing daily revenue - non-linear relationships might exist between variables. Methods like **decision trees** or **random forests** could help uncover more complex relationships.

---

## 6. Visual Insights (PowerBI Dashboard)
1. **Revenue by Location:** Uptown generated the most revenue, followed by Midtown.
2. **Traffic and Revenue:** Moderate traffic yielded the highest revenue, suggesting that focusing on high-traffic times can optimize profits.
3. **Pickup Zones:** Five key pickup zones generated more trips, contributing the most to revenue.
4. **Trip Duration:** Most trips lasted between 45 and 60 minutes, with an overall average duration of **32 minutes** for all trips.
5. **Driver Performance:** Some drivers completed more trips but generated less revenue per trip. Others had fewer trips but higher revenue per trip, indicating route optimization and efficiency variations.
6. **Demand Patterns:** Demand for taxis peaked on **Thursdays** (mainly for leisure), followed by **Tuesdays and Wednesdays** for errands.

---

## 7. Troubleshooting Python Integration in PowerBI
While doing correlation analysis in PowerBi, I faced some challenges with integrating Python into PowerBi. I have outlined below the steps I took to resolve the issue. I hope it helps 😊

To successfully run Python scripts within PowerBI, follow these steps:
1. Open a **Miniconda/Anaconda prompt**.
2. Run `conda info --envs` to list available environments.
3. If necessary, create a new environment using `conda create --name [env_name]`.
7. Run `conda list` to ensure required packages like `numpy`, `pandas`, and `matplotlib` are installed. Install necessary packages where applicable
4. Activate the necessary environment using `activate [env_name]`.
5. Open **PowerBI** from the command line, ensuring the environment is activated.
    To find your PowerBi executable, use EVERYTHING app (filter to exe and search for PBIDesktop)
    Copy the path and use within the Miniconda/Anaconda prompt
6. In PowerBI settings, ensure the correct environment path is set under Python Scripting options.
