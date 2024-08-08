# A/B Testing of Website Landing Pages

## Project Overview

This project involves conducting an A/B test to compare the effectiveness of two different website landing pages: the old landing page and the new landing page. The objective is to determine which page performs better in terms of user engagement, conversions, or other relevant metrics.

### Experimental Design

- **Control Group:**  
  Users in this group were shown the **new landing page**.
  
- **Treatment Group:**  
  Users in this group were shown the **old landing page**.

### Data Overview

The dataset contains user interaction data with the following key attributes:

- **`group`:** Indicates whether the user was in the control or treatment group.
- **`landing_page`:** Indicates whether the user saw the old landing page or the new landing page.
- **`converted`:** A binary indicator of whether the user performed the desired action (e.g., signing up, purchasing, etc.).

### Data Anomalies

During the initial data exploration, it was discovered that some users were assigned to the wrong landing pages:

- **Control Group:** Users in this group should have been shown the new landing page, but some were shown the old page.
- **Treatment Group:** Users in this group should have been shown the old landing page, but some were shown the new page.

These discrepancies were addressed before proceeding with the analysis to ensure accurate results.

## Methodology

1. **Data Cleaning:**  
   - Removed records where the `group` and `landing_page` did not match the intended experimental design (e.g., control group with old page or treatment group with new page).

2. **Exploratory Data Analysis (EDA):**  
   - Performed EDA to understand the distribution of the data, conversion rates across groups, and any potential biases.
  
3. **Statistical Testing:**  
   - Applied hypothesis testing to determine whether the difference in conversion rates between the old and new landing pages is statistically significant.

4. **Results Interpretation:**  
   - Analyzed the p-value and confidence intervals to draw conclusions about the effectiveness of the new landing page compared to the old one.

## Conclusion

The A/B test provided insights into the relative performance of the old and new landing pages. Based on the results of the hypothesis testing, recommendations were made regarding which page the website should use to maximize user engagement and conversions.

## Files Included

- `data/`: Contains the cleaned and processed A/B testing data.
- `scripts/`: R scripts for data cleaning, EDA, and hypothesis testing.
- `Rmd/`: R Markdown files documenting the entire analysis process.
- `README.md`: This document.

## How to Run

1. Clone the repository.
2. Install the required R packages listed in the `Rmd/` files.
3. Open the R Markdown files in the `Rmd/` directory and run the analysis to reproduce the results.

## Acknowledgments
