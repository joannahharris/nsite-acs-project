# Commuting Patterns Analysis: Who Spends More Time Commuting?

## Introduction
The following data story will present findings from my analysis of a deceptively simple question: "Who spends more time commuting, rural drivers or urban drivers?". This research challenges fundamental assumptions about geography and mobility while demonstrating how accessibility can be seamlessly integrated into rigorous data science project. 

To answer this question, I gathered data from the IPUMS American Community Survey microdata spanning 2021-2023 including non-metropolitan areas and metropolitan areas located in central/principal cities. I then analyzed the dataset using Python with Pandas, Matplotlib, NumPy, and SciPy. The statistical approach employed a log-normal distribution for modeling with maximum likelihood estimation to characterize commute time patterns by calculate measures of central tendency and dispersion.

Critically, this project embedded WCAG 2.2 AA accessibility standards throughout the entire workflow. The chosen development environment utilized Visual Studio with high contrast mode and screen reader compatibility, meeting success criteria for 1.4.3 Contrast (Minimum) and 4.1.2 Name, Role, Value. All documentation implemented logical heading structures per 2.4.6 Headings and Labels, included comprehensive alt text for visualizations following 1.1.1 Non-text Content, and semantic markup for mathematical expressions ensuring assistive technology compatibility under 1.3.1 Info and Relationships. Furthermore, I integrated audioplotlib which is an experimental sonification library that converts statistical visualizations into auditory representations, this extending beyond standard 1.2.1 Audio-only and Video-only (Prerecorded) requirements to provide enhanced accessibility for blind and low-vision users.

This project proves that research can be both scientifically rigorous and accessible to all. By combining robust statistical modeling with inclusive design, we not only challenge long-standing assumptions with empirical evidence, we make that evidence usable and meaningful to a broader audience. This is the kind of work I am passionate about.

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
This project employs a maximum likelihood estimation (MLE) approach to determine statistically significant patterns in commuting times. The log-normal MLE method was chosen due to the skewed nature of the data with more frequency of shorter commute times and a lower frequency of long commute times. 

## Preliminary Results
While the complete analysis is best experienced by running the code, the results fundamentally challenge conventional wisdom. Despite widespread assumptions that rural workers endure long commutes or urban drivers crawl through endless traffic, the empirical distributions revealed statistically equivalent commute times between rural and urban automobile commuters. The log-normal models demonstrated remarkable similarity in both mean duration and variance.

## How to Run This Project
To replicate the analysis:
1. **Prerequisites:** Ensure you have the required statistical libraries installed (e.g., NumPy, SciPy, Pandas, Matplotlib). As well as audio-plot-lib.
2. **Installation:** Clone the repository and install dependencies (see enviroment.yml).
3. **Download the data from IPUMS** You will need to make an account with [IPUMS USA Datasets](https://usa.ipums.org/usa/) to download the data. For our examples, we used a 3% sample of ACS data from 2021, 2022, and 2023 with key attributes YEAR, STATEFIP, PUMA, METRO, PWSTATE2, TRANWORK, TRANTIME.
4. 
