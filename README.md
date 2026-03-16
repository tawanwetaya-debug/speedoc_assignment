Home Healthcare Visit Analysis

Project Overview
This project analyzes home healthcare visit data to understand service duration patterns, urgent cases, and operational characteristics. 
The goal is to explore the dataset, data manipulation and data imputation and identify insights that could improve service efficiency and scheduling.

The analysis is performed using Python with Pandas and Matplotlib in a Jupyter Notebook environment.
-----------------------------------------------------------

Project Structure
    LittleSteps/
    │
    ├── data/
    │   └── visits.csv          # Raw dataset
    │
    ├── data_analysis.ipynb     # Data cleaning and analysis notebook
    ├── requirement.txt         # Required Python libraries
    └── README.md               # Project documentation
--------------------------------------------------------------

Dataset Description

The dataset contains records of healthcare visits performed by nurses.

Original Variables

The dataset includes the following key variables:

    visit_id – Unique identifier for each visit

    nurse_id – Unique identifier for each nurse

    patient_id – Unique identifier for each patient

    service_type – Type of healthcare service provided

    visit_location – Location where the visit occurred

    visit_start_time – Timestamp when the visit started

    visit_end_time – Timestamp when the visit ended

    nurse_notes – Text notes written by the nurse describing the visit

Derived Variables

Additional variables were created during the analysis to support further insights:

    urgent_case – Indicates whether the visit is urgent based on keywords detected in the nurse notes

    revisit_case – Indicates whether the visit is a follow-up visit based on keywords detected in the nurse notes

    visit_duration_minutes – Calculated as: visit_end_time − visit_start_time

    travel_duration_minutes – Estimated travel time between visits.

For the first service of the day, a default 30 minutes response time is assumed.

If the calculated travel duration is negative (due to data logging inconsistencies), the value is marked as 999 to indicate a potential data error.
--------------------------------------------------------------

Analysis Performed

The analysis includes:

    Data cleaning and preprocessing

    Calculation of visit duration

    Histogram visualization of visit durations

    Box plots to analyze duration distribution

    Bar charts comparing average visit duration by service type and location

Comparison between urgent and non-urgent cases
--------------------------------------------------------------

Technologies Used

Python

Pandas

Matplotlib

Jupyter Notebook
--------------------------------------------------------------

How to Run the Project

Clone the repository

git clone https://github.com/yourusername/littlesteps-analysis.git

Install required libraries

pip install -r requirement.txt

Run the notebook

jupyter notebook data_analysis.ipynb