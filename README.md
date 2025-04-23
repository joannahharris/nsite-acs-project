# Commuting Patterns Analysis: Who Spends More Time Commuting?

## Introduction
The transition back to the office has raised questions about commuting times across different demographics and metropolitan areas. This project leverages real-world data to answer the question:  
**"With the current drive towards back to the office, who actually spends more time commuting to work?"**

In this 180-second data story, we utilize a maximum likelihood estimation (MLE) approach to analyze and interpret commuting patterns. The insights derived not only inform transportation policy debates but also help to understand modern workforce dynamics.

## Data Sources

### Commute Time Data
The analysis is based on detailed commuting data from the American Community Survey (ACS), accessible via the IPUMS USA datasets. The ACS provides comprehensive information on travel times and commuting modes, which is essential for accurately assessing the commuting burden.

![Logo for IPUMS USA](https://www.ipums.org/sites/www.ipums.org/files/project-logo/logo-usa_0.png)

- **Data Portal:** [IPUMS USA Datasets](https://usa.ipums.org/usa/)

### Key Variables
- **YEAR:**  
  - Data from the years 2021, 2022, and 2023

- **TRAVEL_TIME:**  
  - Measured in minutes, this variable records the total time spent commuting.

- **METRO:**  
  - 1 = Not in metropolitan area  
  - 2 = In metropolitan area (central/principal city)

- **COMMUTE_MODE:**  
  - 11 = Auto  
  - 60 = Walked only  
  - 31 = Bus  
  - 50 = Bicycle

## Methodology
This project employs a maximum likelihood estimation (MLE) approach to determine statistically significant patterns in commuting times. The MLE method was chosen for its robustness in parameter estimation, which allows for statistical modeling of travel time distributions.

## Preliminary Results
While the complete analysis is best experienced by running the code, key initial findings suggest interesting disparities in commuting times based on metropolitan status and mode of transportation. These results hint at underlying socio-economic patterns that warrant further investigation.

## How to Run This Project
To replicate the analysis:
1. **Prerequisites:** Ensure you have the required statistical libraries installed (e.g., NumPy, SciPy, Pandas, Matplotlib). As well as audio-plot-lib.
2. **Installation:** Clone the repository and install dependencies (see enviroment.yml).
3. **Download the data from IPUMS** We used a 3% sample of ACS data with key attributes () from 2021, 2022, and 2023
