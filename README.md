# Taxi Organization Revenue Analysis


[Dashboard Overview](/04_visuals/PBIDesktop_Taxi.gif)

## Overview
This project explores trip data from a taxi organization to help drive revenue growth. By analyzing key metrics like fare amounts, trip distances, and traffic conditions, I aim to uncover insights that could optimize the taxi company’s operations and increase profitability.

### Dataset:
- **Number of Records:** 1,000 trips
- **Key Variables:** 
  - `Total Amount`
  - `Fare Amount`
  - `Trip Distance`
  - `Tip Amount`
  - `Day of the Week`
  - `Traffic Conditions`

---

## Key Insights
- **Trip Distance** has the strongest impact on revenue.
- **Moderate Traffic Conditions** generate the highest revenue.
- **Errands** and **Business Trips** account for the most profitable trip purposes.
- Revenue is highest on **Tuesdays, Wednesdays, and Fridays**.

---

## Project Structure

```
/Taxi_Revenue_Analysis/
│
├── /01_data/                     # Contains the dataset(s)
│
├── /02_notebooks/                # Jupyter notebooks for EDA
│
├── /03_reports/                  # Documentation and analysis notes
│
├── /04_visuals/                  # PowerBI files and other visualizations
│
├── /09_charticons/               # SVGs and PNGs used to enhance the PowerBi visual
│
└── README.md                     # Overview of the project
```

---

## How to Run the Project
1. **Data Analysis:** The Jupyter notebook (`eda_analysis.ipynb`) can be used to explore the dataset and examine key correlations.
2. **PowerBI Dashboard:** The PowerBI file (`revenue_analysis.pbix`) provides visual insights into driver performance, trip duration, and revenue trends.
3. **Python Integration with PowerBI:**
   - Ensure your environment is activated by opening PowerBI from the **Miniconda** prompt (see `analysis_notes.md` for troubleshooting).

---

## Requirements
- **PowerBI Desktop**
- **Python 3.7+** with libraries:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `seaborn`

--- 

## Next Steps
- **Explore Non-linear Relationships:** Future analysis should employ machine learning techniques such as **decision trees** or **random forests** to explore non-linear relationships between trip features and revenue.
- **Customer Segmentation:** Investigating customer behavior based on trip purposes and locations could offer personalized services that increase overall revenue.


## Troubleshooting Python Integration in PowerBI
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